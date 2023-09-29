pipeline{
	agent any 
	stages{
		stage('1-clonecode'){
			steps{
				checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'team7 git-id', url: 'https://github.com/etech-team007/gitjenkins.git']])
			}
		}
		parallel{
			stage('2-artifactbuild'){
			steps{
				sh 'df -h'
			}
		}
		stage('3-unitest'){
			steps{
				sh 'lscpu'
			}
		}
		}
		stage('4-build'){
			steps{
				sh 'free -m'
			}
		}
		stage('5-deploy'){
			steps{
				sh 'uname -r'
			}
		}
		stage('6-test'){
			steps{
				sh 'cat /etc/os-release'
			}
		}
		stage('7-approval'){
			steps{
				input message: 'Do you want to approve this?', ok: 'Yes'
			}
		}
	}
}



