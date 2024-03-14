pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Étape pour récupérer le code depuis un référentiel Git
                git 'https://github.com/votre-utilisateur/votre-projet.git'
            }
        }
        stage('Build') {
            steps {
                // Étape de construction du projet
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                // Étape pour exécuter les tests
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                // Étape de déploiement (exemple: copier les fichiers générés vers un serveur)
                sh 'scp target/*.jar utilisateur@serveur:/chemin/vers/depot'
            }
        }
    }
    
    post {
        success {
            // Actions à effectuer si la pipeline réussit
            echo 'La pipeline a réussi! Déploiement effectué avec succès.'
        }
        failure {
            // Actions à effectuer si la pipeline échoue
            echo 'La pipeline a échoué! Veuillez vérifier les logs pour plus de détails.'
        }
    }
}
