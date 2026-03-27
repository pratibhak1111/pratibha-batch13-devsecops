# Module 8 – Tasks | Nexus Artifact Management

This module simulates how teams manage build artifacts and container images in real environments.

You will:

- Setup Nexus  
- Publish artifacts  
- Consume artifacts in pipelines  
- Configure Docker registry  
- Work with versioning and repositories  

Complete tasks in sequence.

---

## Task 1 – Nexus Setup

**Objective**

Install and run Nexus.

**What You Need to Do**

- Run Nexus using Docker or VM  
- Access UI in browser  
- Set admin password  

**Deliverables**

- Nexus dashboard access proof  

**Interview Connect**

- What is Nexus used for  

---

## Task 2 – Understand Nexus Concepts

**Objective**

Learn core components.

**What You Need to Do**

Explore:

- Hosted repositories  
- Proxy repositories  
- Group repositories  

Create `nexus-basics.md` explaining these

**Deliverables**

- nexus-basics.md  

**Interview Connect**

- Difference between hosted and proxy repo  

---

## Task 3 – Create Repositories

**Objective**

Setup repositories.

**What You Need to Do**

Create:

- Maven hosted repo  
- NPM hosted repo  
- Docker hosted repo  

**Deliverables**

- Repository setup proof  

**Interview Connect**

- Why multiple repo types are needed  

---

## Task 4 – Publish Node.js Artifact to Nexus

**Objective**

Store Node package.

**What You Need to Do**

- Configure .npmrc  
- Publish package to Nexus  
- Verify in UI  

**Deliverables**

- Published package proof  

**Interview Connect**

- Why private npm registry is used  

---

## Task 5 – Publish Java Artifact to Nexus

**Objective**

Store Maven artifact.

**What You Need to Do**

- Configure pom.xml  
- Setup distribution management  
- Run Maven deploy  

**Deliverables**

- Artifact in Nexus  

**Interview Connect**

- Difference between install and deploy  

---

## Task 6 – Download Artifacts from Nexus

**Objective**

Consume stored artifacts.

**What You Need to Do**

- Configure project to pull from Nexus  
- Install dependencies  

**Deliverables**

- Dependency download proof  

**Interview Connect**

- Why artifact reuse is important  

---

## Task 7 – Nexus in CI/CD Pipeline

**Objective**

Use Nexus in pipelines.

**What You Need to Do**

Update pipeline to:

- Build app  
- Publish artifact to Nexus  

**Deliverables**

- Pipeline logs  

**Interview Connect**

- Why artifact storage is needed in CI/CD  

---

## Task 8 – Versioning Strategy

**Objective**

Manage artifact versions.

**What You Need to Do**

- Publish multiple versions  

Use version naming:

- snapshot  
- release  

**Deliverables**

- Multiple versions in repo  

**Interview Connect**

- Snapshot vs release  

---

## Task 9 – Proxy Repository Setup

**Objective**

Cache external dependencies.

**What You Need to Do**

- Create proxy repo (npm/maven)  
- Configure project to use it  

**Deliverables**

- Cached dependency proof  

**Interview Connect**

- Why proxy repos improve performance  

---

## Task 10 – Repository Group Setup

**Objective**

Simplify repository access.

**What You Need to Do**

- Create group repo  
- Combine hosted + proxy  
- Use group URL in project  

**Deliverables**

- Group repo usage proof  

**Interview Connect**

- Why group repositories are used  

---

## Task 11 – Private Docker Registry Setup

**Objective**

Use Nexus for container images.

**What You Need to Do**

- Create Docker hosted repo  
- Configure Docker login  
- Push image to Nexus  

**Deliverables**

- Image in Nexus  

**Interview Connect**

- Why private registries are used  

---

## Task 12 – Pull Docker Image from Nexus

**Objective**

Consume private images.

**What You Need to Do**

- Pull image from Nexus  
- Run container  

**Deliverables**

- Running container proof  

**Interview Connect**

- Difference between Docker Hub and private registry  

---

## Task 13 – Secure Nexus Access

**Objective**

Manage authentication.

**What You Need to Do**

- Create users and roles  
- Assign permissions  

**Deliverables**

- Role configuration proof  

**Interview Connect**

- Why access control is needed  

---

## Task 14 – Cleanup and Retention Policy

**Objective**

Manage storage.

**What You Need to Do**

- Configure cleanup policies  
- Remove old artifacts  

**Deliverables**

- Policy configuration  

**Interview Connect**

- Why artifact cleanup is important  

---

## Task 15 – Multi-Project Artifact Flow

**Objective**

Simulate real usage.

**What You Need to Do**

- Build two projects  
- Publish artifacts  
- Consume one in another  

**Deliverables**

- End-to-end flow proof  

**Interview Connect**

- How microservices use artifacts  

---

## Task 16 – Notes and Documentation

**Objective**

Consolidate learning.

**What You Need to Do**

Create `notes-module-8.md` including:

- Nexus workflow  
- Repository types  
- Docker registry setup  
- Common issues and fixes  

**Deliverables**

- Notes file  

**Interview Connect**

- Explain artifact lifecycle  

---

## Learn in Public

After completing this module:

Share:

artifacts published  

pipelines used  

Docker registry setup  

Suggested tags:

#Batch13 #Nexus #ArtifactManagement #DevOps #Docker #CI_CD #LearnInPublic

---

## Outcome of Tasks

After completing these tasks, you will be able to:

- Manage artifacts using Nexus  
- Publish and consume artifacts in pipelines  
- Work with versioning and repositories  
- Configure private Docker registry  
- Apply artifact management in real workflows  