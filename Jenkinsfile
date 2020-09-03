pipeline {
    agent any
    tools {
        maven 'M2_HOME'
    }

    stages {
        
        stage('Build') {
            steps {
                echo 'Hello World'
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
       stage('Test') {
            steps {
                sh 'mvn test'
                
            }
        }
        stage ('create and push docker image') {
            steps {
              script {
                 checkout scm
                 docker.withRegistry('', 'DockerID') {
                 def customImage = docker.build("smutoni2/holy-pipe:${env.BUILD_ID}")
                 customImage.push()
                 }
         }
        
         }               
                
 }
         }
 }



