pipeline {
    agent any
    
    stages {
//        stage('Clone repository') {
//            steps {
//                checkout([$class: 'GitSCM', 
//                    branches: [[name: '*/main']], 
//                   userRemoteConfigs: [[url: 'https://github.com/roshnav2025/PES2UG21CS438_JENKINS']]])
//            }
//        }
       
        stage('Build') {
            steps {
                build 'PES2UG21CS438-1'
                sh 'g++ main/hello.cpp -o output'
            }
        }
        
        stage('Test') {
            steps {
                sh './output'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
