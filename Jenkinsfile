pipeline { 
    agent any 
 
    tools { 
        maven 'Maven-3.9' 
        jdk 'JDK17' 
    } 
 
    stages { 
        stage('Checkout Git') { 
            steps { 
                checkout scm 
            } 
        } 
 
        stage('Build') { 
            steps { 
                bat 'mvn clean compile' 
            } 
        } 
 
        stage('Package') { 
            steps { 
                bat 'mvn package -DskipTests' 
            } 
        } 
    } 
 
    post { 
        success { 
            echo 'Pipeline CI reussie !' 
        } 
        failure { 
            echo 'Pipeline CI echouee.' 
        } 
    } 
} 
