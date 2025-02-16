pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                git branch: 'master', credentialsId: 'pc-git-hub-token', url: 'https://github.com/pradeepch82/pc-ansible-app'
            }
        }
        
        stage('Install Apache') {
            steps {
    ansiblePlaybook credentialsId: 'p-ec2-ssh', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'apache.yml', vaultTmpPath: ''
    
    
                }
        }
        
    }
}
