pipeline {
	 agent { label 'master'}
 
	stages {
		stage ('make and maven') {
			parallel {
				stage ('makefile')
				{
							steps { 
							git 'https://github.com/vkavyag/c-project.git'
							sh 'make'
							      }
							}
		
				stage ('maven') {
	
							steps {
							git 'https://github.com/vkavyag/hello-world.git'
							sh 'mvn clean install'
							      }	
							}
				}
		}
	}
}
		

