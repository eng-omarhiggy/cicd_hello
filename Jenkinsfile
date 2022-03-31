pipeline {
  agent {label 'agent'}
stages {
          stage('start') {
            steps {
              script {
              withCredentials([usernamePassword(credentialsId: 'dockerhub', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                sh """
                    docker login -u $DOKCER_LINK ${USERNAME} -p ${PASSWORD} --password-stdin
                    docker build -t $DOCKER_REPO:latest .
                    docker push $DOCKER_REPO:latest
                """
              }
              
            }
            }
          }
}
}
