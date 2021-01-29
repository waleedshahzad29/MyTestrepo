pipeline {
    agent any

    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
//                sh './gradlew assemble'
                sh 'mkdir origin'
                sh 'touch "${BRANCH_NAME##origin/}_${TAG_NAME}"'
                sh 'echo readable >> "${BRANCH_NAME##origin/}_${TAG_NAME}"'
            }
        }
        stage('Test') {
            steps {
//                sh './gradlew test'
                echo "This build was successful!"
            }
        }
    }
}
