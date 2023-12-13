
node {

  
   def IMAGE="srv-web-luc"
	
    stage('Clone') {
          checkout scm
    }

    stage('Build') {
          docker.build("$IMAGE",  '.')
    }

    stage('Run image') {
        docker.image('srv-web-luc').withRun('--name srv_web-luc' ) { c ->

        sh 'docker ps | grep srv_web-luc'
	}

    }
}
