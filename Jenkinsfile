pipeline {
    agent any
    tools { 
        maven 'maven' 
        jdk 'jdk8' 
    }
    stages {
        
        }

        stage ('Clean') {
            steps {
                echo 'mvn clean '
            }
        }
         stage ('Build') {
            steps {
                echo 'mvn compile '
            }
        }

         stage ('Package') {
            steps {
                echo 'mvn package '
            }
        }
     

    }
}
