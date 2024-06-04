pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/narharigtm/Java_Project.git']])
            }
        }
        stage('build & run'){
            steps{
                sh 'docker-compose up -d'
                sh 'docker ps'
            }
        }
    }
    
}
