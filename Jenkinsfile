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

    stage('Build')
	    steps {
		    script{
			sh "ansible-playbook ansible/build.ym1 -i ansible/inventory/host.yml"
		    }
	    }
	    
    }
}
