pipeline { 
    agent any  

    stages { 
	    stage('checkout-SCM') {
		  steps{ 
               	     git 'https://github.com/rajkumar2289/maven-archetype-webapp.git' 
            	 }
            }
	    stage('list scm')
	    {
		      steps{
		 	 sh 'ls -l'
		      }
	    }
		  
	    stage('Maven-Build') { 
		    steps{
			    sh  'mvn test'
		    }
		     
	    }

	    stage('build stage') { 
		    steps {
			    sh  'mvn clean package'
		    }
        }
    }
}
