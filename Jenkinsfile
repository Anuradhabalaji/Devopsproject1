pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "This is build stage"
				sh "docker build -t jenkins-docker ."
            }
        }
        stage('Tag') { 
            steps {
                echo "This is test stage"
				sh "docker tag jenkins-docker dockeruseranu123/jenkins-image"
            }
        }
        stage('Login') { 
            steps {
                echo "This is login stage"
				sh "docker login --username=dockeruseranu123 --password=Raghav!23"
            }
        }
		stage('Push') { 
            steps {
                echo "This stage is Pushing image to docker hub"
				sh "docker push dockeruseranu123/jenkins-image"
            }
        }
    }
}
