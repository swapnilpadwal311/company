pipeline {
    agent any

    stages {

        stage("Checkout Q1") {
            steps {
                dir("Q1") {
                    git url: 'https://github.com/swapnilpadwal311/company.git', branch: '2026Q1'
                }
            }
        }

        stage("Run c1") {
            steps {
                script {
                    docker.image('httpd').run("-dp 80:80 -v ${pwd()}/q1:/usr/local/apache2/htdocs/ --name c1")
                }
            }
        }

        stage("Checkout Q2") {
            steps {
                dir("Q2") {
                    git url: 'https://github.com/swapnilpadwal311/company.git', branch: '2026Q2'
                }
            }
        }

        stage("Run c2") {
            steps {
                script {
                    docker.image('httpd').run("-dp 90:80 -v ${pwd()}/q2:/usr/local/apache2/htdocs/ --name c2")
                }
            }
        }

        stage("Checkout Q3") {
            steps {
                dir("Q3") {
                    git url: 'https://github.com/swapnilpadwal311/company.git', branch: '2026Q3'
                }
            }
        }

        stage("Run c3") {
            steps {
                script {
                    docker.image('httpd').run("-dp 8080:80 -v ${pwd()}/q3:/usr/local/apache2/htdocs/ --name c3")
                }
            }
        }
    }
}
