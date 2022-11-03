pipeline {
    agent any
    stages {
        stage("Build the maven project") {
            agent {
                docker {
                    image 'maven'
                    args '-v $HOME/.m2:/root/.m2'
                }
            }
            steps {
                script {
                    sh 'mvn clean package'
                }
            }
        }
            
        }
    }
