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
        input(message: 'Are you sure to deploy?', ok: 'Yes, I am sure')
        echo 'Deployment Completed'
      }
    }

    stage('Notify for a new build') {
      steps {
        echo 'New build completed successfully'
      }
    }

  }
}