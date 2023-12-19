pipeline{
	agent any
	stages{
		stage('1-clean workspace'){
			steps{
				sh 'ls'
			}
		}
		stage('2-git clone'){
			steps{
				checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'jenkins-jobs', url: 'https://github.com/team8-org/jenkinst8.git']])
			}
		}
		stage('3-maven build'){
			steps{
				sh 'lsblk'
			}
		}
		stage('3-maven build'){
			steps{
				sh 'pwd'
			}
		}
	}
}