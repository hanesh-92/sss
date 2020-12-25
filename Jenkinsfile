pipeline{
    agent any
        stages{
            stage('Git Checkout'){
                steps{
                    git branch: 'main', url: 'https://github.com/hanesh-92/sss'
                }
            
            }
            stage('Ansible-playbook'){
                steps{
                    ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'anisble2', inventory: 'dev.inv', playbook: 'ansible.yml'
                }
            
            }
            
        }
}
