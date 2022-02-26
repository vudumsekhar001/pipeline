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
           stage('clean stage') { 
		    steps {
			    sh  'mvn clean package'
		    }
        }		  
	    stage('test stage') { 
		    steps{
			    sh  'mvn test'
		    }
		     
	    }

	    stage('build stage') { 
		    steps {
			    sh  'mvn package'
		    }
        }
	    stage('install stage') { 
		    steps {
			    sh  'mvn install'
		    }
        }
    }
}
