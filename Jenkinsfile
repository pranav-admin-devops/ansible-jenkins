pipeline{
    agent any
    stages {
        stage('Check Files') {
            steps {
                sh '''
                pwd
                ls -l
                '''
            }
        }
        stage ('Ping servers') {
            steps {
                sh  '''
                ansible linux -m ping
                '''
            }
        }
        stage ('Run Playbok') {
            steps {
                sh '''
                ansible-playbook user.yml
                '''
            }
        }
    }
}
