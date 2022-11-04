pipeline {
  agent any
  stages{

    stage('Build'){
	    steps {
		    script{
			    sh "sudo ansible-playbook -kK ansible/build.yml -i ansible/inventory/host.yml"
		    }
	    }
    }
	    
    }
}
