pipeline {
    agent any

    stages {

        stage("Checkout Code") {
            steps {
                git url: 'https://github.com/swapnilpadwal311/company.git', branch: 'main'
            }
        }

        stage("Run Container") {
            steps {
                script {
                    docker.image('httpd').run("-d -p 80:80 -v ${pwd()}:/usr/local/apache2/htdocs/ --name web1")
                    docker.image('httpd').run("-d -p 90:80 -v ${pwd()}:/usr/local/apache2/htdocs/ --name web2")
                    docker.image('httpd').run("-d -p 8080:80 -v ${pwd()}:/usr/local/apache2/htdocs/ --name web3")
                }
            }
        }
    }
}
