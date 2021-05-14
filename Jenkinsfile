pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh 'cargo build --release'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
        sh 'cargo test'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
        sh 'Jenkins/deploy.sh'
      }
    }

  }
}