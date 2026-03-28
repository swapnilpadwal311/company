pipeline {

       agent any 
	       
		stages {
              stage ("deploy 2026Q1"){
                 steps {
				    git branch: "2026Q1", url: "https://github.com/swapnilpadwal311/company.git" 
				     
                       sh "docker rm -f c1 || true"					 
                       sh "docker run -dp 80:80 --name c1 httpd:latest"
					   sh "docker exec c1 rm -rf /usr/local/apache2/htdocs/*"
					   sh "docker cp . c1:/usr/local/apache2/htdocs/"
					   }
					}
					
			  stage ("deploy 2026Q2"){
                 steps {
                    git branch: "2026Q2", url: "https://github.com/swapnilpadwal311/company.git"
					
                       sh "docker rm -f c2 || true"					 
                       sh "docker run -dp 90:80 --name c2 httpd:latest"
					   sh "docker exec c2 rm -rf /usr/local/apache2/htdocs/*"
					   sh "docker cp . c2:/usr/local/apache2/htdocs/"
					   }
					}
					
			  stage ("deploy 2026Q3"){
                 steps {
				    git branch: "2026Q3", url: "https://github.com/swapnilpadwal311/company.git"
					
                       sh "docker rm -f c3 || true"					 
                       sh "docker run -dp 70:80 --name c3 httpd:latest"
					   sh "docker exec c3 rm -rf /usr/local/apache2/htdocs/*"
					   sh "docker cp . c3:/usr/local/apache2/htdocs/"
					   }
					}
				}
			}	
					
