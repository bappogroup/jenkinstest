def CHANGED_FILES = ' '
pipeline {
    agent any
    stages {
        stage('Example Build') {
            steps {
                script {
                    CHANGED_FILES = sh (
                        script: 'git diff --name-only HEAD~2..HEAD',
                        returnStdout: true
                    ).trim()
                    echo "Changed Files: ${CHANGED_FILES}"
                }
            }
        }
    }
}
