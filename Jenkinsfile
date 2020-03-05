
 pipeline 
{
agent any
tools
{
maven "maven"
}
stages {
stage('Gitcheckout')
{
steps{
git 'https://github.com/Akhil2003/game-of-life.git'
}
}
stage('Maven conf')
{
steps {
sh label: '', script: 'mvn clean package'
}
}
      
//stage('sonarqube') {
  //environment 
  //{
   //def scannerHome = tool 'sonarqube'
    //}
   //steps {
     //   withSonarQubeEnv('sonarqube') {
       //sh "${scannerHome}/bin/sonar-scanner"
//}
  //  timeout(time: 10, unit: 'MINUTES') {
    // waitForQualityGate abortPipeline: true
     //}
	//  }
      //}
nexusArtifactUploader artifacts: [[artifactId: 'gameoflife', classifier: '', file: 'gameoflife-web/target/gameoflife.war', type: '.war']], credentialsId: '', groupId: '1234', nexusUrl: '52.87.226.7:8081/nexus', nexusVersion: 'nexus2', protocol: 'http', repository: 'sam123', version: 'BUILD_NUMBER'
}
}
stage ('Deploy war')
{
steps {
sh label: '', script: 'ansible playbook deploye'
    }
  }
 }
}  
