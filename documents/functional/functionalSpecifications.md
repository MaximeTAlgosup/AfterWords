# Functional Specification Document - AfterWords <!-- omit in toc -->

<details>
<summary> Table Of Contents </summary>

- [1. Introduction](#1-introduction)
  - [1.1. Project Overview](#11-project-overview)
  - [1.2. Project Definition](#12-project-definition)
    - [1.2.1. Vision](#121-vision)
    - [1.2.2. Objectives](#122-objectives)
    - [1.2.3. Scope](#123-scope)
      - [1.2.3.1. In-scope](#1231-in-scope)
      - [1.2.3.2. Out-of-scope](#1232-out-of-scope)
    - [1.2.4. Target Audience](#124-target-audience)
    - [1.2.5. Deliverables](#125-deliverables)
  - [1.3. Project Organisation](#13-project-organisation)
    - [1.3.1. Project Representatives](#131-project-representatives)
    - [1.3.2. Stakeholders](#132-stakeholders)
    - [1.3.3. Project Reviewers](#133-project-reviewers)
  - [1.4. Project Plan](#14-project-plan)
    - [1.4.1. Retroplanning](#141-retroplanning)
    - [1.4.2. Milestones](#142-milestones)
    - [1.4.3. Dependencies](#143-dependencies)
    - [1.4.4. Assumptions/Constraints](#144-assumptionsconstraints)
    - [1.4.5. Risks/Mitigation](#145-risksmitigation)
- [2. Use Cases and Personas](#2-use-cases-and-personas)
  - [2.1. Use Cases](#21-use-cases)
    - [2.1.1. Creating A New Account](#211-creating-a-new-account)
    - [2.1.2. Select Instances](#212-select-instances)
    - [2.1.3. Uploading Documents](#213-uploading-documents)
    - [2.1.4. Send Letters To All Instances](#214-send-letters-to-all-instances)
  - [2.2. Personas](#22-personas)
    - [2.2.1. Persona 1: Janice LeBlanc](#221-persona-1-janice-leblanc)
    - [2.2.2. Persona 2: Sean McPhil](#222-persona-2-sean-mcphil)
    - [2.2.3. Persona 3: Alexandre Moutarde](#223-persona-3-alexandre-moutarde)
- [3. Design](#3-design)
  - [3.1. Wireframes](#31-wireframes)
    - [3.1.1. Redirection Page](#311-redirection-page)
    - [3.1.2. Mourners Side](#312-mourners-side)
      - [3.1.2.1. Login Section](#3121-login-section)
      - [3.1.2.2. Home Section](#3122-home-section)
      - [3.1.2.3. Profile Section](#3123-profile-section)
      - [3.1.2.4. Instance Section](#3124-instance-section)
      - [3.1.2.5. Letters Section](#3125-letters-section)
      - [3.1.2.6. Undertaker Section](#3126-undertaker-section)
      - [3.1.2.7. Procedure Section](#3127-procedure-section)
    - [3.1.3. Undertakers Side](#313-undertakers-side)
      - [3.1.3.1. Login Section](#3131-login-section)
      - [3.1.3.2. Home Section](#3132-home-section)
      - [3.1.3.3. Profile Section](#3133-profile-section)
      - [3.1.3.4. Clients Section](#3134-clients-section)
      - [3.1.3.5. Employees Section](#3135-employees-section)
    - [3.1.4. Administrator Side](#314-administrator-side)
      - [3.1.4.1. Login Section](#3141-login-section)
      - [3.1.4.2. Home Section](#3142-home-section)
      - [3.1.4.3. Application Section](#3143-application-section)
      - [3.1.4.4. Undertakers Section](#3144-undertakers-section)
      - [3.1.4.5. Mourners Section](#3145-mourners-section)
      - [3.1.4.6. Profile Section](#3146-profile-section)
  - [3.2. Mockups](#32-mockups)
    - [3.2.1. Redirection Page](#321-redirection-page)
    - [3.2.2. Mourners Side](#322-mourners-side)
      - [3.2.2.1. Login Section](#3221-login-section)
      - [3.2.2.2. Home Section](#3222-home-section)
      - [3.2.2.3. Profile Section](#3223-profile-section)
      - [3.2.2.4. Instance Section](#3224-instance-section)
      - [3.2.2.5. Letters Section](#3225-letters-section)
      - [3.2.2.6. Undertaker Section](#3226-undertaker-section)
      - [3.2.2.7. Procedure Section](#3227-procedure-section)
    - [3.2.3. Undertakers Side](#323-undertakers-side)
      - [3.2.3.1. Login Section](#3231-login-section)
      - [3.2.3.2. Home Section](#3232-home-section)
      - [3.2.3.3. Profile Section](#3233-profile-section)
      - [3.2.3.4. Clients Section](#3234-clients-section)
      - [3.2.3.5. Employees Section](#3235-employees-section)
    - [3.2.4. Administrator Side](#324-administrator-side)
      - [3.2.4.1. Login Section](#3241-login-section)
      - [3.2.4.2. Home Section](#3242-home-section)
      - [3.2.4.3. Application Section](#3243-application-section)
      - [3.2.4.4. Undertakers Section](#3244-undertakers-section)
      - [3.2.4.5. Mourners Section](#3245-mourners-section)
      - [3.2.4.6. Profile Section](#3246-profile-section)
  - [3.3. Color Palette](#33-color-palette)
  - [3.4. Logo](#34-logo)
  - [3.5. Font](#35-font)
- [4. Functional Requirements](#4-functional-requirements)
  - [4.1. User Roles And Permissions](#41-user-roles-and-permissions)
    - [4.1.1. Administrator](#411-administrator)
    - [4.1.2. Undertakers](#412-undertakers)
    - [4.1.3. Mourners](#413-mourners)
  - [4.1.4. System Features And Functions](#414-system-features-and-functions)
  - [4.1.5. Application Workflow](#415-application-workflow)
- [5. Non-Functional Requirement](#5-non-functional-requirement)
  - [5.1. Security](#51-security)
  - [5.2. Responsiveness](#52-responsiveness)
  - [5.3. Performance](#53-performance)
  - [5.4. Connectivity](#54-connectivity)
  - [5.5. Marketing](#55-marketing)
- [6. Data](#6-data)
  - [6.1. Templates](#61-templates)
  - [6.2. Documents To Obtain](#62-documents-to-obtain)
  - [6.3. Urgent Procedure (In The Week Following The Death)](#63-urgent-procedure-in-the-week-following-the-death)
  - [6.4. No Urgent Procedure (Within Six Months After Death)](#64-no-urgent-procedure-within-six-months-after-death)
  - [G.5. Tags](#g5-tags)
- [7. External Interfaces](#7-external-interfaces)
- [8. Constraints And Limitations](#8-constraints-and-limitations)
- [9. Appendices](#9-appendices)
  - [9.1. Glossary](#91-glossary)
  - [9.2. Resources](#92-resources)

</details>

## 1. Introduction

### 1.1. Project Overview

---

This project is made to help mourners with the french administration system. It would be delivered to undertakers which will deliver it to mourners.

This project is held by Maxime THIZEAU.

---

### 1.2. Project Definition

---

#### 1.2.1. Vision

Afterwords is an application allowing mourning people to get some help on the administration part. \
It would ease the process by gathering all instances in one place. \
How would that work?
The mourner just have to enter all the different instances and the required documents. Once it would be done, they would have to complete some templates of letters to send them all in one click.

---

#### 1.2.2. Objectives

---

The objectives of this project are pretty clear:

- Centralizing mourners in one platform.
- Helping mourners comnpleting french administration.
- Allowing mourners to have information gathered on one website.

---

#### 1.2.3. Scope

##### 1.2.3.1. In-scope

---

AfterwWords will cover the different subject hereunder:

- It will suggest many letters template, allowing users to have a wider range of choice to complete and write there own letters.
- It will also gather french instances (such as EDF, France connect, ...) in one place.
- Users can chose the intended instances by checking their names within a page.
- AfterWords would have a database to store all the necessary documents for the said instances above.
- AfterWords would save time and energy to mourners.

---

##### 1.2.3.2. Out-of-scope

---

The following points are what AfterWords will not do:

- AfterWords won't display user's information withinvthe application.
- It would not do administartion procedures for the user.
- It won't dispose of a messagerie within the application, the user will need to have an e-mail address of there own.
- Users can't organize funerals within the application.

---

#### 1.2.4. Target Audience

AfterWords will have to target audience. \
The first hand audience would be undertakers company. AfterWords would be a service they could share, sell to their own customers, the second and final target audience of AfterWords, mourning people.

The mourning people are the main audience of this project. AfterWords is meant to help them through a difficult pass which is grieving. However, AfterWords won't be accessible on Internet in free-access. It would be unseen, that's why undertakers have a key role in this project.

---

#### 1.2.5. Deliverables

---

This project don't have a lot of deliverables. They are only composed of the code source and docuents that have to be written.

For the documents, there would be:

- The Functional Specifications.
- The Technical Specifications.
- The Test Plan.
- Test Cases.
- The User Manual.
- Management Artifacts.

The code source could be find in the `src` folder at the root of the project.

---

### 1.3. Project Organisation

---

#### 1.3.1. Project Representatives

---

This project has only one representatives which is Maxime THIZEAU, he would hold every role that a team could possibly have. However, here are the main ones:

| Role              | Description                                                                                                                          |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| Project Manager   | Managment (time, resources)<br>Workload distribution<br> Report to stakeholders<br>Risk anticipation and mitigation                  |
| Program Manager   | Mock-ups and general design of the software<br>Communication with the client<br>Functional specification delivery<br>Risk management |
| Technical Leader  | Define coding conventions<br>Choose technical tools used<br>Technical specification delivery<br>Manages developer tasks              |
| Software engineer | Write the code<br>Fix bugs<br>Document the code<br>Create the tests if needed for the code                                           |
| Quality assurance | Verify documents<br>Test the program<br>Confirm we match the client expectations<br>Test plan delivery                               |
| Technical Writter | Put itself in user shoes<br>User manual delivery                                                                                     |

---

#### 1.3.2. Stakeholders

---

| Role            | Representative           | Expectation                                                              |
| --------------- | ------------------------ | ------------------------------------------------------------------------ |
| owner           | Maxime THIZEAU           | Finished project while meeting requirements and proof-tested version one |
| School director | Franck JEANNIN (ALGOSUP) | Clear documentation and management based on the skills learnt in class   |

---

#### 1.3.3. Project Reviewers

---

This project would be reviewed by other developpers and ALGOSUP students. Moreover, you could be part of the review team by opening an issue on this repository and by following the [CONTRIBUTING document](../../CONTRIBUTING.md).

The main reviewers would be:

| Name            | Role                                                 | Personal Links                                                                                             | Company Links                                                                                                                          |
| --------------- | ---------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| Evan UHRING     | Woopsie Creations Co-founder and ACS Founder         | [GitHub](https://github.com/FlouffyDaWolf)                                                                 | [Woopsie Creation GitHub](https://github.com/woopsie-creations)                                                                        |
| Enzo GUILOUCHE  | Woopsie Creations Co-founder and SeismoSense Founder | [GitHub](https://github.com/EnzoGuillouche) \| [LinkedIn](https://www.linkedin.com/in/enzoguillouche/)     | [Woopsie Creation GitHub](https://github.com/woopsie-creations) \| [SeismoSense GitHub](https://github.com/EnzoGuillouche/SeismoSense) |
| Lucas MEGNAN    | Tomodachi Sport Founder                              | [GitHub](https://github.com/LucasMegnan) \| [LinkedIn](https://www.linkedin.com/in/lucas-megnan/)          | [Tomodachi Sport](https://github.com/LucasMegnan/Tomodachi-Sport)                                                                      |
| Antoine PREVOST | Inkom Founder and CEO                                | [GitHub](https://github.com/TechXplorerFR) \| [LinkedIn](https://www.linkedin.com/in/antoine-prevost-dev/) | [Inkom](https://inkom.ai) \| [Inkom LinkedIn](https://www.linkedin.com/company/in-kom/)                                                |

---

### 1.4. Project Plan

---

#### 1.4.1. Retroplanning

---

**End Goal and Deadline**:

The project should be done (version one) before June, 2026.

**Key Milestones**:

- The Version one should be completed by the 15 of May, 2026.
- The MVP should be completed before the end of September, 2025.
- The Functional Specifications should be done by the end of July, 2025.

**Task Breakdown**:

- The Oral Presentation will be completed by the end of June, 2026.
- The User Manual will be written by the end of May, 2026
- The application would be in its first version by the end of April, 2026.
- The last Test Report will be done and written on the 12 of April, 2026.
- The Admin side of the product would be completed on the 5 of April, 2026.
- The Undertaker side would be completed by the end of February, 2026.
- The Test Plan and Test Cases would be created and completed early December, 2025.
- The MVP should be coded before October 19th, 2025.
- The Mourner Side of the application should be finished current September, 2025.
- The Technical Specification should be finished by the start of August, 2025.
- The Functional Specification should be written before July 12th, 2025.
- The Figma should be designed before the end of June, 2025.
- The Wireframe should be done before the end of June, 2025.

**Critical Path**:

This project has many critical tasks which are:

- Each side of the application (Mourners, Undertakers, Admin).
- The Technical Specifiaction.

**Timeline Visualization**:

The Gantt Chart could be seen in the [Management Artifacts Document](../management/managementArtifacts.md).

---

#### 1.4.2. Milestones

---

| Date       | Milestones                        |
| ---------- | --------------------------------- |
| 07/12/2025 | Functional Specification Delivery |
| 08/05/2025 | Technical Specification Delivery  |
| 10/19/2025 | MVP Release                       |
| 12/03/2025 | Test Plan Delivery                |
| 12/03/2025 | Test Cases Delivery               |
| 04/25/2026 | Version One Release               |
| 05/27/2026 | User Manual Delivery              |
| 05/30/2026 | Management Artifacts Delivery     |
| 06/20/2026 | Oral Presentation Delivery        |

---

#### 1.4.3. Dependencies

---

**Task Dependencies**:

- The Functional Specification would be only completed once the Figma (design) and Excalidraw (Wireframe) would be entirely done.
- The Last Testing phase will start only after the first version is completed.
- The First Version of the application would need all three sides to be completed.

**Resource Dependencies**:

- All resources will be available at any point in the project since only one person complete every role.
- Reviewers will be required on different testing phases lasting one to two weeks after every code advancement (Mourner Side, MVP, Undertakers Side, Admin Side).

---

#### 1.4.4. Assumptions/Constraints

---

**Assumptions**:

- The team assume undertakers would spead the application as much as possible in their clients.
- The team assume the application will be used only by mourners having an account.
- The team assume deadlines will be met.
- The team assume connection will be provided by the client.
- The team assume mourners will have all necessary documents.
- The team assume Undertakers and client will respect the code of concuct.

**Constraints**:

- The application needs to be connected to internet.
- The application can't reach out mourners without passing by undertakers.
- The application won't be used by everyone.
- The application isn't free.
- The application should be developped in a short periiod of time.
- The team power is low.

---

#### 1.4.5. Risks/Mitigation

---

| Type             | Description                                                    | Likelihood | Impact                                                      | Mitigation                                                                 |
| ---------------- | -------------------------------------------------------------- | ---------- | ----------------------------------------------------------- | -------------------------------------------------------------------------- |
| Sickness         | A team member becomes sick.                                    | High       | The project won't be updated while the team member is sick. | Planned more time than necessary to still be on track in case of sickness. |
| No user          | AfterWords is not appealing enough to consumers.               | Low        | The Product won'y be selled and the project obsolete.       | Having an important and efficient marketing campaign.                      |
| Data Leak        | The database leak and private information is lost on internet. | Medium     | AfterWords will lost undertakers and mourners trust.        | Having a solid data privacy and security on the database.                  |
| Unfunctional API | An API is not accessible from the application.                 | High       | This instance won't be accessible from the application.     | Finding another way to send and retrieve data from them.                   |

---

## 2. Use Cases and Personas

### 2.1. Use Cases

<!-- TODO: Add Use Cases, at least 2. And verify accuracy of already existing ones. -->

#### 2.1.1. Creating A New Account

---

**Actor**: undertakers \
**Goal**: user wants to create an account

**Preconditions**:

- User is logged in.
- User is in the `New Account Page`.
- User has all needed mourner's personal information.

**Basic Flow**:

1. Click on `New Account`.
2. Enter deceased personal information (death date, full name, last location, birth date, birth location).
3. Enter Mourner personal information (parenthood, full name).
4. Confirm.

> [!Warning]
> Alternate Flows:
>
> - The deceased already have an account.
> - Failed due to missing information.

**Postconditions**:

- AfterWords generate a password.
- Undertaker transmit account and password to mourner.

---

#### 2.1.2. Select Instances

---

**Actor**: mourner \
**Goal**: user wants to contact instances

**Preconditions**:

- User is logged in.
- User is in the `Instance Page`.

**Basic Flow**:

1. Search for instance name in search bar.
2. Click the checkbox to add it to `Instance to contact`.
3. Repeat the process for every instance.

> [!Warning]
> Alternate Flows:
>
> Instance not registered

**Postconditions**:

- Instance saved in `Instance to contact`.

---

#### 2.1.3. Uploading Documents

---

**Actor**: mourner \
**Goal**: user wants to upload documents for procedure.

**Preconditions**:

- User is logged in.
- User is in the `Your Documents Page`.

**Basic Flow**:

1. Open a teb with all your documents locally.
2. Select the documents you want to upload.
3. Drag & drop them into the `Document container`.
4. Confirm the upload.

> [!Warning]
> Alternate Flows:
>
> - The document the user want to upload already is uploaded.
> - No document given to the `Document container`.

**Postconditions**:

- Documents saved within your account.

---

#### 2.1.4. Send Letters To All Instances

---

**Actor**: mourner \
**Goal**: user wants to inform instances of a death

**Preconditions**:

- User is logged in.
- User is in the `Letter Page`.
- User has selected the intended instances.
- User has uploaded necessary documents.

**Basic Flow**:

1. Select a category.
2. Select a template.
3. Complete blank space with personal information.
4. Confirm.

> [!Warning]
> Alternate Flows:
>
> - Blank space empty.
> - Failed due to lack of document.
> - Failed due to unprecised/no instance.

**Postconditions**:

- Letter sent to the instance via mail.

---

### 2.2. Personas

---

#### 2.2.1. Persona 1: Janice LeBlanc

---

**Name**: Janice LeBlanc

**Age Range**: 60-90

**Frustrations**:

- Can't understand how the administration system works anymore.
- Don't know how to contact efficeietnly all of the instances needed for procedures.
- Would rather spend time with her family than doing papers.

**Goals**:

- Wants to finalize all the procedure in a shorter amount of time.
- Wants to lose less time doing procedures.
- Should understand how to do it on internet.

---

#### 2.2.2. Persona 2: Sean McPhil

---

**Name**: Sean McPhil

**Age Range**: 35-55

**Frustrations**:

- Can't help the mourners coming to his company efficiently enough.
- Already saw people struggling completing procedural papers.
- Can't complete the work for mourners in need.

**Goals**:

- Would like to add mourners on a single application that helps them completing procedures.
- Would like to add other employees to it to have some help.
- Would like to complete procedure for those who wants it.

---

#### 2.2.3. Persona 3: Alexandre Moutarde

---

**Name**: Alexandre Moutarde

**Age Range**: 25-45

**Frustrations**:

- Don't know all the procedures needed.
- Can't pass much time with his family due to the amount of work.
- have enough to search for every instance needed.

**Goals**:

- Would like a documented application to help him.
- Would like to spend more time grieving than doing paperworks.
- Would like having a list of steps guiding him across the procedure.

---

## 3. Design

### 3.1. Wireframes

---

The application would be parted in three different parts, for mourners, undertakers, and administrators. Therefore, more page has been designed for all of them.

This section will start with the common redirection page and then will go through each side independently.

The wireframe (Excalidraw) can also be access as raw file in the [Design Folder](./design/designAfterWords.excalidraw).

---

#### 3.1.1. Redirection Page

---

The Redirection Page will be accessible from everyone and would look like this:

![Redirection Page Picture](./img/wireframe/redirectionPage.png)

---

#### 3.1.2. Mourners Side

---

Once the user has clicked on the Mourner button, they would be redirected on this section of the application. It would be composed of many sections which are:

- [Login](#3121-login-section)
- [Home](#3122-home-section)
- [Profile](#3123-profile-section)
- [Instance](#3124-instance-section)
- [Letters](#3125-letters-section)
- [Undertaker](#3126-undertaker-section)
- [Procedure](#3127-procedure-section)

Each of those are accessible below or you can click on them to be redirected instantly to the intended section description.

---

##### 3.1.2.1. Login Section

---

This section is composed of those pages:

| Name         | Complement | Description                                                             |
| ------------ | ---------- | ----------------------------------------------------------------------- |
| Welcome Page | /          | This page is designed to welcome users into the application.            |
| Login Page   | /          | This section ask for a first name, last name, and password to the user. |
| Login Page   | Error      | Showcase potential error handling on the login page.                    |

It would look like this:

![Login Section Mourners Picture](./img/wireframe/mourners/loginSection.png)

---

##### 3.1.2.2. Home Section

---

**Pages**:

| Name      | Complement | Description                                                                                          |
| --------- | ---------- | ---------------------------------------------------------------------------------------------------- |
| Home Page | /          | Center of the navigation between all pages. it also display basic information about the app/mourner. |

**Visuals**:

![Home Section Mourners Picture](./img/wireframe/mourners/homeSection.png)

---

##### 3.1.2.3. Profile Section

---

**Pages**:

| Name            | Complement                     | Description                                                                                      |
| --------------- | ------------------------------ | ------------------------------------------------------------------------------------------------ |
| Profile Page    | Without Document               | Display information about user and deceased as well as an empty list of documents.               |
| Profile Page    | With Document                  | Display information about user and deceased as well as a list of documents.                      |
| Profile Pop-up  | Verification                   | Pop-up to double check before leaving the page.                                                  |
| Document Pop-up | Cancel                         | Pop-up to double check exiting the document addition.                                            |
| Document Pop-up | Phase 1 - Empty                | Pop-up with all the list of documents you need to add to your profile. The list is empty.        |
| Document Pop-up | Phase 1 - In Validation        | Appears when a document is valid and you you haven't close the pop-up.                           |
| Document Pop-up | Phase 1 - Validated            | Appears when a document is valid and after opening the pop-up a second time.                     |
| Document Pop-up | Phase 2                        | Pop-up to add documents via drag and drop or file explorer.                                      |
| Document Pop-up | Phase 2 - Error                | Pop-up displaying an error on the type of document.                                              |
| Document Pop-up | Phase 2 - New Document         | Pop-up with a form to complete to add a document which is not predefined within the application. |
| Document Pop-up | Phase 2 - New Document - Error | Pop-up displaying an error of type or field.                                                     |

**Visuals**:

![Profile Section Mourners Picture](./img/wireframe/mourners/profileSection.png)

---

##### 3.1.2.4. Instance Section

---

**Pages**:

| Name            | Complement             | Description                                                     |
| --------------- | ---------------------- | --------------------------------------------------------------- |
| Instance Page   | Your Instances         | Displays Instances linked to the account.                       |
| Instance Page   | Your Instances - Empty | Page to add instances when none are linked to the account.      |
| Instance Pop-up | Verification           | Pop-up to double check if the user wants to remove an instance. |
| Instance Page   | Add Instances          | Page listing all the instances.                                 |
| Instance Page   | Search                 | Page with a filtered list of instances following user choices.  |
| Instance Page   | No Result              | Page when no instances match filters.                           |
| Tags Pop-up     | /                      | Pop-up with all the tags related to instances.                  |
| Instance Page   | Instance Info          | Description of the instance the user clicked on.                |

**Visuals**:

![Instance Section Mourners Picture](./img/wireframe/mourners/instanceSection.png)

---

##### 3.1.2.5. Letters Section

---

**Pages**:

| Name            | Complement                 | Description                                                                                                |
| --------------- | -------------------------- | ---------------------------------------------------------------------------------------------------------- |
| Letters Page    | Your Letters               | Display list of needed letter templates to fill and letters already selected.                              |
| Letters Pop-up  | Verification               | Double check before removing a letter.                                                                     |
| Letters Page    | Select Letters Template    | Slideshow with all the letters corresponding to one kind of instance.                                      |
| Letters Page    | Template Creation          | Form to complete to create a brand new template.                                                           |
| Letters Page    | Template Creation - Errors | Form not valid, showcase errors.                                                                           |
| Letters Page    | Your Template              | Page to view a template already selected.                                                                  |
| Template Pop-up | Preview                    | Page to view the template while in creation.                                                               |
| Template Pop-up | Import                     | Pop-up to drag and drop an already existing template, could also find if through file explorer navigation. |
| Template Pop-up | Import - Error             | The document is not in the good format/empty.                                                              |

**Visuals**:

![Letters Section Mourners Picture](./img/wireframe/mourners/lettersSection.png)

---

##### 3.1.2.6. Undertaker Section

---

**Pages**:

| Name            | Complement              | Description                                                                                     |
| --------------- | ----------------------- | ----------------------------------------------------------------------------------------------- |
| Undertaker Page | Your Undertaker Company | Description of the company containing description, words to mourners, and way of communication. |

**Visuals**:

![Undertaker Section Mourners Picture](./img/wireframe/mourners/undertakerSection.png)

---

##### 3.1.2.7. Procedure Section

---

**Pages**:

| Name             | Complement                  | Description                                                                                        |
| ---------------- | --------------------------- | -------------------------------------------------------------------------------------------------- |
| Procedure Page   | Introduction                | Describes all the steps the user will need to complete through the procedure.                      |
| Procedure Page   | Step 1                      | Page to complete all templates for each instances.                                                 |
| Procedure Page   | Step 1 - Completed          | Page when a template is validated.                                                                 |
| Procedure Page   | Step 1 - Error              | Page when templates are not completed yet.                                                         |
| Procedure Page   | Template Completion         | Page with the template and inputs to field missing parts of the template.                          |
| Procedure Page   | Template Completion - Error | When an input is empty, will appear with a red stroke.                                             |
| Procedure Page   | Step 2                      | Same as step 1 for another type of instances.                                                      |
| Procedure Page   | Step 3                      | Same as step 1 for another type of instances.                                                      |
| Procedure Page   | Step 4                      | Same as step 1 for another type of instances.                                                      |
| Procedure Page   | Step 5                      | Finalization step, the user needs to validate the procedure to send emails.                        |
| Procedure Page   | Step 5 - Yes                | Finalization step, same as above. The user can write feedback about AfterWords and/or undertakers. |
| Procedure Pop-up | Validation                  | Double check before sending emails to all instances.                                               |
| Procedure Page   | Last Step                   | Showed to inform the procedure is completed.                                                       |

**Visuals**:

![Procedure Section Mourners Picture](./img/wireframe/mourners/procedureSection.png)

---

#### 3.1.3. Undertakers Side

---

As for the mourners, by clicking on the undertaker button, the user will be redirected into this side of the application. \
This one would be composed of the following sections:

- [Login](#3131-login-section)
- [Home](#3132-home-section)
- [Profile](#3133-profile-section)
- [Clients](#3134-clients-section)
- [Employees](#3135-employees-section)

Each of those are written under and can be access threw the links above.

---

##### 3.1.3.1. Login Section

---

**Pages**:

| Name         | Complement | Description                                          |
| ------------ | ---------- | ---------------------------------------------------- |
| Welcome Page | /          | Display of text to welcome user in.                  |
| Login Page   | /          | Form to fill when the user already have an account.  |
| Login Page   | Error      | Shows error when a part of the form is wrong/empty.  |
| Sign-up Page | /          | Form to fill when the user does not have an account. |
| Sign-up Page | Error      | Show errors when a field is empty.                   |

**Visuals**:

![Login Section Undertakers Picture](./img/wireframe/undertakers/loginSection.png)

---

##### 3.1.3.2. Home Section

---

**Pages**:

| Name      | Complement | Description                                                                                |
| --------- | ---------- | ------------------------------------------------------------------------------------------ |
| Home Page | Admin      | Display all the information about the company and is the center of all the other sections. |
| Home Page | Employee   | Center of the other sections, less information display than the admin.                     |

**Visuals**:

![Home Section Undertakers Picture](./img/wireframe/undertakers/homeSection.png)

---

##### 3.1.3.3. Profile Section

---

**Pages**:

_Admin_:

| Name           | Complement             | Description                                                                                          |
| -------------- | ---------------------- | ---------------------------------------------------------------------------------------------------- |
| Profile Page   | /                      | Contains a form about the company, each field can be completed.                                      |
| Profile Page   | Error                  | One of the fields is empty or incorrect.                                                             |
| Profile Page   | Request                | One of the fields was requested to changes.                                                          |
| Profile Pop-up | Request - Selection    | Contains a list of all the elements where changes are requested.                                     |
| Profile Pop-up | Request - Result       | Contains the same list as above, validated requests are displayed in green, disapproved ones in red. |
| Profile Pop-up | Request - Category     | Pop-up to compare previous data to new one.                                                          |
| Profile Pop-up | Request - Verification | Double check before denying/accepting proposal.                                                      |

_Employees_:

| Name           | Complement             | Description                                                                           |
| -------------- | ---------------------- | ------------------------------------------------------------------------------------- |
| Profile Page   | /                      | Contains company information, can modify the words to mourners section.               |
| Profile Pop-up | Request                | Contains a list of all the fields that can't be accessed directly by the employee.    |
| Profile Pop-up | Request - Category     | Contains a display of previous category's data and an input field for the suggestion. |
| Profile Pop-up | Request - Verification | Double check before validating the suggestion.                                        |

**Visuals**:

![Profile Section Undertakers Picture](./img/wireframe/undertakers/profileSection.png)

---

##### 3.1.3.4. Clients Section

---

**Pages**:

| Name          | Complement                       | Description                                                                                                                      |
| ------------- | -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Client Page   | Admin - With Feedback            | Display basic information about consumers, and a list of all the clients. There is a list of feedback on the side of the screen. |
| Client Page   | Admin - With Feedback - Error    | Appears when a search is made and no client match the search.                                                                    |
| Client Page   | Admin - Without Feedback         | Display basic information about consumers, and a list of all the clients.                                                        |
| Client Page   | Admin - Without Feedback - Error | Appears when a search is made and no client match the search.                                                                    |
| Client Page   | Add Client                       | Displays a form with deceased and client information to fill.                                                                    |
| Client Page   | Add Client - Error               | Appears when a field is empty.                                                                                                   |
| Client Page   | Client Profile                   | Displays all the information about the client that undertakers wrote. A personal message could also be written.                  |
| Client Page   | Modify Client                    | Same form as Add Client but input fields are already filled.                                                                     |
| Client Pop-up | Regenerate - Verification        | Douvle check if a password should be regenerated or not.                                                                         |
| Client Pop-up | Modify - Verification            | Double check if the modification are correct before validating them.                                                             |

**Visuals**:

![Clients Section Undertakers Picture](./img/wireframe/undertakers/clientsSection.png)

---

##### 3.1.3.5. Employees Section

---

**Pages**:

| Name            | Complement            | Description                                                                   |
| --------------- | --------------------- | ----------------------------------------------------------------------------- |
| Employees Page  | /                     | Displays a list of employee and a button to add new ones.                     |
| Employee Pop-up | Remove                | Double check before removing an employee of the list.                         |
| Employee Pop-up | Add                   | Form to fill to add a new employee (Full Name, Email, Password, Permissions). |
| Employee Pop-up | Modify                | Same form as above but filled with already existing information.              |
| Employee Pop-up | Modify - Verification | Double Check before updating database.                                        |

**Visuals**:

![Employees Section Undertakers Picture](./img/wireframe/undertakers/employeesSection.png)

---

#### 3.1.4. Administrator Side

---

Lastly, as for the two previous side, the administrator part could be access by clicking on the administrator button. \
This section will be composed of the sections listed hereunder:

- [Login](#3141-login-section)
- [Home](#3142-home-section)
- [Application](#3143-application-section)
- [Undertakers](#3144-undertakers-section)
- [Mourners](#3145-mourners-section)
- [Profile](#3146-profile-section)

Those can be access via links or on the following section of the document.

---

##### 3.1.4.1. Login Section

---

**Pages**:

| Name         | Complement | Description                             |
| ------------ | ---------- | --------------------------------------- |
| Welcome Page | /          | Page to welcome user in.                |
| Login Page   | /          | Displays a form to fill.                |
| Login Page   | Error      | Appears when a field is emoty or wrong. |

**Visuals**:

![Login Section Administrator Picture](./img/wireframe/administrators/loginSection.png)

---

##### 3.1.4.2. Home Section

---

**Pages**:

| Name      | Complement | Description                                             |
| --------- | ---------- | ------------------------------------------------------- |
| Home Page | /          | Center of the sections and display of basic statistics. |

**Visuals**:

![Home Section Administrators Picture](./img/wireframe/administrators/homeSection.png)

---

##### 3.1.4.3. Application Section

---

**Pages**:

| Name             | Complement | Description                                                         |
| ---------------- | ---------- | ------------------------------------------------------------------- |
| Application Page | /          | Contains more advanced statistics, graphs, and payment information. |

**Visuals**:

![Application Section Administrator Picture](./img/wireframe/administrators/applicationSection.png)

---

##### 3.1.4.4. Undertakers Section

---

**Pages**:

| Name             | Complement         | Description                                                               |
| ---------------- | ------------------ | ------------------------------------------------------------------------- |
| Undertakers Page | /                  | Displays a list of undertakers with colors defining the payment deadline. |
| Undertakers Page | Undertaker Profile | Displays undertaker profile (company, admin, due date, fee amount).       |

**Visuals**:

![Undertakers Section Administrators Picture](./img/wireframe/administrators/undertakersSection.png)

---

##### 3.1.4.5. Mourners Section

---

**Pages**:

| Name          | Complement       | Description                                                                                     |
| ------------- | ---------------- | ----------------------------------------------------------------------------------------------- |
| Mourners Page | /                | List of all the clients link to their undertakers.                                              |
| Mourners Page | Mourners Profile | Displays information about mourners (full name, company name, account creation date, feedback). |

**Visuals**:

![Mourners Section Administrators Picture](./img/wireframe/administrators/mournersSection.png)

---

##### 3.1.4.6. Profile Section

---

**Pages**:

| Name           | Complement                  | Description                                                                                |
| -------------- | --------------------------- | ------------------------------------------------------------------------------------------ |
| Profile Page   | /                           | Displays admin information and a list of feedback.                                         |
| Profile Page   | Modify                      | Displays a form filled with administrator information (photo, full name, email, password). |
| Profile Page   | Error                       | Appears when empty field.                                                                  |
| Profile Pop-up | Modification - Verification | Double Check before updating database.                                                     |
| Profile Pop-up | Website URL - Verification  | Double Check before changing URL.                                                          |

**Visuals**:

![Profile Section Administrators Picture](./img/wireframe/administrators/profileSection.png)

---

### 3.2. Mockups

---

<!-- TODO:  Figma to be done -->

This application contains three main sides which are Mourners, Undertakers, and Administrator.

This section will start with the common redirection page and then will go through each side independently.

The mockup (Figma) can also be access as raw file in the [Design Folder](./design/AfterWords.fig).

---

#### 3.2.1. Redirection Page

---

The Redirection Page will be the first page each user of the application will see when they first connect. It would look like as presented below:

---

#### 3.2.2. Mourners Side

---

After the mourner button clicked, users will be redirected to this side of AfterWords. It would contain the following sections:

- [Login](#3221-login-section)
- [Home](#3222-home-section)
- [Profile](#3223-profile-section)
- [Instance](#3224-instance-section)
- [Letters](#3225-letters-section)
- [Undertaker](#3226-undertaker-section)
- [Procedure](#3227-procedure-section)

Each of those are accessible below or you can click on them to be redirected instantly to the intended section description.

---

##### 3.2.2.1. Login Section

---

---

##### 3.2.2.2. Home Section

---

**Dark Theme**:

**Light Theme**:

---

##### 3.2.2.3. Profile Section

---

**Dark Theme**:

**Light Theme**:

---

##### 3.2.2.4. Instance Section

---

**Dark Theme**:

**Light Theme**:

---

##### 3.2.2.5. Letters Section

---

**Dark Theme**:

**Light Theme**:

---

##### 3.2.2.6. Undertaker Section

---

**Dark Theme**:

**Light Theme**:

---

##### 3.2.2.7. Procedure Section

---

**Dark Theme**:

![alt text](image-2.png)

**Light Theme**:

---

#### 3.2.3. Undertakers Side

---

Once the undertaker buttin is clicked, the user will be redirected into this side of the application. \
This one would be composed of the following sections:

- [Login](#3231-login-section)
- [Home](#3232-home-section)
- [Profile](#3233-profile-section)
- [Clients](#3234-clients-section)
- [Employees](#3235-employees-section)

Each of those are written under and can be access threw the links above.

---

##### 3.2.3.1. Login Section

---

---

##### 3.2.3.2. Home Section

---

**Dark Theme**:

**Light Theme**:

---

##### 3.2.3.3. Profile Section

---

**Dark Theme**:

**Light Theme**:

---

##### 3.2.3.4. Clients Section

---

**Dark Theme**:

**Light Theme**:

---

##### 3.2.3.5. Employees Section

---

**Dark Theme**:

**Light Theme**:

---

#### 3.2.4. Administrator Side

---

Lastly, the administrator part could be access by clicking on the administrator button. \
This section will be composed of the sections listed hereunder:

- [Login](#3241-login-section)
- [Home](#3242-home-section)
- [Application](#3243-application-section)
- [Undertakers](#3244-undertakers-section)
- [Mourners](#3245-mourners-section)
- [Profile](#3246-profile-section)

Those can be access via links or on the following section of the document.

---

##### 3.2.4.1. Login Section

---

---

##### 3.2.4.2. Home Section

---

**Dark Theme**:

**Light Theme**:

---

##### 3.2.4.3. Application Section

---

**Dark Theme**:

**Light Theme**:

---

##### 3.2.4.4. Undertakers Section

---

**Dark Theme**:

**Light Theme**:

---

##### 3.2.4.5. Mourners Section

---

**Dark Theme**:

**Light Theme**:

---

##### 3.2.4.6. Profile Section

---

**Dark Theme**:

**Light Theme**:

---

### 3.3. Color Palette

---

AfterWords would have two themes, a light one and a dark one. They would be set corresponding to the user computer preferences.

The dark theme would be composed of the following colors:

| Name                 | Preview                                                                                                   | Hexacode | RGB Code           |
| -------------------- | --------------------------------------------------------------------------------------------------------- | -------- | ------------------ |
| Dark Gunmetal        | <img alt="Dark Gunmetal" width="200px" height="50px" src="./img/colorPalette/darkTheme/darkGunmetal.png"> | #1F1F2E  | rgb(31, 31, 46)    |
| Gunmetal             | <img alt="Gunmetal" width="200px" height="50px" src="./img/colorPalette/darkTheme/gunmetal.png">          | #2B2B3C  | rgb(43, 43, 60)    |
| Chinese White        | <img alt="Chinese White" width="200px" height="50px" src="./img/colorPalette/darkTheme/chineseWhite.png"> | #E0E0E0  | rgb(224, 224, 224) |
| Cadet Blue (Crayola) | <img alt="Cadet Blue" width="200px" height="50px" src="./img/colorPalette/darkTheme/cadetBlue.png">       | #B0B0C0  | rgb(176, 176, 192) |
| Arsenic              | <img alt="Arsenic" width="200px" height="50px" src="./img/colorPalette/darkTheme/arsenic.png">            | #3A3A4F  | rgb(58, 58, 79)    |
| Sea Serpent          | <img alt="Sea Serpent" width="200px" height="50px" src="./img/colorPalette/seaSerpent.png">               | #4DD0E1  | rgb(77, 208, 225)  |
| Mustard              | <img alt="Mustard" width="200px" height="50px" src="./img/colorPalette/mustard.png">                      | #FFD54F  | rgb(255, 213, 79)  |
| Fire Opal            | <img alt="Fire Opal" width="200px" height="50px" src="./img/colorPalette/fireOpal.png">                   | #EF5350  | rgb(239, 83, 80)   |
| Dark Sea Green       | <img alt="Dark Sea Green" width="200px" height="50px" src="./img/colorPalette/darkSeaGreen.png">          | #81C784  | rgb(129, 199, 132) |

For the light theme the colors would be:

| Name             | Preview                                                                                                         | Hexacode | RGB Code           |
| ---------------- | --------------------------------------------------------------------------------------------------------------- | -------- | ------------------ |
| Ghost White      | <img alt="Ghost White" width="200px" height="50px" src="./img/colorPalette/lightTheme/ghostWhite.png">          | #F7F7FA  | rgb(247, 247, 250) |
| Eerie Black      | <img alt="Eerie Black" width="200px" height="50px" src="./img/colorPalette/lightTheme/eerieBlack.png">          | #1A1A1A  | rgb(26, 26, 26)    |
| Chinese White    | <img alt="Chinese White" width="200px" height="50px" src="./img/colorPalette/darkTheme/chineseWhite.png">       | #E0E0E0  | rgb(224, 224, 224) |
| White            | <img alt="White" width="200px" height="50px" src="./img/colorPalette/lightTheme/white.png">                     | #FFFFFF  | rgb(255, 255, 255) |
| Anti-Flash White | <img alt="Anti-Flash White" width="200px" height="50px" src="./img/colorPalette/lightTheme/antiFlashWhite.png"> | #F0F0F0  | rgb(240, 240, 240) |
| Sea Serpent      | <img alt="Sea Serpent" width="200px" height="50px" src="./img/colorPalette/seaSerpent.png">                     | #4DD0E1  | rgb(77, 208, 225)  |
| Mustard          | <img alt="Mustard" width="200px" height="50px" src="./img/colorPalette/mustard.png">                            | #FFD54F  | rgb(255, 213, 79)  |
| Fire Opal        | <img alt="Fire Opal" width="200px" height="50px" src="./img/colorPalette/fireOpal.png">                         | #EF5350  | rgb(239, 83, 80)   |
| Dark Sea Green   | <img alt="Dark Sea Green" width="200px" height="50px" src="./img/colorPalette/darkSeaGreen.png">                | #81C784  | rgb(129, 199, 132) |

---

### 3.4. Logo

---

The logo of AfterWords was generated by [deepai](https://deepai.org/machine-learning-model/text2img) to fit the shorts deadlines and would look like the following logo:

<img alt="Logo AfterWords" src="./img/logoAfterWords.png" width="200px">

Later on, this logo would be replaced by a handmade one on an application made for design/drawing, which is named [Krita](https://krita.org/en/). It would represent a dove escaping from paperwork and documents.

---

### 3.5. Font

---

About the application font, AfterWords will entirely use Inter. This font is widely spread around websites and is easily readable.

---

## 4. Functional Requirements

### 4.1. User Roles And Permissions

---

#### 4.1.1. Administrator

---

**Role owner**: Maxime THIZEAU

**Permissions**:

> [!Tip]
> Can:
>
> - See all users.
> - See database.
> - Modify UI/UX.
> - Add new undertakers.
> - Add new instances.
> - Add new templates.

---

> [!Caution]
> Can't:
>
> - See mourners' personal information.
> - Have access to uploaded documents.

---

#### 4.1.2. Undertakers

---

**Role owners**: Undertakers (Admin)

> [!Tip]
> Can:
>
> - See users account they created.
> - Access low privacy user database (full name, deceased information).
> - Add new employees
> - Manage employees
> - Add new mourners
> - Update company inforamtion

---

> [!Caution]
> Can't:
>
> - See other users accounts.
> - Access other users accounts.
> - See mourner's personal information.
> - See database.
> - Modify instances.
> - Modify templates.

**Role owners**: Undertakers (Employee)

> [!Tip]
> Can:
>
> - See users account they created.
> - Access low privacy user database (full name, deceased information).
> - Add new mourners

---

> [!Caution]
> Can't:
>
> - See other users accounts.
> - Access other users accounts.
> - See mourner's personal information.
> - See database.
> - Modify instances.
> - Modify templates.
> - Manage other Employees.
> - Change company information.

---

#### 4.1.3. Mourners

---

**Role owners**: Mourners

> [!Tip]
> Can:
>
> - Upload documents.
> - Delete documents.
> - Search for instances.
> - Add instances.
> - Remove instances.
> - See templates.
> - Complete templates.
> - Send letters.
> - Give access to their accounts to undertakers.
> - See deceased information.
> - Add specification to deceased information.
> - Request a modification on deceased information.

---

> [!Caution]
> Can't:
>
> - See database.
> - Access undertakers account.
> - Access other users account.
> - Modify deceased primary information (death date, full name, last location, birth date, birth location).

---

### 4.1.4. System Features And Functions

---

**Mourners Side**:

| Feature Name             | Description                                                                        | Inputs                         | Outputs                                   | Behavior                                                                                                                                                                             |
| ------------------------ | ---------------------------------------------------------------------------------- | ------------------------------ | ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Add Document             | Mourners should add documents to their profile in order to complete the procedure. | Document                       | Documents added to the profile.           | Mourners click on Add Document. They select the intended category. They upload their document. It is added to the profile page and in database.                                      |
| Delete Document          | Mourners want to remove a document that is not necessary for the procedure.        | Document to remove.            | No document.                              | Mourners Click on remove button on the same line as the document they want to remove. Click on validate on the Pop-up Verification.                                                  |
| See Document             | Mourners can see in another tab documents they already inputs.                     | Document                       | New Tab with Document's display.          | Click on see button to preview the page. Open a new tab with the document.                                                                                                           |
| Add Deceased Information | Mourners can precise information about deceased.                                   | Typed information.             | Information in deceased information card. | Click on add infprmation button. Type the information you want to precise. Enter.                                                                                                    |
| Add Instances            | Mourners should add instances to their profile in order to complete the procedure. | Instances checked.             | List of instances in Instances Page.      | Click on add instances. Add tags. Type instance name. Check instances needed. Click on the Validate button.                                                                          |
| Remove Instances         | Mourners want to remove an instances not needed to contact.                        | Instance to remove.            | Instance removed.                         | Click on remove button on the same line as the instance they want to remove. Click on validate on the Pop-up Verification.                                                           |
| See Instances            | Mourners can see in another tab instances they already inputs.                     | Instance                       | New Tab with Instance's display.          | Click on see button. A new tab open with instance information.                                                                                                                       |
| Add Letters              | Mourners should add letters to their profile in order to complete the procedure.   | Letters                        | Letters add to the Letters Page.          | Click on add button. Slide to find the good template. Click on Select Button.                                                                                                        |
| Remove Letters           | Mourners want to remove a letter that is not good enough for them.                 | Letter to remove.              | Letter removed.                           | Click on remove button. The letter is removed from the database and the input cleared.                                                                                               |
| See Letters              | Mourners can see letters in another page.                                          | Letter                         | New Page with letter's display.           | Click on see button. A new page appears with letter's display.                                                                                                                       |
| Create Letters           | Mourners can create their own letters if needed.                                   | Form to complete.              | New letter in pdf format.                 | Click on add button next to other field. Complete every input field. Click on validate button.                                                                                       |
| Ask Undertakers For Help | Mourners can ask help to complete the procedure to undertakers.                    | Email.                         | Procedure                                 | Go on the Undertaker Profile Page. Click on ask for help button. Undertakers can accept or deny your request.                                                                        |
| Complete Procedure       | Mourners need to complete the procedure.                                           | Documents, Letters, Instances. | Emails.                                   | Click on Start button. Complete each step by fullfilling blanks in letters templates for every instance. Give a feedback to AfterWords and/or Undertakers. Click on validate button. |

---

**Undertakers Side**:

| Feature Name                 | Role     | Description                                                                 | Inputs                              | Outputs                           | Behavior                                                                                                          |
| ---------------------------- | -------- | --------------------------------------------------------------------------- | ----------------------------------- | --------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Sign-up                      | Admin    | Complete a form to create an account                                        | Forms field                         | New account created               | Complete Form. Click on Sign-up.                                                                                  |
| Login                        | Both     | Access to account.                                                          | Username, password, email.          | Access to account                 | Complete form. Click on Login.                                                                                    |
| Change profile               | Admin    | Admin can change profile on the application to make it up to date.          | field inputs.                       | Profile page.                     | Click on modify button. Change needed fields. Click on validate button.                                           |
| Request Changes on profile   | Employee | Employees can change directly profile page, they need to ask requests.      | Fields to change, modifications.    | Send a request to admin.          | Click on ask for changes button. Check fields you want to modify. Write your suggestion. Click on Request button. |
| Review Request               | Admin    | Review Employee's suggestions to change the profile page.                   | Employee's request.                 | accept or denied changes.         | Click on review changes. Click on the desired field. Accept or deny changes. Validate choice.                     |
| Write kind words to mourners | Both     | Undertakers can assess small words to mourners.                             | Typed Text.                         | Text display.                     | Click on Small Words Field. Write your Words. Press Enter.                                                        |
| Add Client                   | Both     | Undertakers need to create accounts to mourners.                            | Mourners and deceaseds information. | new mourner account.              | Click on add Client Button. Fill the form. Create account.                                                        |
| Modify Client                | Both     | Undertakers can do mistakes and need to apply changes on clients if needed. | Client Profile.                     | Modified Client Profile.          | Click on the Client Profile. Click on modify Button. Change necessary fields. Validate Choices.                   |
| View Client Profile          | Both     | Undertakers can access Client information.                                  | Client on list.                     | New page with client information. | Search for your client. Click on its line in the list.                                                            |
| Regenerate password          | Both     | Password can be forbiden and so regenerated.                                | Regenerate Button.                  | New password.                     | Go on the Client Profile. Click on the regenerate button. Click on Yes in the Pop-up.                             |
| Add Employee                 | Admin    | Admin undertaker can add employees to lighten his work amount.              | Employees information.              | New Employee Account.             | Click on add Employee button. Fill the form. Click on add new employee button.                                    |
| Remove Employee              | Admin    | Employees can leave company so employees can be removed.                    | Employee accounts.                  | Empty section.                    | Search for employee. Click on remove button. Click on validate.                                                   |
| Modify Employee              | Admin    | Admin undertaker can do mistakes and need to correct them.                  | Employee Account.                   | Modified employee account.        | Go to Employee Profile. Click on Modify Employee button. Change needed fields. Click on Validate.                 |
| Promote Employee             | Admin    | Admin can give admin role to employee.                                      | Employee's role.                    | Admin role given.                 | Search for the employee. Click on the promote icon.                                                               |

---

**Administrators Side**:

| Feature Name                | Description                                                                    | Inputs                             | Outputs                             | Behavior                                                                                                  |
| --------------------------- | ------------------------------------------------------------------------------ | ---------------------------------- | ----------------------------------- | --------------------------------------------------------------------------------------------------------- |
| View Application Statistics | Administrator can view the advancement of the application, number of use, ect. | Statistics.                        | Display.                            | Looks for desired statistics. Display them in a page.                                                     |
| View Undertakers List       | Administrator need to survey undertakers.                                      | Undertakers accounts.              | List of Undertakers.                | Displays undertakers in green if they paid, in orange if they are near due date, in red if they are late. |
| View Undertakers Profile    | Administrator can look at undertaker profiles.                                 | Undertaker account.                | Display                             | Search for the undertaker. Click on the line.                                                             |
| Request Monthly Fee         | Administrator need to remind undertakers to pay fees.                          | Email address and predefined body. | Email sent.                         | Go to undertaker's profile. Click on Send email button.                                                   |
| View Mourners List          | Administrators need to survey mourners.                                        | Mourners account.                  | List of Mourners.                   | Collects all Mourners account in database. Display them as a list.                                        |
| View Mourners Profile       | Administrator can access a precise account.                                    | Mourner Account.                   | New page with mourners information. | Search for the mourner. Click on the line.                                                                |
| Edit Admin Profile          | Administrator can change fields in profile if needed.                          | Admin Profile.                     | Modified Profile.                   | Click on modify button. Change intended fields. Click on validate button.                                 |

---

### 4.1.5. Application Workflow

---

```mermaid
graph TD
  %% Mourner Flow
  subgraph Mourner Flow
    A[Welcome Page] --> B[Login Page]
    B -->|If error| BE[Login Page Error]
    B -->|If no error| C[Home Page]

    C --> D[Profile Page]
    C --> E[Instances Page]
    C --> F[Letters Page]
    C --> G[Undertaker Page]
    C --> H[Procedure Page]

    D --> D1[Pop-up Verifiaction]
    D --> D2[Pop-up Phase 1]
    D2 --> D3[Pop-up Cancel]
    D2 --> D4[Pop-up Phase 2]
    D2 --> D5[Pop-up Phase 2 New Document]
    D4 -->|If error| D4E[Pop-up Phase 2 Error]
    D5 -->|If error| D5E[Pop-up Phase 2 New Document Error]

    E --> E1[Pop-up Verification]
    E --> E2[Add Instance]
    E2 -->|If results| E3[Search]
    E2 -->|If no result| E3E[No Result]
    E2 & E3 & E3E --> E4[Pop-up Tags]
    E2 & E3 --> E5[Instance Info]

    F --> F1[Pop Verification]
    F --> F2[Select Letters Template]
    F --> F3[Your Template]
    F --> F4[Template Creation]
    F4 --> F5[Pop-up Preview]
    F4 --> F6[Pop-up Import]
    F4 -->|If error| F4E[Template Creation Error]
    F6 -->|If error| F6E[Pop-up Import Error]

    H --> H1[Step 1]
    H1 -->|If error| H1E[Step 1 Error]
    H1 --> H2[Step 2]
    H2 -->|If error| H2E[Step 2 Error]
    H2 --> H3[Step 3]
    H3 -->|If error| H3E[Step 3 Error]
    H3 --> H4[Step 4]
    H4 -->|If error| H5[Step 5]
    H5 -->|If yes checked| H5B[Step 5 Feedback]
    H5 & H5B --> H6[Pop-up Validation]
    H6 --> H7[Last Step]

    H1 & H2 & H3 & H4 --> H8[Template Completion]
    H8 -->|If error| H8E[Template Completion Error]
  end
```

```mermaid
graph TD
  %% Undertaker Flow
  subgraph Undertaker Admin Flow
    A[Welcome Page] --> A1[Login Page]
    A1 -->|If error| A1E[Login Page Error]
    A1 --> A2[Sign-up Page]
    A1 --> B[Home Page Admin]
    A2 -->|If error| A2E[Sign-up Page Error]

    B --> C[Profile Page]
    B --> D[Clients Page]
    B --> E[Employees page]

    C -->|If error| CE[Profile Page Error]
    C -->|If request| CR[Profile Page Request]
    C --> C1[Pop-up Request Selection]
    C1 --> C2[Pop-up Request Category]
    C2 -->|If accept| C3[Pop-up Request Verification]
    C2 -->|If denied| C3[Pop-up Request Verification]

    D -->|If error| DE[Client Page No Result]
    D -->|If no feedback| DF[Client Page No Feedback]
    D -->|If no feedback and error| DFE[Client Page No Feedback and No Result]
    D --> D1[Add Client]
    D --> D2[Client Profile]
    D1 -->|If error| D1E[Add Client Error]
    D2 --> D3[Modify Client]
    D2 & D3 --> D4[Pop-up Regenerate Verification]
    D3 --> D3E[Modify Client Error]
    D3 --> D5[Pop-up Modify verification]

    E --> E1[Pop-up Remove]
    E --> E2[Pop-up Add]
    E --> E3[Pop-up Modify Employee]
    E2 -->|If error| E2E[Pop-up Add Error]
    E3 -->|If error| E3E[Pop-up Modify Employee Error]
    E3 --> E4[Pop-up Modify Verification]
  end

  subgraph Undertaker Employee Flow
    ZA[Welcome Page] --> ZA1[Login Page]
    ZA1 -->|If error| ZA1E[Login Page Error]
    ZA1 --> ZA2[Sign-up Page]
    ZA1 --> ZB[Home Page Employee]
    ZA2 -->|If error| ZA2E[Sign-up Page Error]

    ZB --> ZC[Profile Page]
    ZB --> ZD[Clients Page]

    ZC --> ZC1[Pop-up Request]
    ZC1 --> ZC2[Pop-up Request Category]
    ZC1 & ZC2 --> ZC3[Pop-up Request Verification]

    ZD -->|If error| ZDE[Client Page No Result]
    ZD -->|If no feedback| ZDF[Client Page No Feedback]
    ZD -->|If no feedback and error| ZDFE[Client Page No Feedback and No Result]
    ZD --> ZD1[Add Client]
    ZD --> ZD2[Client Profile]
    ZD1 -->|If error| ZD1E[Add Client Error]
    ZD2 --> ZD3[Modify Client]
    ZD2 & ZD3 --> ZD4[Pop-up Regenerate Verification]
    ZD3 --> ZD3E[Modify Client Error]
    ZD3 --> ZD5[Pop-up Modify verification]
  end
```

```mermaid
graph TD
  %% Administrator Flow
  subgraph Administrator Flow
    A[Welcome Page] --> A1[Login Page]
    A1 -->|If error| A1E[Login Page Error]
    A1 --> B[Home Page]

    B --> C[Application Page]
    B --> D[Undertakers Page]
    B --> E[Mourners Page]
    B --> F[Profile Page]

    D --> D1[Undertaker Profile]

    E --> E1[Mourner Profile]

    F --> F1[Modify]
    F1 -->|If error| F1E[Modify Error]
    F1 --> F2[Pop-up Verification]
    F1 --> F3[Pop-up URL]
  end
```

---

## 5. Non-Functional Requirement

### 5.1. Security

---

AfterWords will have security and data privacy on many aspects.

**Authentification**:

Authentification will be done for every accounts. They will need to register a username and a password to connect to their account. However, Password would be automatically generated for Clients and it would be transferred to them by email via undertakers.

**Authorization**:

Every roles will have different authorization on the application and database.

- Clients will only view data related to their account and will have access to the template and instance list.
- Undertakers Admin will have access to very feature on the undertaker account and could access every client account they created.
- Undertakers Employees have fewer access on the undertaker account and can't modify profile or add/remove employee. They could access every client account the company has created.
- Administrators can view every client and undertakers profile. However, they cannot access employees account.

**Encryption**:

All passwords will be necrypted. When an undertaker creates a new account for a mourner, they should not see the password. This one would be send directly via email to the mourner.

---

### 5.2. Responsiveness

---

This application is a web application and should be compatible on every operating system to touch a wider range of clients/mourners. Moreover, the application would be accessible only for computers as tablets and smartphone aren't relevant enough to fulfill this kind of procedure.

In other words, AfterWords should be usable on every operating system, chrome, mozilla firefox, and google. It would be responsible on the following screen sizes:

- 1920×1080px,
- 1366×768px,
- 1280×1024px,
- 1024×768px.

---

### 5.3. Performance

---

AfterWords should be really performant on two aspects.

First, it needs to load entirely in less than 4 seconds, and to change pages in less than 1. Mourners are already in a difficult time and don't want to spend to much time waiting for the website to load.

Secondly, AfterWords would have to be performant under an important amount of user at the same time. A lot of deceased are identified each day (1,800 deceased a day). In case a huge amount of people dies the same day, the application should not crash under 10,000 users at the same time.

---

### 5.4. Connectivity

---

This application would be a web application, therefore, an internet connecrtion should be provided by the user to acces the website.

---

### 5.5. Marketing

---

Concerning the marketing of the application, it would be sold as a subscription plan with three offers. The offers would be mensual, trimestrial and anual. They would respectively cost, ..., ..., and ....

The application would be promoted by the administrator, Maxime THIZEAU. The promotion would be done by phone call or email exchange to the different underatker companies, firstly in Bourges, Cher, then in a wider region to end to the globality of France.

---

## 6. Data

### 6.1. Templates

---

AfterWords would contain templates for mourners to complete. However, it would be too long to describe them all in this specification. Therefore, they would be stored in a subfolder called [templates](./templates/).

They would be ordered in subcategories which are the following:

- To Obtain
- Finance
- Employer and ASSEDIC
- Health Insurance
- Insurances
- Mutual
- Pensions
- Family Allowance
- Notary and Estate Taxation
- Subscriptions

---

### 6.2. Documents To Obtain

---

Completing a procedure after a death is quite long and complicated in France. Therefore, a mourner will have to collect the following documents to complete it.

The documents needed are:

- Extrait d'acte de décès (10 à 15 ex.) ou copie
- La copie du livret de famille remplace la fiche familiale ou individuele d'état civil
- Extrait d'acte de naissance ou copie
  - pour le défunt
  - pour le conjoint
  - pour les exs-conjoints
- Certificat de concubinage
- Pacte civil de solidarité (P.A.C.S.)
- Acte de mariage
- Fiche de revalorisation de salaire
- Trois derniers bulletins de salaire
- Attestation de présence dans l'entreprise
- Certificat d'hérédité

The mourner will also need to have:

- Relevé d'identité bancaire (10 à 15 originaux)
- Relevé d'identité postal (10 à 15 originaux)
- Relevé de la caisse d'épargne (10 à 15 originaux)

Other documents:

- Avis de non-imposition deux dernières années : pour certains organismes
- Avis d'imposition des deux dernières années : pour les caisses de retraites
- Justificatifs des ressources : pour certains organismes

As well as the deceased papers:

- Assurance
  - Quittances et primes
  - Contrat d’assurance habitation et automobile
  - Dossier d’indemnisation (dommages corporels)
  - Assurance sur la vie et assurance décès
- Voiture
  - Contraventions
  - Factures (achat, réparation…)
- Banque
  - Chèques à encaisser
  - Prêts à la consommation
  - Prêt immobilier
  - Relevés de compte, virements, prélèvements, remises de chèques, talons de chèques
- Famille
  - Actes d’état civil (copies intégrales et extraits)
  - Remboursement des allocations familiales
  - Jugement de divorce, jugement d’adoption
  - Acte de reconnaissance d’un enfant
  - Mariage (contrat, documents relatifs aux biens)
  - Livret de famille
  - Testament, succession
- Logement
  - Factures d’électricité et de gaz
  - Factures d’eau
  - Factures de téléphone
- Santé
  - Capital décès, radiographies, dossiers médicaux
  - Accident du travail, remboursement, indemnités journalières
  - Mutuelle (carte, remboursement)
  - Remboursement d’assurance maladie-maternité
  - Titres de paiement de la pension de retraite
- Impôts et Taxes
  - Avis d’impôts (revenu, taxe foncière, taxe d’habitation)
  - Bulletins de salaire, contrat de travail
- Contrat de location et logement
  - Inventaire du mobilier pour les locations meublées
  - Quittances de loyer
  - Contrat de location
  - Charges de copropriété
  - Procès-verbaux d’assemblée de copropriété
  - Travaux (factures, devis)

In case the mourner don't know how to get these documents or what they are, more information are displayed in the [documents to get file](./documentsToGet.md).

---

### 6.3. Urgent Procedure (In The Week Following The Death)

---

The procedures are inspired by a physical document that has been translated and reformated into markdown. However, this procedure is too long to put in the Functional Specification at once. Therefore, an appendix was made specialy for the Urgent Procedure.

This appendix can be find following [this link](./appendices/urgentProcedureGuide.md) or in the [appendices folder](./appendices/).

---

### 6.4. No Urgent Procedure (Within Six Months After Death)

---

The procedures are inspired by a physical document that has been translated and reformated into markdown. However, this procedure is too long to put in the Functional Specification at once. Therefore, an appendix was made specialy for the No Urgent Procedure.

This appendix can be find following [this link](./appendices/noUrgentProcedureGuide.md) or in the [appendices folder](./appendices/).

---

### G.5. Tags

---

<!-- TODO: List all the potential tags to ease the search of instances on the client side. -->

---

## 7. External Interfaces

<!-- - **APIs**: Describe any APIs the system will expose or consume.
- **Third-Party Integrations**: List any integrations with external systems.
- **Hardware Interfaces**: Describe interactions with physical devices if applicable.   -->

## 8. Constraints And Limitations

<!-- - Highlight known constraints, such as technology limitations or compliance requirements.   -->

## 9. Appendices

### 9.1. Glossary

---

---

### 9.2. Resources

---

**Color-name**: <https://www.color-name.com>

**Color Hunt**: <https://colorhunt.co>

**Krita**: <https://krita.org/en/>

---
