pipeline {
  agent any
stages {
          stage('start') {
            steps {
              script {
              cleanWs()
                sh """
                    docker build -t omarhiggy/hello:lts .
                    docker run -d -p 80:80 omarhiggy/hello:lts
                """
              
            }
            }
          }
}
}