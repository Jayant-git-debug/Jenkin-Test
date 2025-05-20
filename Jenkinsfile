pipeline {
  agent any

  tools {
    maven 'Maven-3.9.8'
    jdk 'Java-17'
  }
  
  environment {
    BUILD_FILE = "sampleApp"
    ROLE = "Developer"
    NAME = "Jayant"
  }

  stages {
    stage('Initialize the App'){
      steps {
        sh '''
          echo "PATH = $PATH"
          echo "M2_HOME" = "$M2_HOME"
          mvn --version
        '''
      }
    }
    stage('Compile and Build the App'){
      steps {
        sh 'mvn compile'        
      }
    }
    stage('Build the Application'){
      steps {
        sh 'mvn clean package'
      }
    }     
  }
}
