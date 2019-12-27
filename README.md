### Create a basic python program which can deployed to AWS lambda. Create linter scripts and unit test coverage

Make sure python (preferred python3.7) is added to path.

      python --version
       or		
     python3.7 --version
     
 Install virtualenv using pip.

     pip install virtualenv 
   
 First create a virtual environment for the project.
 
    virtualenv -p python3.7 venv or virtualenv venv
       . venv/bin/activate (Linux)
       . venv/Scripts/activate (windows)

set up linter:

    create setup.cfg file for  pycodestyle and pep8
    generate pylintrc file using below command for pylint
      pylint --generate-rcfile > .pylintrc
      (change max_length_character to 160 (as per requiremnet))
      
    Linter Script:
       create lint.sh file
        run using command sh lint.sh
 
 To run app using below command
 
     python src/lambda_handler.py
     
  Run unit Test case of app using below command
  
         python -m unittest tests/test_lambda_handler.py
         
  Install dependencies for AWS Lambda
 
    pip install -r requirements.txt -t ./
    
   
Create zip file of all library and upload it into AWS lambda function

change Handler info from AWS Console to below name

    src/lambda_handler.lambda_handler ---->this is like (src folder/my_module_name.function_name)
    
 
Upload lambda_handler.zip file to AWS lambda

   
        
     
     
   
  



