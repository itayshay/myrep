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
          }
        }

        stage('') {
          steps {
            sleep 10
          }
        }

      }
    }

  }
}