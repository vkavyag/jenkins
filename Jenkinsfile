pipeline {
	agent none
 
	stages {
		stage ('make and maven') {
			parallel {
			agent { label 'C-node'}
			steps { 
				git 'https://github.com/vkavyag/c-project.git'
				sh 'make'
			}	
		}
		stage ('maven') {
			agent { label 'Java-node'}
			steps {
				git 'https://github.com/vkavyag/hello-world.git'
				sh 'mvn clean install'
			}	
		}
		/*stage ('STAGE 3') {
			steps {
				echo 'This is slaveforc with STAGE 3'
				sh 'sleep 10'
			}	
		}
		stage ('STAGE 4') {
			steps {
				echo 'This is master with STAGE 4'
				sh 'sleep 10'
			}	
		}*/
	}
}
