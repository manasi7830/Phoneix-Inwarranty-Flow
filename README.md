# Postman API Automation Integration with Github Action #

This repository is demonstration of POC for integrating postman tests with github actions. The Tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_displatch. The project runs on a schedule time with the help of cron job.


The HTML report is achieved and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page https://manasi7830.github.io/Phoneix-Inwarranty-Flow/
The latest report is mailed to the team members using GMAIL SMTP.
## About Me ##
Hi This is Manasi Avachat. You can connect with me on Linkedin-(https://www.linkedin.com/in/manasi-avachat-695a4823/)
## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Githib Secrets

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for data driven testing 
9. AWS-EC2 instance for self hosted github runner.

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link:https://manasi7830.github.io/Phoneix-Inwarranty-Flow/

## HTML Report ##
The report will be created in the newman folder 
![Postman Report](https://github.com/manasi7830/Phoneix-Inwarranty-Flow/blob/static-content/NewmanReport.png)

## Project Structure ##
```
Phoneix Inwarranty Flow
├─ Inwarranty-Flow Collection CSVFile.postman_collection.json # Collection File
├─ QA.postman_environment.json #Environment File
└─ testdata.csv #TestData File

```
## How to run the Project ##
You can run the project on your local system for that:
1. Clone the project on the local system https://github.com/manasi7830/Phoneix-Inwarranty-Flow.git
2. Install Nodejs and NPM from https://www.npmjs.com/
3. Install Newman using command``` $ npm install -g newman ```
4. Install Newman-reporter-htmlextra ``` $ npm install -g newman-reporter-htmlextra ```
5. Run the newman command 
  ```
 newman run 'Inwarranty-Flow Collection CSVFile.postman_collection.json' \
            -e QA.postman_environment.json \
            -d testdata.csv \
            -r cli,htmlextra \
            --reporter-htmlextra-export ./newman/index.html
 ```

