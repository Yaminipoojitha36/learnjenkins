pipeline {
    //agent any
    agent { node { label 'workstation' } }

    environment {
        TEST_URL ="google.com"
        SSH = credentials("centos-ssh")
    }

    options {
        ansiColor('xterm')
    }

    stages {
        stage('compile') {
            steps {
                //echo 'Hello World'
                //error 'This is an error'
                echo TEST_URL
                echo SSH
                sh 'env'
                sh 'ansible -i 52.90.42.229,all -e ansible-user=${SSH_USR} -e ansible_password=${SSH_PSW} -m ping'
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