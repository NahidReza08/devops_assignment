pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo '--- Checking out the latest code from the main branch ---'
                git(
                    branch: 'main',
                    credentialsId: 'nahid_reza', // make sure this matches your Jenkins credential ID
                    url: 'https://github.com/NahidReza08/devops_module1_assignment.git'
                )
            }
        }

        stage('Read hello.txt') {
            steps {
                echo '--- Reading hello.txt file ---'
                script {
                    def content = readFile('hello.txt')
                    echo "📄 Content of hello.txt:\n${content}"
                }
            }
        }
    }
}