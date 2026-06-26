pipeline {
  agent any
  triggers {
    githubPush()
  }
  stages {
    stage('Build') {
      steps {
        echo 'Triggered by GitHub push!'
      }
    }
  }
}
