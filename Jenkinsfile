pipeline {
    agent any

    stages {
        stage('Instalar dependencias') {
            steps {
                bat '''
                    python -m venv venv
                    call venv\\Scripts\\activate
                    if exist requirements.tpipeline {
    agent any

    stages {
        stage('Clonar repositorio') {
            steps {
                git 'https://github.com/<tu_usuario>/<tu_repo>.git'
            }
        }

        stage('Instalar dependencias') {
            steps {
                sh 'pip install pytest'
            }
        }

        stage('Ejecutar pruebas') {
            steps {
                sh 'pytest --maxfail=1 --disable-warnings -q'
            }
        }
    }

    post {
        success {
            echo ' Pipeline ejecutado correctamente.'
        }
        failure {
            echo ' Error durante el pipeline.'
        }
    }
}
xt (
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
                    python test_main.py
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline ejecutado correctamente.'
        }
        failure {
            echo 'Ocurrió un error en la ejecución del pipeline.'
        }
    }
}
