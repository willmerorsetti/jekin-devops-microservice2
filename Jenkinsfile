pipeline {
    agent any
    stages{
        stage('Build') {
	    steps{
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
	  changed  {
	      echo "Se Cambio de estatus ..."  
	  }
    }	
	    
}
