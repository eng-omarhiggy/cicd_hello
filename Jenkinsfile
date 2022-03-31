pipeline {
  agent {label 'agent'}
stages {
          stage('start') {
            steps {
              script {
              withCredentials([usernamePassword(credentialsId: 'dockerhub', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                sh """
                    docker login $DOKCER_LINK -u ${USERNAME} -p ${PASSWORD} 
                    docker build -t $DOCKER_REPO:latest .
                    docker push $DOCKER_REPO:latest
                """
              }
              
            }
            }
          }
}
}
