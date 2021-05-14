pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh 'Jenkins/build.sh'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
        sh 'Jenkins/test-all.sh'
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