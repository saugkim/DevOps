Learn YAML
============

yaml ? 
*******
| YAML stands for Yet Another Markup Language at origin.  
| Now it stands for YAML Aint Markup Language.   
| It can be used for configuration like xml, json ...  
| It is humal readable data serialization standard.  

Configuration file can have
 - input(source) output(build) location
 - parameters input (avoid hard code)
 - install dependencies
 - run cmake
 - access control
 - ...


Syntax -good to know to write yaml code, easy to write and read!
*******************************************************************
- string: without quotes(in case no special charactor of yaml), both single and double quotes
- comment: start with # for line comments same as Python (+ others), multiline?
- indentation: 2, 4 spaces, and what about tab(?)
- version: "1.0" (Better use as string, not double)
- windows_path: c:\windows == "c:\windows"
- :  : mapping 
- list:  
   - \- a  
   - \- b  
   - \- c  

example of docs/config.yml
*********************************

.. code-block:: yaml
  
    files:
      input_location: '../data/raw/data.csv'
      output_location: '../data/output/' == "../data/output/" 
  
    writing_at_run: True

how to read yaml in python code?  
*********************************

.. code-block:: python

    import yaml
    with open('docs/config.yml', 'r') as f:
      config = yaml.safe_load(f)

    location_input = config['files']['input_location']
    location_output = config['files']['output_location']

    if config['writing_at_run']:
      filename = 'result_model1.txt'
      path = location_output + filename
      dataframe.to_csv(path)


YAML systax for workflows in GitHub 
*************************************
- file extension: .yml or .yaml
- file location: .github/workflow/yaml_file_here in repository

- name: name of workflow
- on: Required The name of the GitHub event that triggers the workflow.    
- env:
- defaults: map of default setting
- jobs:   
     - jobs.<jon_id>.name 
     - jobs.<job_id>.steps 
     - jobs.<job_id>.steps.name
     - jobs.<job_id>.runs-on: Required The type of machine to run the job on. 
     - jobs.<job_id>.steps.uses
     - jobs.<job_id>.steps.run
     - jobs.<job_id>.steps.with
     - jobs.<job_id>.steps.with.entrypoint
     - jobs.<job_id>.steps.env
     - jobs.<job_id>.services

.. code-block:: yaml

  name: My workflow

  on: [push, pull_request]
 
  defaults:
    run:
      shell: bash
      working-directory: scripts
    
  jobs:
    my_deploy: # user specific
      name: my job
      runs-on: ubuntu-latest
      strategy:
        max-parallel: 4
        matrix:
          python-version: [3.7]
      steps:
        - name: My first step
          uses: actions/aws/ec2@main
          with:
            first_name: Mona
            middle_name: The
            last_name: Octocat
        - name: Check out repository
          uses: actions/checkout@v2
        - name: Use local my-action
          uses: ./.github/actions/my-action
        - name: My first step
          uses: docker://alpine:3.8
        - name: Clean temp directory
          run: rm -rf *
          working-directory: ./temp
        - name: Install Dependencies
          run: npm install
        - name: Clean install dependencies and build
          run: |
            npm ci
            npm run build
      steps:
        - name: Run a custom command
          uses: monacorp/action-name@main
          with:
            entrypoint: /a/different/executable
      steps:
        - name: My first action
          env:
            GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
            FIRST_NAME: Mona
            LAST_NAME: Octocat    


| Example using a public action in a subdirectory  
| {owner}/{repo}/{path}@{ref}  
| 
| Example using a Docker public registry action  
| docker://{host}/{image}:{tag}  
| 

| this pages yml file https://github.com/saugkim/DevOps/blob/main/.github/workflows/sphinx-build.yml

.. code-block:: .github/workflow/sphinx-build.yml
