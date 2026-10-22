pipeline {
    agent any

    tools {
        maven 'Maven3' // Or 'Maven_3.9' depending on your Jenkins setup
        jdk 'JDK17'    // Keep your JDK configuration here
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }
    }
}
