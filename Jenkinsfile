pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo 'Código descargado desde GitHub'
                // El checkout se hace automáticamente
            }
        }
        
        stage('Build') {
            steps {
                echo 'Construyendo el proyecto...'
                // Aquí irían tus comandos de build
                sh 'echo "Build completado"'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Ejecutando tests...'
                // Aquí irían tus tests
                sh 'echo "Tests completados"'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Desplegando...'
                // Aquí iría tu deployment
                sh 'echo "Deploy completado"'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completado'
        }
        success {
            echo 'Pipeline exitoso!'
        }
        failure {
            echo 'Pipeline falló'
        }
    }
}
