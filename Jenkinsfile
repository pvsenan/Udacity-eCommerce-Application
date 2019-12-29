pipeline {
    agent any
    stages{
        stage ("Build"){
            steps { sh 'mvn clean compile'}
        }
        stage ('Testing Stage') {
            steps { sh 'mvn test' }
        }
        stage ('Deployment Stage') {
             steps { echo "mvn spring-boot:run" | at now + 1 minutes }
        }
    }
}
