pipeline {
  agent any
  stages {
    stage('stage1') {
      parallel {
        stage('stage1') {
          steps {
            sh 'echo "hello jenkins"'
            sh 'echo "hello stage1"'
          }
        }

        stage('parallel 02') {
          steps {
            sh 'echo "parallel stage"'
          }
        }

        stage('parallel 03') {
          steps {
            sh 'for i in {1..10}; do echo "hello $i" && sleep 1; done'
          }
        }

      }
    }

    stage('stage2') {
      steps {
        sh 'echo "welcome blue-ocean"'
      }
    }

    stage('stage 3') {
      steps {
        sh 'echo "hello stage 3"'
      }
    }

  }
}