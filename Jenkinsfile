pipeline{
    agent any
    environment{
        VERSION = "${env.BUILD_ID}"
    }
    stages{
        stage("sonar qube analysis"){
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonar_token') {
                            sh 'chmod +x gradlew'
                            sh './gradlew sonarqube'
							}
					}
						}
				}
					}
							}
