pipeline {
    agent any
    tools {
        maven 'M2_HOME'
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                
            }
        }
        stage('Build') {
            steps {
                echo 'Hello World'
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
       stage('Deloy') {
            steps {
                echo 'Hello World'
                
            }
        }
        stage('Test') {
            steps {
                echo 'Hello World'
                
            }
        }
    }
}


