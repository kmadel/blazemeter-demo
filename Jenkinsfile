pipeline {
  agent any
  stages {
    stage('Run App') {
      steps {
        sh 'make app'
      }
    }
    stage('Run Perf') {
      steps {
        sh 'make bzt'
      }
    }
  }
  post {
    always {
      sh 'make clean'
    }
  }
}
