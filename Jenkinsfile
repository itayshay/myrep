pipeline {
  agent any
  stages {
    stage('stage1-git_clone') {
      steps {
        sh '''echo "tesing blue ocean"
'''
      }
    }

    stage('stage-2') {
      parallel {
        stage('test') {
          steps {
            echo 'stage2'
            sleep 2
            junit 'target/**/*.xml'
          }
        }

        stage('sleep 10') {
          steps {
            sleep 10
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploying'
        build 'job_deploy'
      }
    }

  }
}