pipeline { 
    agent any  
    stages { 
	    stage('checkout-SCM') {
		  steps{ 
               	     git 'https://github.com/vudumsekhar001/pipeline.git' 
            	 }
            }
	    stage('list scM')
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
	    stage('artifact-upaload') { 
		    steps{
			 nexusArtifactUploader artifacts: [
				 [
					 artifactId: 'simplewebapp',
					 classifier: '',
					 file: '/var/lib/jenkins/workspace/webapp-demo/target/simplewebapp.war',
					 type: 'war'
				 ]
			 ], 
				 credentialsId: 'NEXUS_CRED',
				 groupId: 'com.sekhar',
				 nexusUrl: '13.58.3.193:8081',
				 nexusVersion: 'nexus3',
				 protocol: 'http',
				 repository: 'Maven-repo',
				 version: '1.0'  
			    
		    }     
	    }
    }
}
