pipeline {
  agent any
  stages {
    stage('stage1') {
      parallel {
        stage('parallel 01') {
          steps {
            sh 'echo "hello jenkins"'
            sh 'echo "hello stage1"'
            sh 'echo "hello"'
            sh 'echo "parallel1"'
          }
        }

        stage('parallel 02') {
          steps {
            sh 'echo "parallel stage"'
            sh 'echo "parallel2"'
          }
        }

        stage('parallel 03') {
          steps {
            sh 'for i in {1..10}; do echo "hello $i" && sleep 1; done'
            sh 'echo "paralllel3"'
          }
        }

      }
    }

    stage('stage2') {
      steps {
        sh 'echo "welcome blue-ocean"'
        sh 'echo "hello stage2"'
      }
    }

    stage('stage 3') {
      steps {
        sh 'echo "hello stage 3"'
      }
    }

  }
}