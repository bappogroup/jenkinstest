pipeline {
    agent any
    triggers {
        upstream (
            threshold: hudson.model.Result.SUCCESS,
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
