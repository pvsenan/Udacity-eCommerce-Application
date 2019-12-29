pipeline {
    agent any
    stages{
        stage ("Build"){
            steps { sh 'mvn clean compile'}
        }
        stage ("Build"){
             steps { sh 'mvn package'}
        }
        stage ('Testing Stage') {
            steps { sh 'mvn test' }
        }
        stage ("Copy"){
             steps { sh 'cp *-SNAPSHOT.jar /tmp'}
          }
        stage ('Archive artifacts') {
             steps { archiveArtifacts artifacts: 'dist/ecom_api.zip' }
        }
    }
}
