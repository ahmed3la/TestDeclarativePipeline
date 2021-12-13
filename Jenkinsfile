pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Built Completed'
      }
    }

    stage('Test stages') {
      parallel {
        stage('Test2') {
          steps {
            echo 'Running Test2'
          }
        }

        stage('Test1') {
          steps {
            echo 'Running Test1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployment Completed'
      }
    }

  }
}