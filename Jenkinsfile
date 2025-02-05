pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/SupersaiyanGoku97/-gokul-static-site.git'
            }
        }
        stage('Upload to S3') {
            steps {
                withAWS(credentials: 'aws credential id') {
                    sh 'aws s3 cp index.html s3://gokul-static-site/'
                    sh 'aws s3 cp style.css s3://gokul-static-site/'
                }
            }
        }
    }
}
