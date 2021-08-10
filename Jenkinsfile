pipeline {
    agent any
    stages {
        stage('Build Application') {
            steps {
                def tool name: 'M2_HOME' type: 'maven'
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
