pipeline {
  agent any
  stages {
    stage('CHECKOUT') {
      steps {
        sh 'echo "stage1"'
      }
    }

    stage('BUILD') {
      steps {
        sh 'echo "stage2"'
      }
    }

    stage('TEST') {
      parallel {
        stage('FIREFOX') {
          steps {
            sh 'echo "stage3"'
            sh 'echo "stage6"'
            sh 'echo "stage6"'
          }
        }

        stage('EDGE') {
          steps {
            sh 'echo "stage7"'
          }
        }

      }
    }

    stage('STAGING') {
      steps {
        sh 'echo "stage4"'
      }
    }

    stage('PRODUCTION') {
      parallel {
        stage('PRODUCTION') {
          steps {
            sh 'echo "stage5"'
          }
        }

        stage('MANAGER') {
          steps {
            sh 'echo "stage manager"'
          }
        }

        stage('CLIENT') {
          steps {
            sh 'echo "stage client"'
          }
        }

      }
    }

    stage('HR') {
      steps {
        sh 'echo "stahe of hr"'
      }
    }

    stage('Worker Node1') {
      steps {
        sh 'echo "stage of worker"'
      }
    }

  }
}