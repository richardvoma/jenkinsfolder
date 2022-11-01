pipeline {
    agent any
    tools {
        maven "local maven"
    }
    stages {
        stage('Checkout') {
            steps {
                // Get some code from a GitHub repository
                git url: 'https://github.com/richardvoma/jenkinsfolder.git', 
                    branch: 'main',
                    credentialsId: '2c97cb71-1aca-415b-851c-5a96840c8f52'
            }
        }
    }
}
