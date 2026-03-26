pipeline {
    agent any

    stages {

        stage("Checkout Code Q1") {
            steps {
                git url: 'https://github.com/swapnilpadwal311/company.git', branch: '2026Q1'
            }
        }

        stage("Create Container c1") {
            steps {
                script {
                    docker.image('httpd').run("-d -p 80:80 -v ${pwd()}:/usr/local/apache2/htdocs/ --name c1")
                }
            }
        }

        stage("Checkout Code Q2") {
            steps {
                git url: 'https://github.com/swapnilpadwal311/company.git', branch: '2026Q2'
            }
        }

        stage("Create Container c2") {
            steps {
                script {
                    docker.image('httpd').run("-d -p 90:80 -v ${pwd()}:/usr/local/apache2/htdocs/ --name c2")
                }
            }
        }

        stage("Checkout Code Q3") {
            steps {
                git url: 'https://github.com/swapnilpadwal311/company.git', branch: '2026Q3'
            }
        }

        stage("Create Container c3") {
            steps {
                script {
                    docker.image('httpd').run("-d -p 8080:80 -v ${pwd()}:/usr/local/apache2/htdocs/ --name c3")
                }
            }
        }
    }
}
