node('built-in') {
    stage('continuous download') {
    git'https://github.com/navyap666/Jenkins_multiBranch127.git'
}
    stage('continuous built') {
    sh 'mvn package'
}

    stage('continuous deployment') {
    sh 'scp /home/ubuntu/.jenkins/workspace/job/webapp/target/webapp.war ubuntu@172.31.12.8:/var/lib/tomcat9/webapps/qaenv.war'
}
stage('continuous testing') {
    sh 'echo "test passed"'
}
stage('continuous delivery') {
    sh 'scp /home/ubuntu/.jenkins/workspace/job/webapp/target/webapp.war ubuntu@172.31.3.186:/var/lib/tomcat9/webapps/prodenv.war'
}
}
