pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      parallel {
        stage('Checkout Code') {
          steps {
            git(url: 'https://github.com/iamahmudul/fcc-jenkins-curriculum-app', branch: 'dev')
          }
        }

        stage('Parallel to Checkout Code') {
          steps {
            echo 'This step is running in parallel to Checkout Code'
          }
        }

      }
    }

    stage('Log') {
      steps {
        sh 'ls -la'
      }
    }

  }
}