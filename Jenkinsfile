pipeline {
  agent any

  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/yourusername/devops-cicd.git'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t yourname/devops-cicd:latest .'
      }
    }

    stage('Push Image') {
      steps {
        sh 'docker push melaxa75722/-ci-cd:latest'
      }
    }

    stage('Deploy to Kubernetes') {
      steps {
        sh 'kubectl apply -f deployment.yaml'
        sh 'kubectl apply -f service.yaml'
      }
    }
  }
}

