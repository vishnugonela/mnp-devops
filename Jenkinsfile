pipeline {
  agent any
  stages {
    stage('BuildStart') {
      steps {
        sh 'echo "Build Started"'
      }
    }

    stage('ImageBuilding') {
      steps {
        sh 'echo "FROM centos:7" > Dockerfile'
      }
    }

    stage('Deployment') {
      steps {
        sh 'echo "Creating Container"'
      }
    }

  }
}