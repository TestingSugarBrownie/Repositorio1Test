pipeline {
    agent { label 'docker-agent' }

    stages {
        stage('Preparación') {
            steps {
                echo "Iniciando build en agente Docker dinámico..."
            }
        }

        stage('Información del agente') {
            steps {
                sh '''
                  echo "=== HOSTNAME ==="
                  hostname
                  echo "=== USUARIO ==="
                  whoami
                  echo "=== SISTEMA ==="
                  cat /etc/os-release || uname -a
                '''
            }
        }

        stage('Prueba de build') {
            steps {
                sh 'echo "Compilando proyecto de ejemplo 🚀"'
            }
        }
    }

    post {
        always {
            echo "Build finalizado. El contenedor del agente será destruido automáticamente."
        }
    }
}
