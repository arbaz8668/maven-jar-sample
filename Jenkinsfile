pipeline{
    // agent{
    //     label "agent1"
    // }

    agent any

    stages{
        stage("Maven build"){
            steps{
                echo "========executing Maven build========"
                mvn clean install

            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
            }
        }

        // stage("sonar code coverage "){
        //     steps{
        //         echo "========executing code coverage using sonarqube========"
        //         script {
                    
        //           sh 'export SONAR_SCANNER_OPTS="-Xmx2048m"'
        //           sh "/opt/sonar-scanner/bin/sonar-scanner  \
        //             -Dsonar.projectKey=PROJECT-KEY-IN-SQ \
        //             -Dsonar.projectVersion=PROJECT-VERSION-IN-SQ \
        //             -Dsonar.exclusions= FOLDER-To-NOT-SCAN \
        //             -Dsonar.sources=FOLDER-To-SCAN \
        //             -Dsonar.java.binaries=**/target/classes  \
        //             -Dsonar.qualitygate=QG-NAME \
        //             -Dsonar.host.url=URL-OF-SQ \
        //             -Dsonar.login=TOKEN-ID"
        //        }
        //     }
        //     post{
        //         always{
        //             echo "========always========"
        //         }
        //         success{
        //             echo "========A executed successfully========"
        //         }
        //         failure{
        //             echo "========A execution failed========"
        //         }
        //     }
        // }

        // stage("deploy to tomcat") {
        // steps{
        //     scp target/cvhcjhsg.jar ec2-machine@192.168.1.57:/tmp

        // }

        }
        
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
