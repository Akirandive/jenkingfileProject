
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

   }

}

