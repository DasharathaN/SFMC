# SFMC Welcome Email Campaign

A personalized welcome email template built in Salesforce Marketing Cloud (SFMC) using HTML and AMPscript.

## Overview

This project demonstrates how to create a dynamic welcome email for new customers using Salesforce Marketing Cloud personalization capabilities.

The email displays customer information and dynamically generates promotional offers based on the customer's loyalty tier.

## Features

- Personalized customer greeting using First Name
- Dynamic offer generation using AMPscript
- Loyalty-tier based marketing offers
- Responsive HTML email layout
- Profile Center link
- Unsubscribe link
- CAN-SPAM compliant sender information
- Customer-specific content rendering

## AMPscript Logic

The email assigns a promotional offer based on the customer's loyalty tier:

| Loyalty Tier | Offer |
|-------------|---------|
| Gold | 25% OFF on next purchase |
| Silver | 15% OFF on next purchase |
| Others | 10% OFF on next purchase |

Example:

```ampscript
%%[
IF LoyaltyTier == "Gold" THEN
SET @Offer = "25% OFF on your next purchase"
ELSEIF LoyaltyTier == "Silver" THEN
SET @Offer = "15% OFF on your next purchase"
ELSE
SET @Offer = "10% OFF on your next purchase"
ENDIF
]%%
```

## Personalization Fields

The template uses the following subscriber attributes:

- FirstName
- CustomerID
- Country
- Status
- LoyaltyTier

## Technologies Used

- Salesforce Marketing Cloud
- AMPscript
- HTML5
- Inline CSS
- Email Studio

## Sample Output

The email includes:

- Personalized Welcome Message
- Customer Details
- Loyalty Tier Information
- Dynamic Promotional Offer
- Member Benefits Section
- Call-to-Action Button
- Profile Center and Unsubscribe Links

## Learning Objectives

This project demonstrates:

- AMPscript conditional logic
- SFMC personalization techniques
- Dynamic content rendering
- Email template development
- Marketing automation best practices

## Author

Dhasharatha Nakirekanti

Salesforce Marketing Cloud Developer

<img width="338" height="464" alt="welcome emailer" src="https://github.com/user-attachments/assets/2ddcaf70-7866-471c-b7e1-d896f0ea97b2" />

