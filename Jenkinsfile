pipeline {
    agent any

    tools {
       
        maven 'Maven' 
        
        jdk 'JDK17'
    }

    stages {
        stage('Checkout') {
            steps {

            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

   
