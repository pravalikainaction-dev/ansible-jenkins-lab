pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Specifying both the branch and the URL
                git branch: 'master', 
                    url: 'https://github.com/pravalikainaction-dev/ansible-jenkins-lab.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook -i hosts install_apache.yml'
            }
        }
    }
}
