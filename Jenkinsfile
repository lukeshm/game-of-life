node('master') {
    
    stage ("Checkout")
    {
        
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '671f931f-e878-4984-aa51-96ec63d57fee', url: 'https://github.com/lukeshm/game-of-life.git']]])
    }
    
    stage('Test') {
        
        sh 'mvn test'
        
    }
    
    stage('Build')
    
    sh 'mvn package'
}
