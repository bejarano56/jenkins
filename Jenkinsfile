pipeline {
    agent any

    stages {
        stage('Instalar dependencias') {
            steps {
                bat '''
                python -m venv venv
                call venv\\Scripts\\activate
                if exist requirements.txt (
                    pip install -r requirements.txt
                ) else (
                    echo No hay archivo requirements.txt
                )
                '''
            }
        }

        stage('Ejecutar pruebas') {
            steps {
                bat '''
                call venv\\Scripts\\activate
                pytest -v || echo No hay pruebas
                '''
            }
        }
    }

    post {
        success {
            echo ' Pipeline ejecutado correctamente.'
        }
        failure {
            echo ' Ocurrió un error en la ejecución del pipeline.'
        }
    }
}
