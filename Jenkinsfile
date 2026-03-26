pipeline {
    agent any

    stages {

        stage("Checkout Code") {
            steps {
                git url: 'https://github.com/swapnilpadwal311/company.git', branch: '2026Q1'
			     }
			
			steps {
                script {
                    docker.image('httpd').run("-dp 80:80 -v ${pwd()}:/usr/local/apache2/htdocs/ --name c1")	
				  }
				
				}
            }
		stage("Checkout Code") {
            steps {
                git url: 'https://github.com/swapnilpadwal311/company.git', branch: '2026Q2'
			     }
			
			steps {
                script {
                    docker.image('httpd').run("-dp 90:80 -v ${pwd()}:/usr/local/apache2/htdocs/ --name c2")	
				  }
				
				}
            }
			
		stage("Checkout Code") {
            steps {
                git url: 'https://github.com/swapnilpadwal311/company.git', branch: '2026Q3'
			     }
			
			steps {
                script {
                    docker.image('httpd').run("-dp 8080:80 -v ${pwd()}:/usr/local/apache2/htdocs/ --name c3")	
				  }
				
				}
            }
		}
	}
