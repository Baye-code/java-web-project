pipeline {

    agent any

    stages {
        stage('Build') {
            steps {
                // Run Maven for packaging & skipping our application Tests 
                sh "mvn clean package"
            }
        }
        stage('Deploy') {
            steps {
                // Run Maven for packaging & skipping our application Tests 
                deploy adapters: [tomcat7(credentialsId: 'abce4bf8-8d4f-4392-b44c-c3f67e85e8f7', 
                path: '', 
                url: 'http://52.14.175.43:8080/')], 
                contextPath: 'javawebapp', 
                war: '**/java-web-project.war'
            }
        } 
    }
}
