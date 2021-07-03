pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        dir(path: '/var/jenkins_home/workspace') {
          git(url: 'git@github.com:lotus-dgas/shiyanlou_blue.git', branch: 'main', credentialsId: '9575a40a-f2fd-4ba3-b040-d0b3679c32ae')
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