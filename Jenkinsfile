pipeline {
    agent any
    stages {
        stage('Build'){
            steps {
                sh 'echo "Building..."'
                sh 'chmod +x vendor/bin/premake/premake5'
                sh 'chmod +x scripts/build.sh'
                sh 'scripts/build.sh'
                archiveArtifacts artifacts: 'bin/Debug/*', fingerprint:true
            }
        }
        stage('Test'){
            steps {
                sh 'echo "Running..."'
                sh 'chmod +x vendor/bin/premake/premake5'
                sh 'chmod +x scripts/run.sh'
                sh 'scripts/run.sh'
            }
        }
    }
}