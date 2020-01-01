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
        stage('stage-2') {
          steps {
            echo 'stage2'
            sleep 2
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