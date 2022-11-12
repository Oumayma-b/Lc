pipeline { 
     agent any
     stages{
       stage('Pulling GIT') {
             steps {
		script {
                  git 'https://github.com/Oumayma-b/Livraison.git'
            }
        }        
     }
      
        
          stage('Build') 
        { 
        steps{ 
             script{
                   
              sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml"

             }
          }
        }
        
         stage('Docker') 
        { 
        steps{ 
             script{
                   
              sh "ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml"

             }
          } 
        }
        
        }
        
        }
        
        
