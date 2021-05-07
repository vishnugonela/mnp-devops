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
        sh '''echo "FROM centos:7" > Dockerfile
echo "RUN yum install httpd -y" >> Dockerfile

docker build -t pipelineimg .'''
      }
    }

    stage('Deployment') {
      steps {
        sh '''echo "Creating Container"

docker run -d -p 9000:80 pipelineimg'''
      }
    }

  }
}