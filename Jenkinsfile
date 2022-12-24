node {
        stage('Build') {
        docker.image('python:2-alpine')
        sh 'python3 -m py_compile /home/Downloads/simple-python-pyinstaller-app/sources/add2vals.py /home/Downloads/simple-python-pyinstaller-app/sources/calc.py'
        }

      
        stage('Test') {
                docker.image('qnib/pytest')
                sh 'py.test --verbose --junit-xml test-reports/results.xml sources/test_calc.py'
        
            }
       

}