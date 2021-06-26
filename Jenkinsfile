pipeline {
  agent any
  stages {
    stage('CodeCollection') {
      steps {
        git(url: 'https://github.com/pavansvplearning/simpleMavenJunit', branch: 'master', changelog: true, poll: true)
      }
    }

    stage('Compile') {
      steps {
        sh 'mvn clean compile '
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test '
      }
    }

    stage('Package') {
      steps {
        sh 'mvn package'
      }
    }

  }
}