pipeline {
    agent any
    
     tools {
        maven "M2_HOME"
    }
    stages {
        stage('Build Application') {
            steps {
                
                sh 'mvn clean package'
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
