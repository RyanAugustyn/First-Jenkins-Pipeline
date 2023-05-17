

pipeline {
  agent any
  
  stages{
    stage('Build') {
      steps{
        sh 'echo "Building the application..."'
      }
    }
    stage('Docker'){
      steps{
        withCredentials([usernamePassword(credentialsId: 'personal-dockerhub-credentials', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASWORD')]){
          sh "echo ${DOCKER_USERNAME}"
        }
      }
    }
  }
}
