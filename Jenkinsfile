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
                echo 'Testing....'
            }
        }
        stage('Input Test') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
            steps {
                echo "Hello, ${PERSON}, nice to meet you."
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