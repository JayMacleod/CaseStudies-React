echopipeline {
    agent any

environment {
    VERSION = readMavenPom().getVersion()
}

    stages {
        stage('Version'){
            steps {
                echo "${VERSION}"
            }
        }

        stage('Build') {
            steps {
	        echo "Staging"
            }
        }

        stage('Testing Environment') {
            steps {
                echo "Testing Environment"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy"
            }
        }

        stage('Staging1') {

          when{
              expression{
              env.BRANCH_NAME=='developer'
              }
          }
            steps {
                echo "Staging1"
            }
        }

        stage('End2end Tests') {
            steps {
                echo "End2End Tests"
            }
        }

        stage('Production') {

            when{
                expression{
                env.BRANCH_NAME=='master'
                }
            }
            steps {
                echo "Production"
            }
        }

    }
}

