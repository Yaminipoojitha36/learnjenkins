pipeline {
    //agent any
    agent { node {label 'workstation' } }

    environment {
    TEST_URL = "google.com"
    }

    stages {
        stage('compile') {
            steps {
                echo 'Hello World'
                error 'This is an error'
                echo TEST_URL
            }
        }

    }

    post {
        always {
                echo 'Post'
                //send email
                //Trigger Some another Job
                //Update some JIRA Status about the build
    }
    }
}