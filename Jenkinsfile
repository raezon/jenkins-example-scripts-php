pipeline {
  agent any
  stages {
    stage('verify version') {
      steps {
        sh 'php --version'
      }
    }
    stage('hello') {
      steps {
        sh 'php index.php'
      }
      post {
        success {
          archiveArtifacts artifacts: 'index.php', allowEmptyArchive: true
        }
      }
    }
    
  }
  
}
