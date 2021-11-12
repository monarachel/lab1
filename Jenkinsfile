pipeline {

    agent any


    stages {
       stage ('Pull') {
            steps {
		script {
		checkout([$class: 'GitSCM', branches: [[name: '*/master']],
				userRemoteConfigs: [[
                    url: 'https://github.com/monarachel/lab1.git']]])
                   
            }
        }

       
        
       
      }  
      
      stage('Build'){
                 
                 steps {
                 		
                 	script{
                 	sh "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml -u root --private-key=/var/lib/jenkins/.ssh/id_rsa"
                 	
                 }
                 }
                 }
       
    }
   
  
    
}
