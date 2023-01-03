node { // node/agent
  stage ('Clean') {
              echo 'mvn clean '
              sh 'mvn clean'
        }
    stage ('Build') {
              echo 'mvn clean '
              sh 'mvn clean'
        }

         stage ('Compile') {
              echo 'mvn compile '
              sh 'mvn compile'
        }
          stage ('Package') {
              echo 'mvn package '
              sh 'mvn package'
        }


        stage ('Building docker image'){
            
                sh 'docker build -t mvn:02 .'
            
        }
        
        stage ('Pushing to the docker hub')
        {
            try {
                sh 'docker tag mvn:02 yamikarajputd/mvn:02'
                sh 'docker push yamikarajputd/mvn:02'
                }
           catch (exc) {
            echo 'Something failed, I should sound the klaxons!'
            
        }
            

      }
        
}
