pipeline{
    agent any 
    tools{
        maven "M2_HOME"
    }
    stages{
        stage('maven clean') {
            steps{
                sh 'mvn clean'
            }
        }
     stage('maven install'){
        steps{
            sh 'mvn install'
        }
     }
    

stage('maven package'){
        steps{
            sh 'mvn package'
        }
     }

     stage('upload artifact'){
         steps{ 
            sh 'nexusArtifactUploader artifacts: [[artifactId: 'bioMedical', classifier: '', file: 'target/bioMedical-0.0.2-SNAPSHOT.jar', type: 'jar']], credentialsId: '16de3bf1-4857-4e15-ba96-1d5db31c7902', groupId: 'qa', nexusUrl: '198.58.119.40:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'meganrepo', version: '002'

         }
     }
    

     }
    }

