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
        sh '$HOME/.rustup/env rust main.rs'
      }
    }

    stage('Build') {
      steps {
        sh '$HOME/.cargo/env cargo build --release main.rs'
      }
    }

  }
}