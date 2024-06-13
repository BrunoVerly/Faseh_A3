pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building e Deploy Java..'
                sshagent(credentials: ['159.112.177.250']) {
                    sh "ssh -o StrictHostKeyChecking=no -l ubuntu 159.112.177.250 'cd ~/oficina && ./bash_script.sh'"
                }
            }
        }

        stage('Deploy') {
            steps {
               echo 'Deploy Mysql..'
               sshagent(credentials: ['159.112.177.250']) {
                    sh "ssh -o StrictHostKeyChecking=no -l ubuntu 159.112.177.250 'cd ~/oficina && ./mysql_bash_script.sh'"
               }
            }
        }
    }
}
