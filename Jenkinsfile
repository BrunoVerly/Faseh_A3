pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building e Deploy Java..'
                sshagent(credentials: ['159.112.177.250']) {
                    sh "ssh -o StrictHostKeyChecking=no -l opc 159.112.177.250 'cd ~/projeto && ./bash_script.sh'"
                }
            }
        }

        stage('Deploy') {
            steps {
               echo 'Deploy Mysql..'
               sshagent(credentials: ['159.112.177.250']) {
                    sh "ssh -o StrictHostKeyChecking=no -l opc 159.112.177.250 'cd ~/projeto && ./mysql_bash_script.sh'"
               }
            }
        }
    }
}
