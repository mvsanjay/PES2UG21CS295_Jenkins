pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using a shell script
                    build 'PES2UG21CS295- 1'
                    sh 'g++ main.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Print output of the .cpp file using a shell script
                    sh './output'
                }
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps here
                    echo 'deploy'
            }
        }
    }

    post {
        failure{
            error 'Pipeline failed'
        }
    }
}
