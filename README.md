# Azure Function JS CI/CD 

This repository contains a simple Azure Function written in JavaScript and configured with a full CI/CD pipeline using **Azure DevOps**.

## 📂 Project Structure

```
azure-function-js-ci-cd/
├── src/functions/
│   └── HelloFunction.js     # Main Azure HTTP trigger function
├── azure-pipelines.yml      # CI/CD Pipeline definition
├── package.json             # Node.js project metadata
```

##  Technologies Used

- **Azure Functions** (JavaScript)
- **Azure DevOps Pipelines** (CI/CD)
- **GitHub** (source control)
- **Node.js 18+**

## Function Details

The function `HelloFunction.js` returns a friendly greeting:

```bash
GET https://<your-function-app>.azurewebsites.net/api/HelloFunction?name=John

Response: { "body": "Hello, John!" }
```

If no name is passed, it defaults to `"Hello, world!"`.

##  CI/CD Pipeline

The pipeline is defined in [`azure-pipelines.yml`](./azure-pipelines.yml) and includes:

- **Build Stage** – Install dependencies
- **Test Stage** – Simulated test step
- **Deploy Stage** – Deploys to Azure Function App

> Pipeline triggers on every commit to the `master` branch.

## How to Run Locally

```bash
npm install
func start
```

> Make sure you have the [Azure Functions Core Tools](https://learn.microsoft.com/azure/azure-functions/functions-run-local) installed.

##  Contact

Maintained by [Puneet Mishra](mailto:puneetnow9@gmail.com)

---

Project created for academic purposes as part of a DevOps CI/CD learning activity.
