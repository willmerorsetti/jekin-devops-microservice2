pipeline {
    agent any
    //agent {    docker { image "maven:3.6.3" } }
    //agent {    docker { image "node:13.8" } }
    stages{
        stage('Build') {
	    steps{
		//sh 'mvn --version'
		//sh 'node --version'
		//sh  'mvn -version'  
		withMaven(maven:'maven3.6.1')  {
        	    sh  'mvn -version'
                }    
	        echo "Build"  
	    }
	}
        stage('test') {
	    steps{
		echo "Test"
	    }
	}
        stage('Integration Test') {
	    steps{
		echo "Integration Test"
	    }
	}	    
    } 
	
    post {
          always {
	      echo "Im Awesome. I run always Test"  
	  }
          success {
	      echo "Solo corro si es exitoso"  
	  }	
          failure {
	      echo "Solo corro si Falla"  
	  }
	  //changed  {
	  //    echo "Se Cambio de estatus ..."  
	  //}
    }	
	    
}
