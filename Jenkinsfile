pipeline{
     agent any
      
        stages{

              stage('Quality Gate Status Check'){
                  steps{
                      script{
			      withSonarQubeEnv('sonar-server') { 
			      sh "mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=testing218_analysis"
                       	     	}
			      
		    	    //sh "mvn clean install"
		  
                 	}
               	 }  
              }	
		
            }	       	     	         
}
