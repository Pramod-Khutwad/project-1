pipeline{
	agent{
		label {
			label 'built-in'
		}
	}
	
	stages{
		stage ('clone-test-repo'){
			steps {
				dir ('/mnt/projects'){
					sh "rm -rf project-1"
					sh "git clone https://github.com/Pramod-Khutwad/project-1.git"
				}
			}
		}
		
		stage ('copy-index-file'){
			steps {
				dir ('/var/www/html'){
					sh "rm -rf index.html"
				}
				sh "cp /mnt/projects/project-1/index.html /var/www/html"
			}
		}
	}	
	
}
