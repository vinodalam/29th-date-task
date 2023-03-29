pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               // bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/29th-date-task.git"
                bat "mvn clean -f 29th-date-task "
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f 29th-date-task"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f 29th-date-task"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f 29th-date-task"
            }
        }
    }
}
