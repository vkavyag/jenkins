pipeline {
	 agent none
 
	stages {
		stage ('make and maven') {
			parallel {
				stage ('makefile')
				{
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
				}
		}
	}
}
		

