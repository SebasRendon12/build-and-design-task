pipeline {
    agent any
    stages {
        stage('Build'){
            steps {
                sh 'echo "Building..."'
                sh 'chmod 744 scripts/build.sh'
                sh 'scripts/build.sh'
                archiveArtifacts artifacts: 'bin/Debug/*', fingerprint:true
            }
        }
        stage('Test'){
            steps {
                sh 'echo "Running..."'
                sh 'chmod 744 scripts/run.sh'
                sh 'scripts/run.sh'
            }
        }
    }
}