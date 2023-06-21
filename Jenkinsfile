pipeline{
     agent any
      
        stages{

              stage('Quality Gate Status Check'){
                  steps{
                      script{
			      withSonarQubeEnv('sonar-server') { 
			      sh "mvn clean sonar:sonar -Dsonar.projectKey= Demo"
                       	     	}
			      
		    	    sh "mvn clean install"
		  
                 	}
               	 }  
              }	
		
            }	       	     	         
}
