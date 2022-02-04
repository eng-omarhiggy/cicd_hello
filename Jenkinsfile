pipeline {
  agent {lable 'agent'}
stages {
          stage('start') {
            steps {
              script {
                sh """
                    docker build -t omarhiggy/hello:lts .
                    docker run -d -p 80:80 omarhiggy/hello:lts
                """
              
            }
            }
          }
}
}
