node {
        stage('Build') { 
            docker.image('python:2-alpine').inside {
                    sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
                    stash includes: 'sources/*.py', name: 'compiled-results' 	
            }
        }             
        stage('Test') {
            docker.image('qnib/pytest:latest').inside {
                sh 'py.test --junit-xml test-reports/results.xml sources/test_calc.py'
                junit 'test-reports/results.xml'
            }
        }
        stage('Manual Approval') {
            input message: 'Lanjutkan ke tahap Deploy?', ok: 'Proceed'
        }
        stage('Deploy') {      
                unstash 'compiled-results'    
                archiveArtifacts 'sources/'
                sleep time: 1, unit: 'MINUTES'
        }
}