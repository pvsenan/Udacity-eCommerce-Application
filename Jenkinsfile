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
             steps { sh 'cp target/auth-course*.jar /tmp' }
        }
    }
}
