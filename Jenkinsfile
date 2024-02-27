pipeline {

    agent {
         node {            
            label 'docker-host-test'
         }
    }   

    options{
        timeout(time:1, unit:'HOURS')
    }

    stages {
        stage('Docker Build Pipeline') {
            steps {
                dockerBuild()
            }
        }
    }

    post {        
        always{           
            buildDockerAlways()
        }

    }

}
