pipeline{
    agent any
tools {
        maven "M2_HOME"
    }
    stages{
        stage ('Clean Stage') {

            steps{
                sh """mvn clean"""
            }
        }
        stage('MVN COMPILE'){
                    steps{
                        sh """mvn compile"""
                    }
        }
        stage('MVN BUILD'){
                steps{
                    sh """mvn install"""
                }
        }
        stage ('Testing Stage'){
            steps {
                sh """mvn test"""
            }
        }
        stage ('Deployment Stage'){
            steps{
                sh """mvn deploy"""
            }
        }
    }
}
