pipeline {
    agent any
    stages {
        stage('Pre Build') {
            steps {
                sh 'rm ~/.dockercfg || true'
                sh 'rm ~/.docker/config.json || true'
                checkout scm
            }
        }
    }
    post {
        always {
            sh 'ls'
            archiveArtifacts artifacts: 'test_archive/test_logs/*.log'
        }
    }
}
