
pipeline { 
    agent any 
    tools { 
        maven 'Maven' // Ensure name matches configured Maven installation 
    } 
    stages { 
        stage('Checkout') {  
            steps { 
                git branch: 'master', url: 'https://github.com/Nehal6669/g2a.git'  
            } 
        } 
        stage('Build') {  
            steps { 
                bat 'mvn clean package'  
            } 
        } 
        stage('Test') {  
            steps { 
                bat 'mvn test'  
            } 
        } 
        stage('Run Application') {  
            steps { 
                bat 'java -jar target/g2a-0.0.1-SNAPSHOT.jar'  
            } 
        } 
    } 
}

