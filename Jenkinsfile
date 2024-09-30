pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Récupérer le code source du dépôt
                git branch: 'main', url: 'https://github.com/zahra2111/Devops.git'
            }
        }
        stage('Build') {
            steps {
                // Lancer Maven pour compiler et tester
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                // Exécuter les tests
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                // Par exemple, déployer sur un serveur (facultatif)
                sh 'mvn deploy'
            }
        }
    }
}
