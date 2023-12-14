pipeline {
    agent any
    stages {
        stage("build") {
            steps {
                script {
                    def gv = new YourClassNameHere() // gv'nin bir sınıf adıyla değiştirilmesi gerekiyor
                    gv.buildApp()
                }
            }
            post {
                always {
                    echo 'Build stage completed'
                }
            }
        }
        stage("test") {
            when {
                expression {
                    params.executeTests
                }
            }
            steps {
                script {
                    gv.testApp()
                }
            }
            post {
                always {
                    echo 'Test stage completed'
                }
            }
        }
        stage("deploy") {
            steps {
                script {
                    gv.deployApp()
                }
            }
            post {
                always {
                    echo 'Deployment stage completed'
                }
            }
        }
    }
}
