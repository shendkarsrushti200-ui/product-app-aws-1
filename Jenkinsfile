pipeline {
    agent any

    environment {
        // Set Java home
        JAVA_HOME = "C:/jdk-21.0.9"
        // Add Java and Maven to PATH
        PATH = "${JAVA_HOME}/bin;C:/apache-maven-3.9.11/bin;${env.PATH}"
    }

    stages {
        stage('Check workspace') {
            steps {
                echo "Workspace: ${env.WORKSPACE}"
                bat 'dir'
            }
        }
 
        stage('Clean') {
            steps {
                bat 'mvnw.cmd clean install'
            }
        }

        stage('Compile') {
            steps {
                bat 'mvn compile'
            }
        }
 stage('Install') {
            steps {
                bat 'mvn install'
            }
       
        }
    }
}
