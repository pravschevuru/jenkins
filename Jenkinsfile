pipeline{
    agent any
    environment{
        VERSION = "${env.BUILD_ID}"
    }
    stages{
        stage("sonar qube analysis"){
		agent any

tools{
gradle 'gradle7.3.2'

}
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonar_token') {
                            sh 'chmod +x gradle'
                            sh './gradle sonarqube'
							}
					}
						}
				}
					}
							}
