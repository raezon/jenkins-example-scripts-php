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
        sh 'php hello.php'
      }
      post {
        success {
          archiveArtifacts artifacts: 'hello.php', allowEmptyArchive: true
        }
      }
    }
  }
}
