node{
    stage('code checkout'){
        git 'https://github.com/shubhamkushwah123/addressbook-demo.git'
    }
    
    stage('clean.. compile... test... package...'){
        sh 'mvn clean package'
    }
    
    stage('deploy to tomcat'){
    deploy adapters: [tomcat9(credentialsId: 'tomcat-creds', path: '', url: 'http://3.144.32.162:8080/')], contextPath: 'addressbook-2.0', war: '**/*.war'    
    }
}
