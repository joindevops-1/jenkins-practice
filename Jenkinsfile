pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying.....'
            }
        }
    }

    post { 
        always { 
            echo 'I will Always Run!'
        }
        success{
            echo "I will only run if success"
        }
        failure{
            echo "I will only run if failure"
        }
    }
}