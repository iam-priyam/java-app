pipeline {
    agent any 
    
    tools{
        jdk 'jdk11'
        maven 'maven3'
    }
    
    stages {
        stage('Git Checkout') {
            steps {
                git 'https://github.com/iam-priyam/java-app.git'
            }
        }
        
        stage('Compile') {
            steps {
                sh "mvn compile"
            }
        }
        
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        
        stage('Package') {
            steps {
                sh "mvn package -DskipTests=true"
            }
        }
        
        stage('Install') {
            steps {
                sh "mvn install -DskipTests=true"
            }
        }
    }
}
