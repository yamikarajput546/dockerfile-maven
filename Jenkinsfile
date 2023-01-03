pipeline {
    agent any
    tools { 
        maven 'maven' 
        jdk 'jdk8' 
    }

    environment {
        dockerhub =  credentials('dockerhub')
    }
    stages {

               
        stage ('Clean') {
            steps {
                echo 'mvn clean '
                sh 'mvn clean'
            }
        }
         stage ('Build') {
            steps {
                echo 'mvn compile '
                sh 'mvn compile'
            }
        }

         stage ('Package') {
            steps {
                echo 'mvn package '
                sh 'mvn package'
            }
        }

        stage ('Building docker image'){
            steps{
                sh 'docker build -t mvn:01 .'
            }
        }
        
        stage ('Pushing to the docker hub')
        {
            steps{
                sh 'docker tag mvn:01 yamikarajputd/mvn:01'
                sh 'echo $dockerhub_PSW | docker login -u $dockerhub_USR --password-stdin'
                sh 'docker push yamikarajputd/mvn:01'
            }
        }



    }
}
