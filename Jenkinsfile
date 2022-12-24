node {
        stage('Build') {
        sh 'python3 -m py_compile /home/Downloads/simple-python-pyinstaller-app/sources/add2vals.py /home/Downloads/simple-python-pyinstaller-app/sources/calc.py'
        }

        stage ('Test') {
        sh 'python3  /home/Downloads/simple-python-pyinstaller-app/sources/test_calc.py'
        }
}