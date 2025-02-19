pipeline {
    agent any

    stages {
    stage('Conjur Credentials Secret  ') {
            steps {
             script{
                    user =null
 
                   /// withCredentials([conjurSecretCredential(credentialsId: 'apikey-username-cred', variable: 'CONJUR_SECRET')]) {
                 withCredentials([conjurSecretCredential(credentialsId: 'conjur_sonarqube_cred_freestyle_updated-credential1', variable: 'CONJUR_SECRET')]) {
                      user=CONJUR_SECRET
                }
                echo " Conjur Secret Value : ${user}"
                }
            }
        }
        
           stage(' Conjur Secret  Username Cred ') {
            steps {
             script{
                    user =null
 
                  // withCredentials([conjurSecretCredential(credentialsId: 'conjursecrect-username-ID', variable: 'CONJUR_SECRET')]) {
               withCredentials([conjurSecretUsername(credentialsId: 'conjursecrect-username-ID', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
                      user=CONJUR_SECRET
                }
                echo " API KEY URL : ${user}"
           
        }
       }  
    }
    }
}
