 pipeline {
    agent any
    tools {
        maven "local maven"
    }
     environment {

    PATH = "C:\\WINDOWS\\SYSTEM32"

}


    stages {
        stage('Checkout') {
            steps {
                // Get some code from a GitHub repository
                git url: 'https://github.com/richardvoma/jenkinsfolder.git', 
                    branch: 'main',
                    credentialsId: '2c97cb71-1aca-415b-851c-5a96840c8f52'
            }
        
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package' 
            }
        }
        stage('Test'){
            steps {
               bat 'mvn test'
            }
            post {
             always {
                  junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}    