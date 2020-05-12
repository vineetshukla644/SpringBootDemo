pipeline {

  agent any
 
  stages {
    stage('Clean Project Now1') {
      steps {
           sh 'mvn  clean  compile'
      }
    }

    stage('Test Project') {
      steps {
            sh 'mvn test'
      }
    }

     stage('Package Project') {
     
      steps {
            sh 'mvn package' 
      }
    }
    
    
    stage('Build Docker Image') {
            steps {
                echo 'Starting to build docker image'

                script {

                       docker.build("springmicroservice:${env.BUILD_ID}")

                }
            }
        }
  
  }

  tools {
    maven 'maven'
  }
}
