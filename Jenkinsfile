pipeline {
    agent any
    stages {
        stage('Example Build') {
            steps {
                sh 'git diff --name-only HEAD~2..HEAD'
            }
        }
    }
}
