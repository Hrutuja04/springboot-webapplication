pipeline {
  agent any
  stages {
    stage('checkout from git') {
      steps {
        echo 'this is git checkout'
        git(url: 'https://github.com/Hrutuja04/springboot-webapplication.git', branch: 'main', credentialsId: 'github-creds')
      }
    }

    stage('build from maven') {
      steps {
        tool 'maven-3.8.7'
        sh 'clean package'
      }
    }

  }
}