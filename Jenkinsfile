pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        dir(path: '/home/shiyanlou/Code') {
          git(url: 'git@github.com:lotus-dgas/shiyanlou_blue.git', branch: 'main', credentialsId: '69c3b4ef-bc23-4ad3-9d68-a43e0d5293b5')
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
        sh 'uwsgi --http :8001 --wsgi-file app.py --callable app --daemonize true '
      }
    }

  }
}