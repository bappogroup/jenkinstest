pipeline {
    agent any
    stages {
        stage('Example Build') {
            SHOULD_DEPLOY = sh (
                script: 'git diff --name-only HEAD~2..HEAD | grep "abc/|README" ',
                returnStatus: true
            ) == 0
            echo "Build full flag: ${SHOULD_DEPLOY}"
        }
    }
}
