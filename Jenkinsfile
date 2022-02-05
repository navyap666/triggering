node('built-in') {
    stage('continuous download_test') {
    git'https://github.com/navyap666/Jenkins_multiBranch127.git'
}
    stage('continuous built_test') {
    sh 'mvn package'
}

    stage('continuous deployment_test') {
    sh 'scp /home/ubuntu/.jenkins/workspace/job/webapp/target/webapp.war ubuntu@172.31.12.8:/var/lib/tomcat9/webapps/qaenv.war'
}
stage('continuous testing_test') {
    sh 'echo "test passed"'
}
}
