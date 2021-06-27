pipeline {
    agent any
    stages {
        stage('hello AWS') {
            steps {
                withAWS(credentials: 'aws-personal', region: 'eu-west-2') {
                    sh 'echo "hello KB">hello.txt'
                    s3Upload acl: 'Private', bucket: 'britcat.com', file: 'hello.txt'
                    
                }
            }
        }
    }
}
