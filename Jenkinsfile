pipeline {
    agent {
        label 'agent'
    }
    stages {
        stage('Get from GItHub repository') {
            steps {
                git branch: 'main', credentialsId: 'git', url: 'git@github.com:mgesler/vector-role.git'
            }
         }
        stage('Install requirements') {
            steps {
                sh 'pip install -r tox-requirements.txt'
            }
        }
        stage('Run molecule test') {
            steps {
                sh 'molecule test -s compatibility'
            }
        }
        stage('Delete workspace') {
            steps {
              cleanWs()
            }
        }
    }
}
