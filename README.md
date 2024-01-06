# Turbo Terrier
The BU Registration Bot
---

**Author:** [Muhammad Aseef Imran](https://www.linkedin.com/in/aseef/)

**Website:** https://turboterrier.com/

**Email:** support@turboterrier.com

## What is Turbo Terrier
Turbo Terrier is a software application designed to automatically register you Boston University students for their target course(s) as soon as a slot is detected open. This project is currently a work in progress and has not yet launched to the public.

## Components
This project is divided into three major components. As a proprietary software, **not all components of Turbo Terrier** are open source.

* Registration Bot [closed source]: The heard and soul of Turbo Terrier, the Registration Bot is where the magic is happening. The Registration Bot runs on the consumers own machines. This python registration bot then uses the selenium web framework to automatically scan the BU Student Link for open courses and register students for their target courses. To ensure's security of the user's university credentials, all sensetive data is only stored after being encrypted and never leaves the user's device except for connect to the Boston University servers. In order to prevent application cracking and pirating, the end consumer software is obfuscated uses Pycharm and distributed in a packed, executable format for user accessibility. The application further signs and verifies most communication with the backend server using public and private keys to ensure the integrity of the communication.

* [The Rust Backend](https://github.com/Turbo-Terrier/Rust-Backend) [open source]: The Rust Backend is the cloud backend that serves multiple purposes. First, the HTTP server is the backend for the front-facing react site (as on https://turboterrier.com). Second, the Rust Backend also doubles are as a licensing and cloud monitoring server where data relating to the Registering Bot's usage is also collected and stored. The backend signs all communication it conducts with the Registration Bot on the consumer side. Finally the Backend uses MySQL to facilate its data storage.
  
* The React JS Frontend [open source]: The Frontend is built uses the Bootstrap CSS framework alongside React for a rich interface. (Note: as of 1/4/24, no code relating to the React JS front end has been pushed onto github)

## Languages
This project is built with the following languages and major framewokrs:
* Rust:
  * Actix-Web
  * Ring
  * SQLx
  * Async-Stripe
  * Tokio
* HTML/CSS
  * Bootstrap
* Javascript
  * React
* Python
  * Selenium
  * Cryptography
  * PyArmor
* MySQL
