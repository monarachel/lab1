pipeline {

    agent any


    stages {
          
      stage('Build'){
                
                 steps {
                 		
                 	script{
                 	sh "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml -u root --private-key=/var/lib/jenkins/.ssh/id_rsa"
                 	
                 }
                 }
                 }
                 
                  
      
    }
  post {
        always {
            cleanWs()
        }
    }
    
}
