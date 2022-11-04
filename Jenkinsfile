pipeline {
  agent any
  stages {
      
    stage("Pull") {
      steps {
        script {
          checkout([$class: 'GitSCM',
            branches: [[name: '*/main' ]],
            userRemoteConfigs: [[
            url: 'https://github.com/anas1412/Myapp.git',
            credentialsId: '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'
            ]]
            ])
          }
        }
    }

    stage('Build'){
	    steps {
		    script{
			    sh "ansible-playbook -kK ansible/build.yml -i ansible/inventory/host.yml -e "ansible_become_password=vagrant""
		    }
	    }
    }
	    
    }
}
