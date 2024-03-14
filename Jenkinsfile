pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Étape pour récupérer le code depuis un référentiel Git
                git 'https://github.com/RyanPeyrot/alpinehelloworld.git'
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
