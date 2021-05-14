pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh 'sh "ls"'
        git(url: 'https://github.com/AlexTretiakov-wr/rusticify-jenkins', branch: 'main')
      }
    }

  }
}