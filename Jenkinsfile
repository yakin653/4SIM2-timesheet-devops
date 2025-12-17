pipeline { 
    agent any 
 
    stages { 
        stage('Checkout') { 
            steps { 
                checkout scm 
            } 
        } 
 
        stage('Build') { 
            steps { 
                bat "C:\maven\apache-maven-3.9.9\bin\mvn clean compile" 
            } 
        } 
 
        stage('Package') { 
            steps { 
                bat "C:\maven\apache-maven-3.9.9\bin\mvn package -DskipTests" 
            } 
        } 
    } 
} 
