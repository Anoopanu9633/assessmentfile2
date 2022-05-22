pipeline
{
    agent any
    stages 
    {
        stage('git repo & clean') 
        {
            steps
            {
              // bat "rmdir  /s /q assesmentfile2"
               bat "git clone https://github.com/Anoopanu9633/assesmentfile2.git"
                bat "mvn clean -f assesmentfile2"
            }
        }
       
        stage('package')
        {
            steps 
            {
                bat "mvn package -f assesmentfile2"
            }
        }
      
        
        
        
       stage('Building docker image')
        {
           steps
            {
             //  bat 'docker build -t anoop9633/spring-boot-docker .'
               bat 'docker pull anoop9633/gs-spring-boot-docker'  
            }
        }
    
        
        
        
         stage('Pushing docker image')
        {
            steps
            {
                bat "docker login -u anoop9633 -p Preetha123"   
                bat 'docker push anoop9633/gs-spring-boot-docker'
            }
        }
        
    }
    
    
}
