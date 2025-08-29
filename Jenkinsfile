pipeline {
    agent { label 'linux' } // ensure this matches your Linux node label

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository (this Jenkinsfile)
                git branch: 'main', url: 'https://github.com/anuruddhapratap/jenkins.git'
            }
        }
        stage('Build') {
            steps {
                script {
                    // Simulated build: create a dummy build file
                    sh '''
                    echo "Building the project..."
                    echo "Build completed successfully." > build.log
                    '''
                }
            }
        }
        stage('Test') {
            steps {
                sh '''
                echo "Running tests..."
                echo "Tests passed." > test1.log
                '''
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                echo "Deploying application..."
                echo "Deployment successful." > deploy.log
                cat deploy.log
                '''
            }
        }
    }
}
