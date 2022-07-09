pipeline {
    stages {
        stage('Pre Build') {
            steps {
                sh 'rm ~/.dockercfg || true'
                sh 'rm ~/.docker/config.json || true'
                checkout scm
            }
        }
    }
}
