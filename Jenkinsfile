pipeline {
	agent any  
	stages {
		stage('BUILD') {
			steps {
				sh '''
					pwd
					sleep 5
					echo This is the fist stage: BUILD
				'''
			}	
		}
		
		stage('TEST') {
			parallel {
				steps('test1') {
					sh 'sleep 3'
					echo "phase1"
				}
				steps('test2') {
					sh 'sleep 3'
					echo "phase2"
				}
				steps('test3') {
					sh 'sleep 3'
					echo "phase3"
				}
			}	
		}
		
		stage('DEPLOY') {
			steps {
				sh '''
					pwd
					sleep 5
					echo This is the fist stage: DEPLOY
				'''
			}	
		}
	}
}
