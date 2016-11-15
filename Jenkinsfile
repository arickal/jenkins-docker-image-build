node("docker") {
    git url: "https://github.com/arickal/jenkins-docker-image-build"
    
    stage "build"
    def app = docker.build "test-docker-build-image"
    
    stage "publish"
    app.push 'master'
    app.push "${commit_id}"
}
