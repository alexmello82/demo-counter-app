pipeline {

    agent any
    
    stages{

        stage('Git Checkout'){

            steps{
                git branch: 'main', url: 'https://github.com/alexmello82/demo-counter-app.git'
            } 
        }
        stage('UNIT Testing'){

            steps{
                sh 'mvn test'
            }  
        }
        stage('Integration Tests'){

            steps{
                sh 'mvn verify -DskipUnitTests'
            } 
        }
    }
}
