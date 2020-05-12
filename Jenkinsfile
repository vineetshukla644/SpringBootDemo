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

                       docker.build("springmicroservice")

                }
            }
        }
    
    stage('Run Docker Image') {
            steps {
                echo 'Starting to run docker image'

                sh 'docker run -it -d -p 6000:6000 springmicroservice'

                }
            }
        
  
  }

  tools {
    maven 'maven'
  }
}
