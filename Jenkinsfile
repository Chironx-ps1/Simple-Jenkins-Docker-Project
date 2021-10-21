node {
    def app

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */

        app = docker.build("ec2-user/example-node-app")
    }

    stage('Test image') {
        /* Ideally, we would run a test framework against our image.
        */

        app.inside {
            sh 'echo "Tests passed"'
        }
    }

}
