pipeline {
    agent any

    stages {
        stage('Pull Code') {
            steps {
                echo "Pulling latest code from GitHub..."
                git branch: 'main',
                    url: 'https://github.com/Aimen12782/myjenkinrepo.git',
                    credentialsId: 'YOUR_GITHUB_CREDENTIALS_ID'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying website to Nginx..."
                
                // Copy all files to Nginx root folder
                sh '''
                sudo cp -r * /var/www/html/
                sudo chown -R www-data:www-data /var/www/html/
                sudo systemctl reload nginx
                '''
            }
        }
    }
}
