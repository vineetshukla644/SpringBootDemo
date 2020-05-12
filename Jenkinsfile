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
  
  }

  tools {
    maven 'maven'
  }
}
