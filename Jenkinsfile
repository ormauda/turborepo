pipeline {
    agent any

    tools { nodejs "node" }

    stages {
        stage('Cloning Git') {
            steps {
                git branch: 'main', url: 'https://github.com/ormauda/turborepo.git'
            }
        }
        stage('Install') {
            steps {
                script {
                    sh 'npm i -g pnpm'
                }
                script {
                    sh 'pnpm install'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'pnpm build'
                }
            }
        }
    }
}
