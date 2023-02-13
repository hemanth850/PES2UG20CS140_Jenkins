pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ PES2UG20CS140-1.cpp -o PES2UG20CS140-1'
            }
        }
        stage('Test') {
            steps {
                sh './PES2UG20CS140-1'
            }
        }
        stage('Deploy') {
            stage {
                // Add your deployment steps here
            }
        }
    }

    post {
        always {
            script {
                if (currentBuild.result == "FAILURE") {
                    echo "Pipeline failed"
                }
            }
        }
    }
}
