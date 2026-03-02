pipeline {
    agent any

    stages {
        stage('git clone') {
            steps {
                git branch: 'main', url: 'https://github.com/yashwant-sh/spring-petclinic.git'
            }
        }
        
         stage('create mvn package') {
            steps {
               sh 'mvn package'
            }
        }
    }
    post{
        success{
            mail bcc: '', body: 'aee vedya bat ka grip nikal ke', cc: 'harshvpatel2807@gmail.com', from: '', replyTo: '', subject: 'vedya...bat ka grip', to: 'yashwantjangrarn32@gmail.com'
        }
        failure{
             success{
            mail bcc: '', body: 'aee vedya bat ka grip nikal ke', cc: 'harshvpatel2807@gmail.com', from: '', replyTo: '', subject: 'vedya...bat ka grip hogya fail', to: 'yashwantjangrarn32@gmail.com'
        }
     }
    }
    }
    
