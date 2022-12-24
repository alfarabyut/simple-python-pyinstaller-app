node {
        stage('Build') {
        docker.image('python:2-alpine')
        sh 'python3 -m py_compile add2vals.py calc.py'
        stash(name: 'compiled-results', includes: 'sources/*.py*')
        }
}