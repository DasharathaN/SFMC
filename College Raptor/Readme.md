# CollegeRaptor Personalized Program Recommendation Email

A dynamic Salesforce Marketing Cloud (SFMC) email campaign that delivers personalized college program and scholarship recommendations using AMPscript and Data Extension lookups.

## Project Overview

This email uses customer and program data stored in Salesforce Marketing Cloud Data Extensions to generate tailored educational recommendations for each subscriber.

Based on the subscriber's Customer ID, the email dynamically retrieves:

- Program information
- Personalized banner image
- Program description
- Scholarship recommendations
- Award amounts
- Application deadlines
- Dynamic CTA content

## Business Scenario

A student visits CollegeRaptor and expresses interest in higher education opportunities.

When the student enters a nurturing journey, the email automatically recommends:

- Relevant academic programs
- Available scholarships
- Program-specific resources
- Personalized next steps

## Features

### Subscriber Personalization

The email personalizes content using:

- First Name
- Customer ID

Example:

```ampscript
SET @FirstName = AttributeValue("FirstName")
SET @CustomerID = AttributeValue("CustomerID")
```

### Data Extension Lookups

The solution retrieves data from multiple Data Extensions:

#### CustomerProgram_DE

Maps customers to educational programs.

#### Programs_DE

Stores:

- Program Name
- Banner URL
- Heading
- Description
- CTA

#### Scholarships_DE

Stores:

- Scholarship Name
- Award Amount
- Application Deadline
- Scholarship Description
- CTA

### Dynamic Content Areas

- Personalized greeting
- Dynamic hero banner
- Program recommendation section
- Scholarship recommendation section
- Dynamic call-to-action button

## Data Model

```text
CustomerProgram_DE
    |
    | CustomerID
    v
Programs_DE
    |
    | ProgramID
    v
Scholarships_DE
```

## AMPscript Functions Used

### AttributeValue()

Retrieves subscriber attributes.

```ampscript
AttributeValue("FirstName")
```

### Lookup()

Retrieves related records from Data Extensions.

```ampscript
Lookup(
    "Programs_DE",
    "ProgramName",
    "ProgramID",
    @ProgramID
)
```

## Email Sections

### Header

- CollegeRaptor branding

### Dynamic Banner

Displays a program-specific image.

### Personalized Introduction

Greets the subscriber by name.

### Program Recommendation

Displays:

- Program Name
- Program Description

### Scholarship Recommendation

Displays:

- Scholarship Name
- Scholarship Amount
- Application Deadline
- Scholarship Details

### Call To Action

Displays a dynamic CTA button based on the recommended program.

### Footer

Includes:

- Profile Center
- Unsubscribe Link
- Sender Information

## Technologies Used

- Salesforce Marketing Cloud
- AMPscript
- HTML Email Development
- Data Extensions
- Email Studio
- Personalization
- Dynamic Content

## Learning Objectives

This project demonstrates:

- AMPscript data retrieval
- Multi-Data Extension relationships
- Personalized email experiences
- Dynamic content rendering
- Scholarship recommendation workflows
- Educational marketing campaigns

## Project Structure

```text
CollegeRaptor-Program-Recommendation/
│
├── index.html
├── README.md
└── screenshots/
    ├── desktop-preview.png
    └── mobile-preview.png
```

## Screenshots

### Email Preview

![Email Preview](screenshots/desktop-preview.png)

### Mobile Preview

![Mobile Preview](screenshots/mobile-preview.png)

## Key Salesforce Marketing Cloud Concepts Demonstrated

- AMPscript Personalization
- Lookup Functions
- Subscriber Attributes
- Data Extensions
- Dynamic Content Blocks
- Journey-Based Email Personalization
- Educational Marketing Automation

## Author

Dhasharatha Nakirekanti

Salesforce Marketing Cloud Developer | Email Developer | Marketing

<img width="431" height="495" alt="image" src="https://github.com/user-attachments/assets/0119d601-61ce-4fe5-8337-7cf5aeb26ba8" />
<img width="478" height="484" alt="image" src="https://github.com/user-attachments/assets/b1d1a56f-a5b6-4afe-a4ac-6382ef0a2547" />

