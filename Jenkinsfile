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
      parallel {
        stage('Log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End Unit Test') {
          steps {
            sh 'cd curriculum-front && rm -rf node_modules && rm -rf package-lock.json && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}