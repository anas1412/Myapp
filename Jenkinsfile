pipeline {
  agent any
  stages{

    stage('Build'){
	    steps {
		    script{
			    sh "ansible-playbook -kK ansible/build.yml -i ansible/inventory/host.yml -e ansible_become_password=vagrant"
		    }
	    }
    }
	    
    }
}
