pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Compiling hello.cpp...'
                sh 'g++ hello.cpp -o output'
                sh 'echo "build PES2UG22CS671-1"'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running the compiled program...'
                sh './output'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploy stage completed.'
            }
        }
    }
    
    post {
        failure {
            error 'pipeline failed'
        }
    }
}
