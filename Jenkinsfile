pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Compiling hello.cpp...part 2(mohith)'
                sh 'g++ -Wall hello.cpp -o output || exit 1'
                sh 'echo "build PES2UG22CS671-1"'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running the compiled program...'
                sh '[ -f output ] && ./output || exit 1'
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
            echo 'Pipeline failed'
        }
    }
}
