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
             steps { sh 'nohup mvn spring-boot:run &' }
        }
    }
}
