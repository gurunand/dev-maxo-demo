/*pipeline {
    agent { label 'Master' }
    
    stages {
    	/*stage ('Code Analysis'){
	    steps {
                withSonarQubeEnv('SonarQube') {
			sh 'mvn clean sonar:sonar'
		}
	    }
	}

	stage ('Compile Stage'){
	    steps {
	        withMaven(maven : 'Maven'){
		    sh 'mvn clean package'
		}
	    }
	}

	stage ('Deploy to Nexus'){
	    steps {
	        withMaven(maven : 'Maven'){
		    sh 'mvn deploy'
		}
	    }
	}
	stage ('Deploy to QA'){
	    steps {
	            sh 'sudo ansible-playbook /etc/ansible/main.yml'
	    }
	}

    }
}
*/

pipeline {
    agent any
	tools{
		maven 'MAVEN'
	}
    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout'
		        git url: 'https://github.com/harinpatel1991/jenkins-maven-pipeline.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Clean Build'
                sh 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
                sh 'mvn test'
            }
        }
      /*  stage('JaCoCo') {
            steps {
                echo 'Code Coverage'
                jacoco()
            }
        }
        stage('Sonar') {
            steps {
                echo 'Sonar Scanner'
		       withSonarQubeEnv('sonarqube') {
			//    withSonarQubeEnv('SonarQube Server') {
      		       sh 'mvn clean install -D sonar.host.http://35.229.42.239:9000/projects'
		//bat 'C:/Dock/ci/sonar/sonar-scanner-3.0.3.778-windows/bin/sonar-scanner'
		        }
          }
        }
 
      stage('Package') {
            steps {
                echo 'Packaging'
                sh 'mvn package'
            }
        }
    }*/
}
