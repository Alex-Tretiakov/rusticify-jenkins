pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        pwd(tmp: true)
        sh 'sh "rustic --version"'
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