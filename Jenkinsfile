pipeline {
  agent any
  stages {
    stage('init') {
      steps {
        sh 'echo "Hello World!"'
      }
    }

    stage('Static-Code Analysis') {
      steps {
        echo 'Static-Code Analysis'
      }
    }

    stage('Build Web App') {
      steps {
        echo 'Build Web App'
      }
    }

    stage('Deploy to Test') {
      parallel {
        stage('Deploy to Test') {
          steps {
            echo 'Deploy to Test'
          }
        }

        stage('Store Artifacts') {
          steps {
            echo 'Store Artifacts'
          }
        }

      }
    }

    stage('UI Test') {
      parallel {
        stage('UI Test') {
          steps {
            echo 'UI Test'
          }
        }

        stage('Performance Test') {
          steps {
            echo 'Performance Test'
          }
        }

      }
    }

    stage('Deploy to Prod') {
      steps {
        echo 'Deploy to Prod'
      }
    }

    stage('Sanity Test') {
      steps {
        echo 'Sanity Test'
      }
    }

  }
}