pipeline{

    agent any

    stages {

        stage ('Compile Stage') {

            steps {

                withMaven(maven: 'maven_3.5.2') {
                    sh 'mvn clean install'

                }

            }
         stage ('Test Stage') {

            steps {

                withMaven(maven: 'maven_3.5.2') {
                    sh 'mvn test'

                }

            }
          }
         stage ('Deployment Stage') {

            steps {

                withMaven(maven: 'maven_3.5.2') {
                    sh 'mvn deploy'

                }
			  }
            }
        }
    }
}
