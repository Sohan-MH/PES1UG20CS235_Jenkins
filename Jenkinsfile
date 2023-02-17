pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'make -C main'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh '/var/jenkins_home/workspace/PES1UG20CS235-1/main/working_exec'
                sh '/var/jenkins_home/workspace/PES1UG20CS235-1/main/hello_exec'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echoes 'Deployed Sucessfully'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
