// Sintaxe Declarativa de Pipeline
pipeline {
    // 1. Onde o pipeline vai rodar? 'agent any' significa em qualquer agente Jenkins disponível.
    agent any
 
    // 2. 'stages' agrupa todas as etapas do nosso processo.
    stages {
        // 3. 'stage' define uma etapa específica, como "Build", "Test", etc.
        stage('Preparação') {
            steps {
                // 4. 'steps' contém as ações a serem executadas.
                echo 'Iniciando o processo... limpando o workspace.'
            }
        }
        stage('Build Simples') {
            steps {
                echo 'Aqui é onde você compilaria o código.'
                // Se estivesse no Windows, usaria: bat 'echo Compilando...'
                // Se estivesse no Linux/macOS, usaria: sh 'echo Compilando...'
            }
        }
 
        stage('Testes Simples') {
            steps {
                echo 'Aqui é onde você executaria os testes unitários.'
                // Exemplo: sh './run-tests.sh'
            }
        }
    }
    // 5. 'post' define ações que acontecem no final do pipeline.
    post {
        always {
            echo 'Pipeline finalizado.'
        }
        success {
            echo 'O pipeline foi um sucesso!'
        }
        failure {
            echo 'O pipeline falhou.'
        }
    }
}