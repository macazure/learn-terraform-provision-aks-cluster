pipeline {
  
agent any
  tools {
        "org.jenkinsci.plugins.terraform.TerraformInstallation" "terraform"
    }
  
  
//   environment {
//        TF_HOME = tool('terraform')
//        TF_IN_AUTOMATION = "true"
//        PATH = "$TF_HOME:$PATH"
//    }
      stages {

    

      stage('TF Init&Plan') {
        steps {
     gi     container(terraform) {
          sh 'terraform init'
          sh 'terraform plan'
        }      
      }
    }

//      stage('Approval') {
  //      steps {
  //        script {
   //         def userInput = input(id: 'confirm', message: 'Apply Terraform?', parameters: [ [$class: 'BooleanParameterDefinition', defaultValue: false, description: 'Apply terraform', name: 'confirm'] ])
    //      }
 //       }
//      }

 //     stage('TF Apply') {
//        steps {
 //         sh 'terraform apply -input=false'
  //      }
//      }
//    }   
 }
}
