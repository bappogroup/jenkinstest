pipeline {
    triggers {
        upstream (
            threshold: 'SUCCESS',
            upstreamProjects: 'backendtrigger'
        )
    }
    stages {
        stage('Example Build') {
            steps {
                sh 'echo helllloooo'
            }
        }
    }
}
