pipeline {
    agent {
        node { 
            label 'ansible' 
        }
    }

    stages {
        stage('git_checkout') {
            steps {
                git 'https://github.com/nileshpatel111/Hello-Indore.git'
            }
        }
        stage('build_hello-world') {
            steps {
                sh 'mvn clean verify'
            }
        }
        
        stage('deploy_hello-world') {
            steps {
                sh 'ansible-playbook /etc/ansible/my_yaml/copyhelloworldwar.yaml'
            }
        }
    }
}
