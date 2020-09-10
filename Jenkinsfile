node {

    stage('Checkout scm') {

    checkout scm
    }
    stage('Build Alpine3.11,Java11') {
    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {

        def customImage = docker.build("venkateshdevops2020/alpinebuild_3.11_jdk")
     
        /* Push the container to the custom Registry */
        customImage.push()
    }
}
}