pipeline {
    agent any
    stages {
        stage('Build Application') {
            steps {
                sh 'mvn clean install package'
            }
            post {
                success {
                    echo "Now Archiving the Artifacts...."
                    archiveArtifacts artifacts: '**/*.war'
                }
            }
        }


      }
   }
