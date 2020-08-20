pipeline {
   agent any
   stages {
     stage('build') {
       steps {
         script {
           openshift.withCluster('aws1') {
             openshift.withProject('shared') {
               echo "Building on project ${openshift.project()}"
               def build = openshift.selector("bc/fl-yo-test")
               build.describe()
               def buildconfig = build.startBuild()
               timeout(5) { // Throw exception after 5 minutes
                 buildconfig.untilEach{
                     return (it.object().status.phase == "Complete")
                 }
               }
             }
           }
         }
       }
     }
     stage('deploy') {
       steps {
         script {
           openshift.withCluster('aws1') {
             openshift.withProject('shared') {
             def dc=openshift.selector("dc/fl-yo-test")
             dc.rollout().latest()
             }
           }
         }
       }
     }
   }
}
