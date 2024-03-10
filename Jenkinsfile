pipeline {
    agent any
    stages {
        // stage('Clone repository') {
        //     steps {
        //         checkout ([$class: 'GitSCM',
        //         branches: [[name: '*/main']],
        //         userRemoteConfigs: [[url: *https://github.com/Nikitamabel/PES2UG21CS263_Jenkins.git']]])
        
        //     }
        // }
        stage('Build') {
            steps {
                build 'PES2UG21CS263-1'
                sh 'g++x main.cpp -o output'
            }
        }
        stage( 'Test') {
            steps {
                sh './output'
            }
        }
        stage( 'Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}
