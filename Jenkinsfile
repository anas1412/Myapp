pipeline {
  agent any
  stages {

    stage("Build") {
      steps {
        script{
          sh "ansible-playbook -K ansible/build.yml -i ansible/inventory/host.yml"
              }
            }
        }
   stage("docker") {
            steps {
                script{
                    sh 'ansible-playbook -K ansible/docker.yml -i ansible/inventory/host.yml'
                }
            }
        }
    stage("docker-registry") {
            steps {
                script{
                    sh 'ansible-playbook -K ansible/docker-registry.yml -i ansible/inventory/host.yml'
                }
            }
        } 

//stage("Grafana") {
            //steps {
                //script{
                    //sh 'ansible-playbook -K ansible/grafana.yml -i ansible/inventory/host.yml'
                //}
            //}
        //}
    stage("Grafana") {
            steps {
                script{
                    sh 'docker-compose up -d'
                }
            }
        } 


  }
}
