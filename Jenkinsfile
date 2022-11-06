pipeline {
  agent any
  stages{

    stage('Build'){
	    steps {
		    script{
			    sh "ansible-playbook -kK ansible/build.yml -i ansible/inventory/host.yml"
		    }
	    }
    }
    
    stage ('test docker'){
      steps{
        script{
          sh "docker run hello-world"
        }
      }
    }
    
    stage ('docker'){
      steps{
        script{
          sh "ansible-playbook -kK ansible/docker.yml  -i ansible/inventory/host.yml"
        }
      }
    }
    
    
    
	    
  }
}
