pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        dir(path: '/home/shiyanlou/Code') {
          git(url: 'git@github.com:lotus-dgas/shiyanlou_blue.git', branch: 'main', credentialsId: '	b35067a1-3ef5-47da-b256-9cd7d0979e95')
        }

      }
    }

    stage('build') {
      steps {
        sh '''pip3 install -r requirements.txt
'''
      }
    }

    stage('run') {
      steps {
        sh 'python3 app.py'
      }
    }

  }
}