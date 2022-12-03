pipeline{
  agent any  
  stages{  
      stage("Run an ansible playbook"){
        steps{
          ansiblePlaybook credentialsId: 'SSH-KEY', inventory: 'hosts', playbook: 'nginx_install.yaml'
          //ansiblePlaybook become: true, disableHostKeyChecking: true, inventory: 'hosts', playbook: 'nginx_install.yaml', vaultCredentialsId: 'SSH-KEY'
        }
      }
      stage("Print Nginx Installed"){
        steps{
           sh"echo nginx installed on all servers"
        }
      }
  }
}
