pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh 'sh "https://github.com/AlexTretiakov-wr/rusticify-jenkins/tree/main/src"'
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