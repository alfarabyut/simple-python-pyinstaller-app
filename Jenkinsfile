node {
        stage('Build') {
        docker.image('python:2-alpine')
        sh 'python3 -m py_compile /home/Downloads/simple-python-pyinstaller-app/sources/add2vals.py /home/Downloads/simple-python-pyinstaller-app/sources/calc.py'
        }

        stage ('Test') {
        
        sh 'python3 -m unittest --junit-xml test-reports/results.xml sources/test_calc.py'
        }
}