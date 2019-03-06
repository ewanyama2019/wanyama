node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t wanyama:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'ewanyamadockerxt' -p '1Mdcccl3x3' "
sh "docker tag wanyama:latest ewanyamadockerxt/wanyama:latest"
sh "docker push ewanyamadockerxt/wanyama:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
