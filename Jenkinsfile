#!groovy

stage 'multibranch test 1'

node('master') {
    sh "whoami"
    echo "test 1"
}

stage 'multibranch test 2'

node {
  echo "test 2"
  pwd()

    }
    
    
stage 'Build in parallel 3'

parallel (

  'app': {

    node {
      echo "testttt" 
    }

  },

  'app2': {

    node {
      echo "testttt2"
      build 'test2'
      
    }
  
  }

)
