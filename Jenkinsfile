pipeline{
    agent {
        label "jenkins-agent"
    }

    tools {
        jdk 'Java17'
        maven 'Maven3'
    }

    stages {
        stage("Cleanup Workspace") {
            steps {
                echo "========executing A========"
                cleanWs()
            }
        }

        stage("Build Application") {
            steps {
                sh "mvn clean package -DpomFile=pom.xml"
            }
        }

        stage("Test Application") {
            steps {
                sh "mvn test"
            }
        }
    }
}