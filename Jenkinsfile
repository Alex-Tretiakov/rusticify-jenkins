pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        pwd(tmp: true)
        sh 'sh "cargo"'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
      }
    }

  }
}