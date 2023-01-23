pipeline {
    agent any
    parameters {
            string(defaultValue: "", description: 'SONARCLOUDKEY', name: 'SONARCLOUDKEY')
    }
    tools {
        maven 'Maven_3_5_2'  
    }
    stages{
    stage('CompileandRunSonarAnalysis') {
        steps {
            sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=buggywebapp10 -Dsonar.organization=sandjaie10 \
            -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=${SONARCLOUDKEY}'
            }
        }
    }
}
