 pipeline
 {
 	agent any
 	stages{
 		stage('Build Application'){
 		steps{
 			bat 'mvn clean install'
 			}
 		}
 		
 		stage('Deploy Application To Mulesoft Cloudhub'){
 		steps{
 		 	bat 'mvn clean deploy -DmuleDeploy'
 		}
 		}
 		
 		stage('Perform Regression Testing'){
 		steps{
 			bat 'newman run C:\\Users\\tavet\\Desktop\\newman\\worldtimezone.postman_collection.json --disable unicode'
 			}
 		}
 	}
 }
 