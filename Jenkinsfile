pipeline {
  agent any
  stages {
    stage('Git') {
      steps {
        dir(path: '/tmp/syl') {
          git(url: 'git@github.com:lotus-dgas/shiyanlou_blue.git', branch: 'main', credentialsId: '9575a40a-f2fd-4ba3-b040-d0b3679c32ae')
        }

      }
    }

  }
}