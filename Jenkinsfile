pipeline {
    agent any

    tools {
        maven 'Maven' 
        jdk 'JDK17'
    }

    stages {
        stage('Checkout') {
            steps {
                // Assuming the Jenkins job is setup to checkout the SCM,
                // this will checkout the code for the branch that triggered the build
                checkout scm
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
    }

    post {
        success {
            echo 'Build succeeded.'
        }
        failure {
            echo 'Build failed.'
        }
        always {
            echo 'Pipeline completed.'
        }
    }
}
