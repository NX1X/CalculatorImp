pipeline {
    agent any

    tools {
        // 'Maven' or 'M3' refers to the label given to the Maven installation on Jenkins.
        // This label is configured in the Global Tool Configuration.
        maven 'Maven' 
        // Make sure JDK is configured properly in Jenkins with the label 'JDK11'
        jdk 'JDK11'
    }

    stages {
        stage('Checkout') {
            steps {
                // This step checks out the SCM code into the workspace
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // This step will invoke 'mvn clean install' command.
                // 'clean install' will compile the code and package it into a JAR/WAR/EAR
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // This step will invoke 'mvn test' command to run tests
                // Assuming tests are configured in your pom.xml
                sh 'mvn test'
            }
        }

        // Add more stages if needed (e.g., for deployment or further
