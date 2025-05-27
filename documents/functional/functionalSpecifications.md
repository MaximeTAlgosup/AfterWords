# Functional Specification Document - AfterWords <!-- omit in toc -->

<details>
<summary> Table Of Contents </summary>

- [Introduction](#introduction)
  - [Project Overview](#project-overview)
  - [Project Definition](#project-definition)
    - [Vision](#vision)
    - [Objectives](#objectives)
    - [Scope](#scope)
      - [In-scope](#in-scope)
      - [Out-of-scope](#out-of-scope)
    - [Target Audience](#target-audience)
    - [Deliverables](#deliverables)
    - [Definitions And Acronyms](#definitions-and-acronyms)
  - [Project Organisation](#project-organisation)
    - [Project Representatives](#project-representatives)
    - [Stakeholders](#stakeholders)
    - [Project Reviewers](#project-reviewers)
  - [Project Plan](#project-plan)
    - [Retroplanning](#retroplanning)
    - [Milestones](#milestones)
    - [Dependencies](#dependencies)
    - [Assumptions/Constraints](#assumptionsconstraints)
    - [Risks/Mitigation](#risksmitigation)
- [Use Cases and Personas](#use-cases-and-personas)
  - [Use Cases](#use-cases)
    - [Creating A New Account](#creating-a-new-account)
    - [Select Instances](#select-instances)
    - [Uploading Documents](#uploading-documents)
    - [Send Letters To All Instances](#send-letters-to-all-instances)
  - [Personas](#personas)
    - [Persona 1: Janice LeBlanc](#persona-1-janice-leblanc)
    - [Persona 2: Sean McPhil](#persona-2-sean-mcphil)
    - [Persona 3: Alexandre Moutarde](#persona-3-alexandre-moutarde)
- [Design](#design)
  - [Wireframes](#wireframes)
  - [Mockups](#mockups)
  - [Color Palette](#color-palette)
  - [Logo](#logo)
  - [Font](#font)
- [Functional Requirements](#functional-requirements)
  - [User Roles And Permissions](#user-roles-and-permissions)
    - [Administrator](#administrator)
    - [Undertakers](#undertakers)
    - [Mourners](#mourners)
  - [System Features And Functions](#system-features-and-functions)
  - [Application Workflow](#application-workflow)
- [Non-Functional Requirement](#non-functional-requirement)
- [Data Management](#data-management)
  - [Data Flow](#data-flow)
  - [Database Schema](#database-schema)
- [External Interfaces](#external-interfaces)
- [Constraints And Limitations](#constraints-and-limitations)
- [Acceptance Criteria](#acceptance-criteria)
- [Appendices](#appendices)

</details>

## Introduction

### Project Overview

---

This project is made to help mourners with the french administration system. It would be delivered to undertakers which will deliver it to mourners.

This project is held by Maxime THIZEAU.

---

### Project Definition

---

#### Vision

Afterwords is an application allowing mourning people to get some help on the administration part. \
It would ease the process by gathering all instances in one place. \
How would that work?
The mourner just have to enter all the different instances and the required documents. Once it would be done, they would have to complete some templates of letters to send them all in one click.

---

#### Objectives

---

The objectives of this project are pretty clear:

- Centralizing mourners in one platform.
- Helping mourners comnpleting french administration.
- Allowing mourners to have information gathered on one website.

---

#### Scope

##### In-scope

---

AfterwWords will cover the different subject hereunder:

- It will suggest many letters template, allowing users to have a wider range of choice to complete and write there own letters.
- It will also gather french instances (such as EDF, France connect, ...) in one place.
- Users can chose the intended instances by checking their names within a page.
- AfterWords would have a database to store all the necessary documents for the said instances above.
- AfterWords would save time and energy to mourners.

---

##### Out-of-scope

---

The following points are what AfterWords will not do:

- AfterWords won't display user's information withinvthe application.
- It would not do administartion pe=rocedures for the user.
- It won't dispose of a messagerie within the application, the user will need to have an e-mail address of there own.
- Users can't organize funerals within the application.

---

#### Target Audience

AfterWords will have to target audience. \
The first hand audience would be undertakers company. AfterWords would be a service they could share, sell to their own customers, the second and final target audience of AfterWords, mourning people.

The mourning people are the main audience of this project. AfterWords is meant to help them through a difficult pass which is grieving. However, AfterWords won't be accessible on Internet in free-access. It would be unseen, that's why undertakers have a key role in this project.

---

#### Deliverables

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

#### Definitions And Acronyms

---

<!-- - List key terms and abbreviations with their explanations.   -->

---

### Project Organisation

---

#### Project Representatives

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

#### Stakeholders

---

| Role            | Representative           | Expectation                                                              |
| --------------- | ------------------------ | ------------------------------------------------------------------------ |
| owner           | Maxime THIZEAU           | Finished project while meeting requirements and proof-tested version one |
| School director | Franck JEANNIN (ALGOSUP) | Clear documentation and management based on the skills learnt in class   |

---

#### Project Reviewers

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

### Project Plan

---

#### Retroplanning

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

#### Milestones

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

#### Dependencies

---

**Task Dependencies**:

- The Functional Specification would be only completed once the Figma (design) and Excalidraw (Wireframe) would be entirely done.
- The Last Testing phase will start only after the first version is completed.
- The First Version of the application would need all three sides to be completed.

**Resource Dependencies**:

- All resources will be available at any point in the project since only one person complete every role.
- Reviewers will be required on different testing phases lasting one to two weeks after every code advancement (Mourner Side, MVP, Undertakers Side, Admin Side).

---

#### Assumptions/Constraints

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

#### Risks/Mitigation

---

| Type             | Description                                                    | Likelihood | Impact                                                      | Mitigation                                                                 |
| ---------------- | -------------------------------------------------------------- | ---------- | ----------------------------------------------------------- | -------------------------------------------------------------------------- |
| Sickness         | A team member becomes sick.                                    | High       | The project won't be updated while the team member is sick. | Planned more time than necessary to still be on track in case of sickness. |
| No user          | AfterWords is not appealing enough to consumers.               | Low        | The Product won'y be selled and the project obsolete.       | Having an important and efficient marketing campaign.                      |
| Data Leak        | The database leak and private information is lost on internet. | Medium     | AfterWords will lost undertakers and mourners trust.        | Having a solid data privacy and security on the database.                  |
| Unfunctional API | An API is not accessible from the application.                 | High       | This instance won't be accessible from the application.     | Finding another way to send and retrieve data from them.                   |

---

## Use Cases and Personas

### Use Cases

<!-- TODO: Add Use Cases, at least 2. And verify accuracy of already existing ones. -->

#### Creating A New Account

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

> [!Warning] Alternate Flows
>
> - The deceased already have an account.
> - Failed due to missing information.

**Postconditions**:

- AfterWords generate a password.
- Undertaker transmit account and password to mourner.

---

#### Select Instances

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

> [!Warning] Alternate Flows
> Instance not registered

**Postconditions**:

- Instance saved in `Instance to contact`.

---

#### Uploading Documents

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

> [!Warning] Alternate Flows
>
> - The document the user want to upload already is uploaded.
> - No document given to the `Document container`.

**Postconditions**:

- Documents saved within your account.

---

#### Send Letters To All Instances

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

> [!Warning] Alternate Flows
>
> - Blank space empty.
> - Failed due to lack of document.
> - Failed due to unprecised/no instance.

**Postconditions**:

- Letter sent to the instance via mail.

---

### Personas

---

<!-- TODO: Create three personas, mourner, undertaker, admin -->

#### Persona 1: Janice LeBlanc

---

**Name**:

**Age Range**:

**Frustrations**:

-
-
-

**Goals**:

-
-
-

---

#### Persona 2: Sean McPhil

---

**Name**:

**Age Range**:

**Frustrations**:

-
-
-

**Goals**:

-
-
-

---

#### Persona 3: Alexandre Moutarde

---

**Name**:

**Age Range**:

**Frustrations**:

-
-
-

**Goals**:

-
-
-

---

## Design

### Wireframes

---

<!-- TODO: insert excalidraw and describe each part/page -->

---

### Mockups

---

<!-- TODO:  Figma to be done -->

---

### Color Palette

---

<!-- TODO: dark blue, purple, black, gold or white, light green, light blue, yellow, light pink -->

---

### Logo

---

<!-- TODO: Create a logo, maybe on krita -->

---

### Font

---

<!-- TODO: Inter -->

---

## Functional Requirements

### User Roles And Permissions

<!-- - Define different user roles and their access levels.   -->

#### Administrator

---

**Role owner**: Maxime THIZEAU

**Permissions**:

> [!Tip] Can
>
> - See all users.
> - See database.
> - Modify UI/UX.
> - Add new undertakers.
> - Add new instances.
> - Add new templates.

> [!Caution] Can't
>
> - See mourners' personal information.
> - Have access to uploaded documents.

---

#### Undertakers

---

**Role owners**: Undertakers

> [!Tip] Can
>
> - See users account they created.
> - Access low privacy user database (full name, deceased information).

> [!Caution] Can't
>
> - See other users accounts.
> - Access other users accounts.
> - See mourner's personal information.
> - See database.
> - Modify instances.
> - Modify templates.

---

#### Mourners

---

**Role owners**: Mourners

> [!Tip] Can
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

> [!Caution] Can't
>
> - See database.
> - Access undertakers account.
> - Access other users account.
> - Modify deceased primary information (death date, full name, last location, birth date, birth location).

---

### System Features And Functions

<!-- - Provide detailed functional requirements, such as:
  - **Feature 1**: Description, inputs, outputs, behavior.
  - **Feature 2**: Description, inputs, outputs, behavior.
  - (Continue for all key functionalities.)   -->

---

---

### Application Workflow

---

<!-- TODO: Redo mermaids to fit excalidraw -->

```mermaid
graph TD
  %% Undertaker Flow
  subgraph Undertaker Flow
    A1[Registration/Login] -->|New User| A2[Register: Input company name, user name, password, email]
    A1 -->|Returning User| A3[Login: password, username]
    A2 --> HP[Home Page]
    A3 --> HP[Home Page]

    HP --> PP[Profile Page]
    HP --> UP[User Page]

    PP --> PP1[Edit Profile]
    PP --> PP2[Logout]

    UP --> UP1[Create Account]
    UP --> UP2[Delete Account]

    UP1 --> UP1.1[Add deceased information]
    UP1 --> UP1.2[Add mourner information]
  end
```

```mermaid
graph TD
  %% Mourner Flow
  subgraph Mourner Flow
    A1[Registration/Login] -->|New User| A2[Register: Input company name, user name, password, email]
    A1 -->|Returning User| A3[Login: password, username]
    A2 --> HP[Home Page]
    A3 --> HP[Home Page]

    HP --> PP[Profile Page]
    HP --> IP[Instance Page]
    HP --> TP[Template Page]
    HP --> LP[Letter Page]
  end
```

---

## Non-Functional Requirement

<!-- - **Performance**: Expected response times, scalability, etc.
- **Security**: Authentication, authorization, encryption needs.
- **Usability**: UI/UX expectations, accessibility.
- **Availability and Reliability**: Uptime, fault tolerance, backups.   -->

---

---

## Data Management

### Data Flow

<!-- - Describe how data moves through the system.
- Include data flow diagrams if necessary.   -->

### Database Schema

<!-- - Define key tables and relationships if applicable.   -->

## External Interfaces

<!-- - **APIs**: Describe any APIs the system will expose or consume.
- **Third-Party Integrations**: List any integrations with external systems.
- **Hardware Interfaces**: Describe interactions with physical devices if applicable.   -->

## Constraints And Limitations

<!-- - Highlight known constraints, such as technology limitations or compliance requirements.   -->

## Acceptance Criteria

<!-- - Define what constitutes successful implementation and acceptance by stakeholders.   -->

## Appendices

<!-- - Any additional supporting information, such as diagrams, references, or links to related documents. -->
