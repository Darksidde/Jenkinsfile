pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Building the project..."
                // Buraya projenizin derlenmesi, paketlenmesi veya herhangi bir yapı aşaması ekleyebilirsiniz.
            }
        }
        
        stage("Test") {
            when {
                expression {
                    params.executeTests == 'true'
                }
            }
            steps {
                echo "Running tests..."
                // Buraya testlerin çalıştırılması için gerekli adımları ekleyebilirsiniz.
            }
        }

        stage("Deploy") {
            when {
                expression {
                    params.deploy == 'true'
                }
            }
            steps {
                echo "Deploying the application..."
                // Buraya uygulamanızın dağıtılması veya yayınlanması için gerekli adımları ekleyebilirsiniz.
            }
        }
    }
}
