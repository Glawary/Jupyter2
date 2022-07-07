pipeline {
	agent any

	stages {
		stage('Build'){
			steps{
                           sh '''
				#!bin/bash
				echo 'Building...'
                                pwd
                                pip3 install -r requirements.txt
				jupyter-nbconvert --to=html Jupyter2.ipynb
			      '''
                        }
		}
		stage('Test'){
			steps{
				echo 'Testing..'
			}
		}
}
                post {
        always {
              
               archiveArtifacts artifacts: 'Jupyter2.html', followSymlinks: false
     
               }
   }

     
}
