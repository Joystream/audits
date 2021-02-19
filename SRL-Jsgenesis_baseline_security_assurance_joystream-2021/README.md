# Joystream baseline security assurance

This review assesses the Joystream blockchain system’s existing protections against a variety of likely hacking scenarios and points out the most relevant weaknesses, all with the goal of improving the protection capabilities of the blockchain system.

This repository contains all deliverables created in the course of the project as well as an issue overview.

## Structure

| Folder        | Description           |
| :------------ | :-------------------- |
| 0-deliverables| Project deliverables  |
| 1-status      | Jour fixe slides      |
| x-resources   | Embeddable resources      |

## Issue overview

| Issue description | Severity | Reference |
| :------------ | :----------- | :-------- |
| Exponential complexity of weight calculation functions in multiple imported Substrate 2.0.0 pallets allows for Denial of Service attack, potentially stalling the blockchain           | Critical          | [#1](https://github.com/Joystream/audits/issues/1)       |
| Missing checks on the `referral_cut` value could enable creating unlimited membership accounts for free | Info | [#2](https://github.com/Joystream/audits/issues/2)|
| Members can undermine the intent of the `invite_member` extrinsic by inviting themselves to get free tokens | Low | [#3](https://github.com/Joystream/audits/issues/3) |
|In the commit-reveal voting scheme for referendums, UUID 4 is used for random salt generation instead of a cryptographic random generator | Info | [#4](https://github.com/Joystream/audits/issues/4) |
|No deposit is charged for creating forum posts and threads|Moderate|[#5](https://github.com/Joystream/audits/issues/5)|
|The `set_stickied_threads` extrinsic can be used to cheaply fill up the blockchain storage|Moderate|[#6](https://github.com/Joystream/audits/issues/6)|
|Account takeover via malicious membership invitation| Moderate | [#7](https://github.com/Joystream/audits/issues/7) |
|In referendums, the voting stake is only locked for balances transfer| Low | [#8](https://github.com/Joystream/audits/issues/8)|
|The existential deposit is configured to be 0|High|[#9](https://github.com/Joystream/audits/issues/9)|
|Multiple votes per user possible in the forum pallet via `vote_on_poll`|Low|[#10](https://github.com/Joystream/audits/issues/10)|


For each of the reported issues, we assign a severity based on its estimated impact when exploited:

| Severity	|Description        |
| ------------- | ----------------- |
|Critical	|Immediately exploitable under real-world conditions. Very high impact if exploited.|
|High		|Under real-world conditions, exploit requires greater attack effort to cause high or very high impact.|
|Moderate	|Minor exploit, exploit fragment, information leak, or best practice deviation. Real-world exploit, if possible, causes only low to moderate impact.|
|Low		|Not directly tied to a potential exploit. Low impact. Minor bug, information leak, or best practice deviation.|
|Info-level	|No direct security impact. Minor bug or best practice deviation.|

Critical and high severity issues need to be addressed right away. Moderate, low and info-level issues should be addressed in the next maintenance cycle.
