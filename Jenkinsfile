pipeline {
    agent any
    stages{
        stage ("Build"){
            steps { sh 'mvn clean compile'}
        }
        stage ("Package"){
             steps { sh 'mvn package'}
        }
        stage ('Testing Stage') {
            steps { sh 'mvn test' }
        }
        stage ("Copy"){
             steps { sh 'cp target/auth-course-0.0.1-SNAPSHOT.jar /tmp'}
        }
    }
}
