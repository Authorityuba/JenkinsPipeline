pipeline{
    agent any
    stages{
        stage("version of software"){
            steps{
                bat "java --version"
            }
        }
        stage("compile java program"){
            steps{
                bat "javac SimpleJavaProj.java"
            }
        }
        stage("crun thhe java program"){
            steps{
                bat "java SimpleJavaProj"
            }
        }
        //stage("Test"){
           // steps{
           //     bat 'echo "Fail!",exit 1'
           // }
        //}
    }
    post{
        always{
            echo'This will always run'
        }
        success{
            echo'This will run only if sucessful'
        }
        failure{
            echo'This will run only if failed'
        }
        changed{
            echo'This will run only if the state of the Pipeline had changed'
            echo'Example: if the Pipeline was previously failing but now successful'
        }
    }
}