def DEPLOY_API = ' '
pipeline {
    agent any
    stages {
        stage('Example Build') {
            steps {
                script {
                    DEPLOY_API = sh (
                        script: 'git diff --name-only HEAD~2..HEAD | grep "abc/" ',
                        returnStatus: true
                    ) == 0
                }
            }
        }
        stage('deploy API') {
            steps {
                echo "value is ${DEPLOY_API}"
            }
        }
    }
}
