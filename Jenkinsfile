pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-github-username/your-repo-name.git'
            }
        }
        stage('Upload to S3') {
            steps {
                withAWS(credentials: 'your-aws-credentials') {
                    sh 'aws s3 cp index.html s3://your-bucket-name/'
                    sh 'aws s3 cp style.css s3://your-bucket-name/'
                }
            }
        }
    }
}
