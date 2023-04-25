pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo \'Building..\''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh 'echo \'Testing..\''
          }
        }

        stage('Test2') {
          steps {
            echo 'Second Testing'
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            sh 'echo \'Deploying..\''
          }
        }

        stage('Deploy2') {
          steps {
            echo 'Docker'
          }
        }

      }
    }

  }
}