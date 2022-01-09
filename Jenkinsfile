pipeline {
    agent any
    stage('Cloning Git') {
        steps {
            git 'https://github.com/ormauda/turborepo.git'
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
