pipeline {
    agent any
    triggers {
        // Déclencheur pour démarrer le build dès qu'un push est détecté dans le référentiel Git
        pollSCM('* * * * *')
    }
    stages {
        stage('Récupération du code source') {
            steps {
                // Récupère le code source depuis le référentiel Git configuré dans le job Jenkins
                checkout scm
            }
        }
        stage('Afficher la date système') {
            steps {
                // Affiche la date et l'heure système actuelles
                script {
                    def date = new Date()
                    echo "La date et l'heure actuelles sont : ${date}"
                }
            }
        }
    }
}
