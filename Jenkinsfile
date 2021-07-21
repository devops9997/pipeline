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
				stage('test1') {
					steps {
						sh 'sleep 3'
						echo "phase1"
					}
				}
				stage('test2') {
					steps {
						sh 'sleep 3'
						echo "phase2"
					}
				}
				stage('test3') {
					steps {
						sh 'sleep 3'
						echo "phase3"
					}
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
