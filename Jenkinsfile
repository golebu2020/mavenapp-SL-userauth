def gv
pipeline{
    agent any
    stages{
        stage ("init"){
            steps{
                script{
                    gv = load "script.groovy"
                }
            }
        }

        stage ("build jar"){
            steps{
                script{
                    echo "Building the app jar..."
                }
            }
        }

        stage ("build image"){
            steps{
                script{
                    echo "Building the app image..."
                }
            }
        }
        
        stage ("deploy"){
            steps{
                script{
                    echo "Deploying the app..."
                }
            }
        }
    }
}