pipeline {

	agent { label 'linux-slave' }

	stages {
	  stage('build') {
		steps {
		  sh 'mvn install -DskipTests'
		}
	  }

	  stage('test') {
		  steps {
				sh 'echo new'
			}
		 post {
			 always{
				archiveArtifacts artifacts: 'target/**.jar', followSymlinks: false
			
			 }
			}
	  }
		
}

}
