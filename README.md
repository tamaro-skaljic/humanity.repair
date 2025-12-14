# [Humanity Repair](https://humanity.repair)

## Mission Statement

Humanity Repair is intended to become a social media platform that aims to unite rather than divide.
Its goal is to organize and carry out a global, peaceful revolution to achieve a collective vision.

## The Reason

TODO

## The Vision

### Right to initiatives

People have the right to launch initiatives to change or amend the constitution or laws.

### The Right for Referendum

Humanity Repair believes in the power of collective decision-making. Every member has the right to call for a referendum on important issues affecting the community. This ensures that all voices are heard and that decisions are made democratically.

## (Unique) Selling Points

### Hosted only in the European Union (EU)

- The platform will be hosted only in the European Union (EU), which has some of the strictest data protection laws in the world ([GDPR](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng)).

### Decentralization

- Should be built on a decentralized architecture.

### Identity Verification

- While the remaining internet is a de facto lawless place, this platform is not.
- Every user has to verify their identity using a government-issued ID during account creation, therefore it should not be possible to create multiple accounts as a human.
- Identity verification is done by a third-party service, which ensures that the platform itself does not have access to users' personal information.
- The third-party service will hash the user's ID using a one-way hash function, deletes the user data and sends the hash to the platform.

### Community Moderation

- If a user is found to be violating the platform's rules, their account can be temporarily or permanently suspended.

### Do Not Sell My Personal Information

- Data will never be sold to anyone. You don't have to opt-out and you aren't able to opt-in.

## Licensing

Humanity Repair is dual-licensed under both the [MIT License](https://choosealicense.com/licenses/mit/) and the [Apache License (Version 2.0)](https://choosealicense.com/licenses/apache-2.0/) and therefore Open Source.

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in this crate by you, as defined in the Apache-2.0 license, shall
be dual licensed as above, without any additional terms or conditions.

```txt
Table: vision
Columns:
- id
- title -- Usually just a few words.
- abstract -- A concise and comprehensive overview of the purpose and contents of the entire vision, so that a reader can decide whether reading it will be useful.
- motivation -- The motivation of the vision.
- changes -- The changes the vision will bring.
- normative_references -- Normative references specify sources that must be read to understand the vision.
- informative_references -- An informative reference only provides additional information.

Table: human_generated_content
Columns:
- id
- user_id -- Foreign key to user table.
- content -- The content of the human generated content.

Table: reported_human_generated_content
Columns:
- id -- Foreign key to human_generated_content table.

Table: human_generated_content_reporter
Columns:
- id -- Foreign key to user table.
- human_generated_content_id -- Foreign key to human_generated_content table.

Table: user
Columns:
- id
- user_phrase -- A unique phrase that does not reveal the user's identity.
- identity_hash -- A hash of the user's government-issued ID.
```
