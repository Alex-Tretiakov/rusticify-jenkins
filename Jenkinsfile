pipeline {
  agent any
  stages {
    stage('GetFile') {
      steps {
        echo 'Building'
        git(url: 'https://github.com/AlexTretiakov-wr/rusticify-jenkins', branch: 'main')
      }
    }

    stage('Test') {
      steps {
        sh 'cd src'
        sh 'ls'
        sh 'script: \'$HOME/.cargo/env cargo test main.rs\', returnStdout: true'
      }
    }

    stage('Build') {
      steps {
        sh '$HOME/.cargo/env cargo build --release main.rs'
      }
    }

  }
}