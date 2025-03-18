pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the CC lab 8...'
                sh 'make -C main'  // Runs the Makefile in main folder
            }
        }
        stage('Test') {
            steps {
                echo 'Running the compiled program...'
                sh './main/hello_exec' // Run the executable
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy step (PES1UG22CS454)'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed. Please check the errors.'
        }
    }
}
