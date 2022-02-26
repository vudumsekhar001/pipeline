pipeline { 
    agent any  
    stages { 
	    stage('checkout-SCM') {
		  steps{ 
               	     git 'https://github.com/vudumsekhar001/pipeline.git' 
            	 }
            }
	    stage('list scm')
	    {
		      steps{
		 	 sh 'ls -l'
		      }
	    }
           stage('build stage') { 
		    steps {
			    sh  'mvn clean package'
		    }
        }		  
	    stage('Maven-Build') { 
		    steps{
			    sh  'mvn test'
		    }
		     
	    }

	    stage('build stage') { 
		    steps {
			    sh  'mvn package'
		    }
        }
	    stage('build stage') { 
		    steps {
			    sh  'mvn install'
		    }
        }
    }
}
