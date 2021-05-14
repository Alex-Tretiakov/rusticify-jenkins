pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        pwd(tmp: true)
        sh 'sh "cargo test main.rs"'
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