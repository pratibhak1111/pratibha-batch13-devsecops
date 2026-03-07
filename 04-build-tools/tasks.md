# Module 4 – Tasks | Build Tools (Maven, NPM, Python, .NET)

This module is designed like a real corporate setup:
You will **pull real project repos**, build them using the correct build tools,
connect them to databases, run locally, and deploy.

Complete tasks in sequence.

---

## Task 1 – Setup Build Environment

### Objective
Prepare your machine/VM for building multiple tech stacks.

### What You Need to Do
- Install and verify:
  - Java + Maven
  - Node.js + NPM
  - Python3 + pip + venv
  - .NET SDK
- Create a `module-4-env.md` file listing tool versions

### Deliverables
- Version outputs for all tools
- `module-4-env.md`

### Interview Connect
- Why version consistency matters in builds?

---

## Task 2 – How To Get Project Repos

### Objective
Learn to pull and manage multiple project repositories.

### What You Need to Do
- Create a folder named `module-4-projects/`
- Clone at least 2 repos (one Java and one Node/Python/.NET)
- Add a `repos.md` file listing:
  - Repo name
  - Tech stack
  - Build command

### Deliverables
- `repos.md`
- Clone proof

### Interview Connect
- What’s the difference between cloning vs downloading ZIP?

---

## Task 3 – Build Tools Part-1 (Java + Maven Basics)

### Objective
Build a Java project using Maven.

### What You Need to Do
- Open the Java project repo
- Identify `pom.xml`
- Run:
  - `mvn clean`
  - `mvn test`
  - `mvn package`
- Locate the generated artifact (`.jar/.war`)

### Deliverables
- Build output screenshot/log
- Artifact proof

### Interview Connect
- What is a Maven lifecycle?

---

## Task 4 – Build Tools Part-2 (Node + NPM Basics)

### Objective
Build a Node project using NPM.

### What You Need to Do
- Identify `package.json`
- Run:
  - `npm install`
  - `npm run build` (if available)
  - `npm start` (if available)
- Explain what `node_modules` is

### Deliverables
- Build output
- Running app proof

### Interview Connect
- Why do teams avoid committing node_modules?

---

## Task 5 – Database Setup Document (Common Format)

### Objective
Create a reusable DB setup guide like corporates do.

### What You Need to Do
- Create `database-setup.md` including:
  - MongoDB setup
  - PostgreSQL setup
  - MySQL setup
- Add connection string examples

### Deliverables
- `database-setup.md`

### Interview Connect
- Why teams standardize DB setup docs?

---

# ✅ 3-Tier Projects (Hands-On)

You will run at least **two 3-tier applications** end-to-end.

---

## Task 6 – 3-Tier .NET + MongoDB (Tutorial Run)

### Objective
Run a .NET 3-tier project connected to MongoDB.

### What You Need to Do
- Start MongoDB locally (Docker allowed)
- Configure DB connection in app config
- Build and run the .NET project
- Verify API or UI is working

### Deliverables
- Running proof (logs/screenshots)
- Build command outputs

### Interview Connect
- Why MongoDB is common for document workloads?

---

## Task 7 – 3-Tier Python + Postgres (Tutorial Run)

### Objective
Run a Python 3-tier project connected to PostgreSQL.

### What You Need to Do
- Start PostgreSQL
- Create database and user
- Configure environment variables for DB
- Run migrations (if applicable)
- Run app and verify endpoints

### Deliverables
- DB connection proof
- Running app proof

### Interview Connect
- What is the purpose of migrations?

---

## Task 8 – 3-Tier NodeJS + MySQL (Tutorial Run)

### Objective
Run a NodeJS 3-tier project connected to MySQL.

### What You Need to Do
- Start MySQL
- Create database and user
- Configure DB settings in project
- Install dependencies and start app
- Verify API/UI output

### Deliverables
- MySQL setup proof
- Running app proof

### Interview Connect
- Why environment variables are used for DB configs?

---

# ✅ Local Setup Tasks (Repeatability)

These tasks ensure students can run everything locally cleanly.

---

## Task 9 – Local Setup: Java + MySQL (3-Tier Local)

### Objective
Run Java 3-tier app locally with MySQL.

### What You Need to Do
- Start MySQL
- Configure Java DB connection
- Build with Maven
- Run locally and verify response

### Deliverables
- Build + run proof

### Interview Connect
- What is JDBC URL and why it matters?

---

## Task 10 – Local Setup: NodeJS + MySQL (3-Tier Local)

### Objective
Run NodeJS 3-tier app locally with MySQL.

### What You Need to Do
- Configure Node app DB connection
- Start app and test endpoint

### Deliverables
- Running proof

### Interview Connect
- What is the role of ORM libraries?

---

## Task 11 – Local Setup: .NET + MongoDB (3-Tier Local)

### Objective
Run .NET app locally with MongoDB repeatably.

### What You Need to Do
- Create a `.env` or config file
- Run app locally and verify

### Deliverables
- Config file example (without secrets)

### Interview Connect
- How do you manage secrets in production?

---

## Task 12 – Local Setup: Python + Postgres (3-Tier Local)

### Objective
Run Python app locally with Postgres repeatably.

### What You Need to Do
- Create Python virtualenv
- Install dependencies from requirements
- Start app and verify

### Deliverables
- `requirements-freeze.txt` (pip freeze output)
- Running proof

### Interview Connect
- Why virtual environments are mandatory?

---

# ✅ Monitoring Projects (Per Stack)

---

## Task 13 – Java Monitoring Project

### Objective
Build and run the Java monitoring project.

### What You Need to Do
- Build with Maven
- Run locally
- Verify monitoring endpoint or logs

### Deliverables
- Build/run output

### Interview Connect
- Why monitoring endpoints matter?

---

## Task 14 – NodeJS Monitoring Project

### Objective
Build and run the Node monitoring project.

### What You Need to Do
- Install dependencies
- Run and verify output

### Deliverables
- Run proof

### Interview Connect
- How do you monitor Node apps in production?

---

## Task 15 – Python Monitoring Project

### Objective
Build and run the Python monitoring project.

### What You Need to Do
- Setup venv
- Install deps
- Run and verify

### Deliverables
- Run proof

### Interview Connect
- What is application health check?

---

# ✅ Deployments & Web Servers

---

## Task 16 – Deploy to Tomcat (Manual)

### Objective
Deploy a Java WAR manually to Tomcat.

### What You Need to Do
- Install Tomcat
- Build WAR file
- Deploy WAR to Tomcat webapps
- Verify app is accessible in browser

### Deliverables
- WAR build proof
- Running application proof

### Interview Connect
- WAR vs JAR?

---

## Task 17 – Tomcat Sample Project with Steps

### Objective
Understand deployment workflow clearly.

### What You Need to Do
- Use the sample project files
- Repeat the Tomcat deployment steps
- Document deployment commands in `tomcat-deploy-notes.md`

### Deliverables
- `tomcat-deploy-notes.md`

### Interview Connect
- How do you debug Tomcat deployment failures?

---

## Task 18 – Nginx Web Server with 3 Real Projects

### Objective
Host multiple apps behind Nginx like real production.

### What You Need to Do
- Install Nginx
- Configure reverse proxy for:
  - One Java app
  - One Node app
  - One Python app
- Use 3 different paths or subdomains
- Restart Nginx and verify routing

### Deliverables
- Nginx config file
- Proof of routing working

### Interview Connect
- Reverse proxy vs load balancer?

---

## Task 19 – Nginx Real World Project Notes

### Objective
Document the setup like corporate teams do.

### What You Need to Do
- Create `nginx-notes.md` containing:
  - Config explanation
  - How to reload
  - Common errors and fixes

### Deliverables
- `nginx-notes.md`

### Interview Connect
- How do you troubleshoot 502/504 errors in Nginx?

---

# ✅ Notes & Documentation

---

## Task 20 – Module-4 Notes & Documentation

### Objective
Create a single place for Module-4 learning.

### What You Need to Do
Create a `notes-module-4.md` including:
- Maven build flow
- NPM build flow
- Python build + venv flow
- .NET build flow
- Common build errors + fixes

### Deliverables
- `notes-module-4.md`

### Interview Connect
- What are the most common build failures?

---

## 🌍 Learn in Public (Mandatory)

After completing Module-4:

1. Push your work to your forked GitHub repo  
2. Post on LinkedIn:
   - What stack you built
   - What broke during builds
   - How you fixed it
3. Tag:
   - **Aditya Jaiswal**
   - **DevOps Shack**

Once tagged, your **repo and tasks will be reviewed**.

Suggested hashtags:
```
#Batch13 #BuildTools #Maven #NPM #DotNet #Python #DevOps #LearnInPublic #devopsshack
```

---

## 🎯 Outcome of Module-4

After completing this module, you will be able to:
- Build apps across Java/Node/Python/.NET
- Connect apps with real databases
- Deploy Java apps to Tomcat
- Configure Nginx reverse proxy for multiple applications
- Troubleshoot real-world build and deployment issues

