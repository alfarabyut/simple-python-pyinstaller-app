node {
        stage('Build') {
        docker.image('python:2-alpine')
        sh 'python3 -m py_compile /home/ubuntuvm/Downloads/simple-python-pyinstaller-app/sources/add2vals.py /home/ubuntuvm/Downloads/simple-python-pyinstaller-app/sources/calc.py'
        stash(name: 'compiled-results', includes: '/home/ubuntuvm/Downloads/simple-python-pyinstaller-app/sources/*.py*')
        }
}