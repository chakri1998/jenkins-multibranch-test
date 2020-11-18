pipeline {
    agent any
    stages {
        stage("Setting-Buildnumber-for-downstream-job") {
            steps {
                script{
                echo $JOB_NAME  

//Jenkins.instance.getItemByFullName("*downstream-job*").updateNextBuildNumber((Jenkins.instance.getItemByFullName("*upstream-job*").getNextBuildNumber()-1))
                             }
                       }
        }
          stage("triggering-downstream-job"){
        steps {
        echo "$JOB_NAME"
        echo "hello world."
//    build job: "*downstream-job*"
}
}

}
}
