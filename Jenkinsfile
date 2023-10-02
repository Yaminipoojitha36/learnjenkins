pipeline {
    //agent any
    agent { node {label 'workstation' } }

    stages {
        stage('compile') {
            steps {
                echo 'Hello World'
                error 'This is an error'
            }
        }

    }
}