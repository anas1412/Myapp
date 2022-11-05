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
    
    stage ('docker'){
      steps{
        script{
          sh "ansible-playbook ansible/docker.yml  -i ansible/inventory/host.yml -e 'ansible_become_password=ansible'     "
        }
      }
    }
    
    
    
	    
  }
}
