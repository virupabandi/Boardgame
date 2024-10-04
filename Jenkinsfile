pipeline {    
    agent any 
    tools {
        jdk 'jdk17'
        maven 'maven3'
    }

    stages {   
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn clean install'  // Add mvn clean install to the Build stage
            }
        }

        stage('Deploy') {  // Add Deploy stage
            steps {
                sh 'mvn deploy'  // Add mvn deploy command here
            }
        }
    }
}
