pipeline{
    agent any
        stages{
            stage('Git Checkout'){
                steps{
                    git branch: 'main', credentialsId: '043999ee-1e90-421a-abf0-2175b4166033', url: 'https://github.com/hanesh-92/anisble-playbook'
                }
            
            }
            stage('Ansible-playbook'){
                steps{
                    ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'anisble2', inventory: 'dev.inv', playbook: 'ansible.yml'
                }
            
            }
            
        }
}
