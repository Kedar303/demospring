pipeline {
  agent any
  
  tools{
    maven 'MAVEN_HOME'
  }
  stages {
    stage('Checkout') {
      steps {
        checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'e2c4f372-b35a-4a0c-bdcf-855c2c203419', url: 'https://github.com/Kedar303/demospring.git']])
        sh 'CHECKOUT COMPLETED'
      }
    }
    
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
   
}
}
    
