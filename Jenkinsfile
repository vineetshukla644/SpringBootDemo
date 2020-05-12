pipeline {

  agent any
 
  stages {
    stage('Clean Project') {
      steps {
            bat 'mvn  clean  compile'
      }
    }

    stage('Test Project') {
      steps {
            bat 'mvn test'
      }
    }

     stage('Package Project') {
     
      steps {
            bat 'mvn package' 
      }
    }
  
  }

  tools {
    maven 'maven'
  }
}