pipeline{
    agent{
        label 'master'}
        tools{maven 'M3'}
        stages{
            stage('CHeckout'){
                steps{
                    git branh: 'main', url:'https://github.com/chandana-srinivas/SpringPetClinic.git'
                    
                }
            }
            stage('Build'){
                steps{
                    sh 'mvn compile'
                }
            }
            stage('Test'){
                steps{
                    sh 'mvn test'
                }
            }
            stage('Package'){
                sh 'mvn package'
            }
        }
        stage('Deploy'){
            steps{
                sh 'java -jar /home/coder/.jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
            }
        }
}

}
