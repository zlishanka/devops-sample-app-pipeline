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
    }

    stages {
        stage("Checkout from SCM") {
            steps {
                git branch: 'main', credentialId: 'github', url: 'https://github.com/zlishanka/devops-sample-app-pipeline'
            }
        }
    }
}