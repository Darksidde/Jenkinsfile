pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                sh 'npm install' // veya projenizin derlenmesi için gereken diğer komutlar
            }
        }
        stage("Test") {
            steps {
                sh 'npm test' // veya test senaryolarını çalıştıracak diğer komutlar
            }
        }
        stage("Deploy") {
            steps {
                sh 'npm deploy' // veya uygulamanızın dağıtılması için gereken diğer komutlar
            }
        }
    }
}
