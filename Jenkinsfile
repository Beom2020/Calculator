pipeline { 
     agent any 
     stages { 
        stage('Compile') {
            steps {
                // 실행 권한 부여 추가!
                sh 'chmod +x gradlew'
                sh './gradlew compileJava'
            }
        }
        stage("Build") {                          
            steps {
                sh "./gradlew build"
            }
        }
        stage("Unit test") { 
            steps { 
                sh "./gradlew test" 
            }           
        } 
    } 
} 