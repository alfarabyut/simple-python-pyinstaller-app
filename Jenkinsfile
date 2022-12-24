node {
        stage('Build') {
        docker.image('python:2-alpine')
        sh 'python3 -m ./sources/add2vals.py ./sources/calc.py'
        }
}