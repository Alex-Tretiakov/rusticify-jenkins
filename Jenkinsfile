pipeline {
  agent any
  stages {
    stage('GetFile') {
      steps {
        echo 'Building'
        git(url: 'https://github.com/AlexTretiakov-wr/rusticify-jenkins', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        sh 'cd src'
        sh 'ls'
        sh 'cargo build --release'
      }
    }

  }
}