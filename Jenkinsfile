pipeline{
     agent any
      
        stages{

              stage('Quality Gate Status Check'){
                  steps{
                      script{
			      withSonarQubeEnv('sonar-server') { 
			      sh "mvn clean sonar:sonar" -Dsonar.projectKey=develop -Dsonar.sources=. "
                       	     	}
			      
		    	    sh "mvn clean install"
		  
                 	}
               	 }  
              }	
		
            }	       	     	         
}
