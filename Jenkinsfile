pipeline{
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['1.0.2', '2.0,3.0', '4.50'], description: '')
        booleanParam(name: 'executeTests', defaultvalues: true, description:'')
    }
       
      stages{
          stage "build" {
            steps {
             "echo iam going"
           }
           
         }   
       stage "test" {
           when {
               expression {
                 prams.executeTests
               }
           }
            steps {
             echo "iam going"
           }
           
         }   
         stage "deploy" {
            steps {
              
              }
             
           }
           
         }   

       }
    }
}
