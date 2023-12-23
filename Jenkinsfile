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
		stage('3-code coverage'){
			steps{
				sh 'pwd'
			}
		}
        stage('3-clean'){
			steps{
				sh 'ls -a'
			}
		}
        stage('4-firstparajob'){
            parallel{
			  stage('3-clean'){
			    steps{
				  sh 'ls -a'
			}
		}
        stage('5-os-version'){
			steps{
				sh 'cat /etc/pos-release'
              }
			}
        stage('6-comment'){
			steps{
				echo "End of parallel job"
              }
			}
		}
	}
}