pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "No build required for HTML site."
            }
        }

        stage('Test') {
            steps {
                echo "Testing not required for static HTML site."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment step..."
                bat "xcopy /E /I /Y index.html C:\\deploy-folder\\"
            }
        }
    }
}
