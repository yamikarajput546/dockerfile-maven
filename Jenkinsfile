pipeline {
    agent any
    tools { 
        maven 'maven' 
        jdk 'jdk8' 
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
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
