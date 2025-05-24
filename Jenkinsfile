pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/d2arshan/PRTDevOps.git'
            }
        }

        stage('Run Ansible Playbook') {
            agent { label 'master' } // This runs the step on the Jenkins master node
            steps {
                sh '''
                    ansible-playbook playbook.yaml -i /etc/ansible/hosts
                '''
            }
        }
    }
}
