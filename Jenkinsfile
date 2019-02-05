def DEPLOY_API = false
def DEPLOY_API_REGEX = "abc/"

pipeline {
    agent any
    stages {
        stage('Example Build') {
            steps {
                script {
                    DEPLOY_API = sh (
                        script: 'git diff --name-only HEAD~1..HEAD | egrep "${DEPLOY_API_REGEX}" ',
                        returnStatus: true
                    ) == 0
                }
            }
        }
        stage('deploy API') {
            when {
                expression { return DEPLOY_API }
            }
            steps {
                echo "value is ${DEPLOY_API}"
            }
        }
    }
}
