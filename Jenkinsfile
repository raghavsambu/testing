pipeline{
     agent any
      
        stages{

              stage('Quality Gate Status Check'){
                  steps{
                      script{
			      withSonarQubeEnv('sonar-server') { 
			      sh "mvn clean package sonar:sonar"
                       	     	}
			      
		    	    //sh "mvn clean install"
		  
                 	}
               	 }  
              }	
		
            }	       	     	         
}
