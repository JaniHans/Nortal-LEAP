# AI Usage

Briefly describe how you used AI (tools, prompts, code snippets, fixes). Be concise and honest (using AI is fine; it's just a tool; we want to know your method). If you did not use AI, state that here.

1. I have been using Maven on SpringBoot so I wanted to understand how to run gradle and indeed AI was helfpul noting that I was using JDK 23 whilst in our gradle.settings section there was 21
2. I was discussing why front end is not rendering in chrome. In this case I figured it out my own it was due to the use of VPN. Still i was able to discuss the problem. So I guess it was 1:1

## No more AI use, backend business logic was done by myself
Some problems still remain with error handling with messages in the front end, but not only. It seems in the backend I am throwing invalid request in the exception handler, 
but controllers are setup in a certain way that expect a boolean value true from the returnBook method in service. I might be wrong, also depending on the return value you could manipulate the front messaging.
Added count field for member entity to avoid pulling all books from the database.
Rest of the logic was done mostly by if statement checks and a few additional method additions.

## Fixed
Fixed borrowAndReturnHappyPath() integration test method. I was returning a more UI friendly messaging instead the test is expecting null if there is no nextmember in the reservation que.
Also changed back  ResultNext boolean value to true, as our controller expecting a true value there.