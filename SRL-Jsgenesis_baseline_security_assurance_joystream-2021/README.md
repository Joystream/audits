# Joystream baseline security assurance

This review assesses the Joystream blockchain system’s existing protections against a variety of likely hacking scenarios and points out the most relevant weaknesses, all with the goal of improving the protection capabilities of the blockchain system.

This repository contains all deliverables created in the course of the project as well as an issue overview.

## Structure

| Folder        | Description           |
| ------------- | --------------------- |
| 0-deliverables| Project deliverables  |
| 1-status      | Jour fixe slides      |
| x-resources   | Embeddable resources      |

## Issue overview

| Issue description | Severity | Reference |
| ------------- | ------------ | --------- |
| Exponential complexity of weight calculation functions in multiple imported Substrate 2.0.0 pallets allows for Denial of Service attack, potentially stalling the blockchain           | Critical          | #1       |

For each of the reported issues, we assign a severity based on its estimated impact when exploited:

| Severity	|Description        |
| ------------- | ----------------- |
|Critical	|Immediately exploitable under real-world conditions. Very high impact if exploited.|
|High		|Under real-world conditions, exploit requires greater attack effort to cause high or very high impact.|
|Moderate	|Minor exploit, exploit fragment, information leak, or best practice deviation. Real-world exploit, if possible, causes only low to moderate impact.|
|Low		|Not directly tied to a potential exploit. Low impact. Minor bug, information leak, or best practice deviation.|
|Info-level	|No direct security impact. Minor bug or best practice deviation.|

Critical and high severity issues need to be addressed right away. Moderate, low and info-level issues should be addressed in the next maintenance cycle.
