pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/yourusername/ansible-nginx-deployment.git'
            }
        }
        stage('Install Nginx') {
            steps {
                ansiblePlaybook installation: 'Ansible',
                                inventory: 'inventory',
                                playbook: 'nginx-playbook.yml',
                                disableHostKeyChecking: true
            }
        }
    }
}
