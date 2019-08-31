pipeline {
    agent any
    stages {
        stage('Lint HTML') {
            steps {
                tidy -q -e *.html
                
            }
        }
         stage('Upload to AWS') {
            steps {
                s3Upload(file:'index.html', bucket:'bucket4jenkinsdemoproject')
                
            }
        }
    }
}