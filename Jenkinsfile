pipeline { 
    agent any  
	tools {
        jdk 'jdk'
        git 'git'
        maven 'maven'
        terraform 'terraform'
    }
    stages { 
	    stage('checkout-SCM') {
		  steps{ 
               	     git 'https://github.com/rajkumar2289/maven-archetype-webapp.git' 
            	 }
            }
	    stage('list scm files')
	    {
		      steps{
		 	 sh 'ls -l'
		      }
	    }
		  
	    stage('Maven-Build') { 
		    steps{
			     mvn test
		    }
		     
	    }

	    stage('build stage') { 
		    steps {
			     mvn clean package
		    }
        }
    }
}
