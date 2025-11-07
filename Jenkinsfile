pipeline{
 environment{
    DOCKER_IMAGE: "subhu667/my-img",
    DOCKER_TAG : "1.0"
 }
    stages{
        stage("checkout from git"){
            steps{
                echo "========Checkout========"
                git branch: 'master', url: "https://github.com/Ramakant-Kushwaha/RunCheck.git"
            }
        }

        stage("checkout from git"){
            steps{
                echo "======== running the container ========"
                docker run -d -p 8081:8080 --name my-conppp ${DOCKER_IMG}:DOCKER_TAG
            }
        }
}
}
