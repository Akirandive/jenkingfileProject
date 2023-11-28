
pipeline{
   agent {
           label {
               label "built-in"
               customWorkspace "/mnt/jenkinfile"
           }
      
   }
   stages{
          stage("Clone Project")
          {
            steps{
                 sh "git clone https://github.com/Akirandive/jenkingfileProject.git "
            }
          }
          stage ("install httpd and service start")
          {
            steps{
                  sh "yum install httpd -y "
                  sh "service httpd start "
            }
          }

      
          stage ("Project Deployment")
          {
            steps{
               sh "cd /var/www/html "
               sh "rm -rf * "
               sh "cp /mnt/jenkingfileProject/index.html  /var/www/html"
                  
            }
          }


      

   }

}

