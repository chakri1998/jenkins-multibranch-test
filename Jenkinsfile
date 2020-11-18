pipeline {
    agent any
    stages {
        stage("printing-branch-name") {
            steps {
                script{
                echo "main"

                             }
                       }
        }
          stage("printing-job-name"){
        steps {
        echo "$JOB_NAME"
}
}

        
        stage("Setting-Buildnumber-for-downstream-job") {
            steps {
                script{
                echo "main"

Jenkins.instance.getItemByFullName("test-multibranch/test").updateNextBuildNumber((Jenkins.instance.getItemByFullName("$JOB_NAME").getNextBuildNumber()-1))
                             }
                       }
        }
          stage("triggering-downstream-job"){
        steps {
    build job: "test-multibranch/test"
}
}
}
}

