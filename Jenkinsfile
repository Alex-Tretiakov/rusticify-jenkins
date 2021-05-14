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
        sh '$HOME/.cargo/env  script: \'cargo test main.rs\', returnStdout: true'
      }
    }

    stage('Build') {
      steps {
        sh '$HOME/.cargo/env cargo build --release main.rs'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts(defaultExcludes: true, artifacts: '**/*.rs', onlyIfSuccessful: true, allowEmptyArchive: true)
      }
    }

  }
}