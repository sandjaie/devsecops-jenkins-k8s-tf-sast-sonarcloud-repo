pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=buggywebapp10 -Dsonar.organization=sandjaie10 \
		-Dsonar.host.url=https://sonarcloud.io -Dsonar.login=ac0ee9e833b4b9a224cb29c41205fa4de3e20951'
			}
        } 
  }
}
