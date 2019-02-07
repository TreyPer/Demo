pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sleep 3
      }
    }
    stage('unit test') {
      parallel {
        stage('unit test') {
          steps {
            sleep 3
          }
        }
        stage('windows agent') {
          steps {
            echo 'windows test'
          }
        }
        stage('linux') {
          steps {
            echo 'linux test'
          }
        }
      }
    }
    stage('Approval Step') {
      steps {
        input(message: 'Do you approve', id: 'Yes', ok: 'Yes')
      }
    }
  }
}