pipeline {
    //agent any
    agent { node { label 'workstation' } }

    stages {
        stage('compile') {
            steps {
                echo 'Hello World'
                error 'This is an error'
            }
        }
    }

    post {
        always {
                echo 'Post'
                // send email
                // Trigger some another Job
                // Update some JIRA Staus about the build.
        }
    }