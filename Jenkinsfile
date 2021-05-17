pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        dir(path: '/home/shiyanlou/Code') {
          git(url: 'git@github.com:lotus-dgas/shiyanlou_blue.git', branch: 'main', credentialsId: 'a6a38475-9a40-49a1-adae-aafda9b64615')
        }

      }
    }

    stage('build') {
      steps {
        sh '''pip2 install -r requirements.txt
'''
      }
    }

    stage('run') {
      steps {
        sh 'python app.py'
      }
    }

  }
}