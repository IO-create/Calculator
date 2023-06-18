pipeline {
	agent any
	tools {
    	maven 'my_mvn'
	}
	stages {
    	stage("Checkout") {   
        	steps {               	 
            	git branch: 'main', url: 'https://github.com/IO-create/Calculator.git'        	 
           	 
        	}    
    	}
    	stage('Maven Clean') {
        	steps {
        	bat "mvn clean"  	 
        	}
    	}
    	stage('Maven Build') {
        	steps {
        	bat "mvn compile"  	 
        	}
    	}
   	 
    	stage("Unit test") {          	 
        	steps {  	 
            	bat "mvn test"          	 
       	}
}
}
}
