node{
    stage('code checkout'){
        git 'https://github.com/shubhamkushwah123/addressbook-demo.git'
    }
    
    stage('clean.. compile... test... package...'){
        sh 'mvn clean package'
    }
    
    stage('deploy to tomcat'){
        deploy adapters: [tomcat8(credentialsId: '8bf4758e-c528-4f41-98d3-afcebacac6c6', path: '', url: 'http://15.206.73.20:8888/')], contextPath: 'demo-deploy', war: '**/*.war'
    }
}
