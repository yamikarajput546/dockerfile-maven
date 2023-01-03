node { // node/agent
  stage ('Clean') {
              echo 'mvn clean '
              sh 'mvn clean'
        }
    stage ('Build') {
              echo 'mvn clean '
              sh 'mvn clean'
        }

         stage ('Clean') {
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
            
                sh 'docker tag mvn:02 yamikarajputd/mvn:02'
                sh 'echo $dockerhub_PSW | docker login -u $dockerhub_USR --password-stdin'
                sh 'docker push yamikarajputd/mvn:02'
            }
        
}
