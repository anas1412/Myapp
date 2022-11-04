pipeline {
  agent any
  stages{

    stage('Build'){
	    steps {
		    script{
			    sh "ansible-playbook -kK ansible/build.yml -i ansible/inventory/host.yml  --user=root \
                              --extra-vars 'ansible_sudo_pass=vagrant'"
		    }
	    }
    }
	    
    }
}
