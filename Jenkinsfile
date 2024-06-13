pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building e Deploy Java..'
                sshagent(credentials: ['159.112.177.250']) {
                    sh "ssh -o StrictHostKeyChecking=no -l ubuntu 159.112.177.250 'cd ~/oficina/Faseh_A3/src/main/resources && ./script-banco-container'"
                }
            }
        }
        stage('Build') {
            steps {
                echo 'Building e Deploy Java..'
                sshagent(credentials: ['159.112.177.250']) {
                    sh "ssh -o StrictHostKeyChecking=no -l ubuntu 159.112.177.250 'cd ~/oficina/Faseh_A3/src/main/resources && ./docker'"
                }
            }
        }
    }
}
