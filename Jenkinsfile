pipeline {
    
    agent any

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                // git 'https://github.com/jglick/simple-maven-project-with-tests.git'

                // Run Maven for packaging & skipping our application Tests 
                sh "mvn -DskipTests clean package"
            }
        }
        stage('Test') {
            steps {
                // Runing our application Tests 
                sh "mvn test"
            }
        }
    }
}
