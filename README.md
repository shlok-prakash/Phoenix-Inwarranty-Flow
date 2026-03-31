# 🚀 Postman API Automation with GitHub Actions

![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-Automated-blue)
![Node.js](https://img.shields.io/badge/Node.js-24.x-green)
![Postman](https://img.shields.io/badge/Postman-API%20Testing-orange)

## 📌 Project Overview

This repository is a Proof of Concept (POC) demonstrating how to integrate Postman API tests with GitHub Actions for automated CI/CD execution. The tests are written and they are executed on the VM with the help of newman and newman-reporter-htmlextra. 

GitHub Actions triggers the workflow in three different ways:
 - On every push to the main branch.
 - Manually using workflow_dispatch
 - Runs on a scheduled time with the help of Cron Job.

After execution, the reports are::
- Stored as artifacts  
- Hosted on GitHub Pages : [Newman-htmlExtra Report](https://shlok-prakash.github.io/Phoenix-Inwarranty-Flow/)
- Sent via Gmail SMTP

## 👨‍💻 About Me

Hi, I'm **Shlok Prakash (aka Pandey)** — an Automation Test Engineer with 3.6+ years of experience in Automation and Functional Testing.

🔹 UI Automation: Selenium WebDriver  
🔹 API Testing: Postman, Rest Assured  
🔹 Mobile Automation: Appium  

📫 Connect with me on [LinkedIn](https://www.linkedin.com/in/shlok-prakash/)

## 🧠 Testing Coverage
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets

## 🛠️ Tech Stack

| Tools |
|------|
| Postman |
| Node.js 24.x |
| Newman |
| Newman Reporter (htmlextra) |
| GitHub Actions |
| Gmail SMTP |
| GitHub Pages |
| CSV (Data-driven testing) |
| AWS EC2 (Self-hosted GitHub runner) |


## 📊 Test Report

👉 You can directly view the latest test report of the Postman Test at the Github Page Link:<br> 
https://shlok-prakash.github.io/Phoenix-Inwarranty-Flow/

## ⚙️ HTML Report

The Report will be created in the newman folder <br> 
![Newman Report](https://github.com/shlok-prakash/Phoenix-Inwarranty-Flow/blob/static-content/newmanreport.png)

## 📂 Project Structure

        Phoenix Inwarranty Flow
        ├─ Inwarranty-flow Collection.postman_collection.json #CollectionFile
        ├─ QA.postman_environment.json #EnviromentFile
        └─ testData.csv #TestDataFile

## ▶️ How to Run

1. Clone the Project on Local System: (https://github.com/shlok-prakash/Phoenix-Inwarranty-Flow.git)
2. Install Nodejs and NPM from (https://nodejs.org/en)
3. Install Newman using  ```npm install -g newman```
4. Install Newman-reporter-htmlextra  ```npm install -g newman-reporter-htmlextra```
5. Run the Newman Command:
     ```
            newman run 'Inwarranty-flow-Collection.postman_collection.json' \
            -e QA.postman_environment.json \
            -d testdata.csv \
            -r cli,htmlextra \
            --reporter-htmlextra-export ./newman/index.html
     ```
## 🧩 System Design Diagram

### 📌 CI/CD Workflow Architecture

```mermaid
flowchart LR
    A[Trigger: Push / Manual / Cron] --> B[GitHub Actions Workflow]
    B --> C[Checkout Code]
    C --> D[Setup NodeJs ]
    D --> E[Install Newman and Newman-HtmlExtra Reporter]
    E --> F[Run Postman Collection]
    F --> G[Generate HTML Report]
    G --> H[Upload Artifact]
    G --> I[Deploy to GitHub Pages]
    G --> J[Send Email Notification]
    I --> K[Public Report URL]
 ```

## 🔮 Future Enhancements

- Integration with another CI/CD pipeline (Jenkins)  
- Parallel execution of Postman tests  


## 🌟 Show Your Support

If you found this project useful:

- ⭐ Star this repository  
- 🍴 Fork it  
- 📢 Share it  


## 📬 Contact

Feel free to reach out for collaboration or opportunities!
