pipeline {
  agent any
  stages {
    stage ('Upload to AWS') {
      steps {
        withAWS(credentials: 'aws-static', region: 'us-east-2') {
          s3Upload(file:'index.html', bucket:'jenkins-project3-aishwarya')
          sh 'echo "Hello World!"'
          sh '''
            echo "Multiline shell steps works too"
            ls -lah
          '''
        }
      }
    }
  }
}
