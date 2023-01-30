### Conceptual Exercise

Answer the following questions below:

- What is a JWT?
- A JWT is a token that contains a 3 parts. It contains a header, payload, and verify signature. The header and payload contain information that is not encrypted and can be easily decoded. However, the signature contains a mixture of the header, payload, and a secret code. This is encrypted and allows the token to be unique. It can only be decoded by the originator of the token since they are the only ones who know the secrete. This can be used to authenticate that a user is logged in, and it can be sent only when authentication is needed, unlike cookies. Also, this authentication can be shared among other websites, so you can have one authentication point for many sites. This is simillar to what Google does with their services. 

- What is the signature portion of the JWT?  What does it do?
- the signature contains a mixture of the header, payload, and a secret code. This is encrypted and allows the token to be unique. It can only be decoded by the originator of the token since they are the only ones who know the secrete.

- If a JWT is intercepted, can the attacker see what's inside the payload?
- The attacker would be able to see what is inside the payload.

- How can you implement authentication with a JWT?  Describe how it works at a high level.
- First within your application server you need to make sure that you have the JWT package installed. Then when someone request loggin information you can create a token for them, using the secret key, and send it back to the user. Then, wherever the user wants to access a route that requires authentication, they can send the JWT token to the server. The server will then decode the information, and verifty the signature. If succeful the user will be granted access to the route.  

- Compare and contrast unit, integration and end-to-end tests.
- Unit tests will test a single function to make sure that it does whats its supposed to do. Integration tests will test how multiple functions integrate with one another to achive the desired result. End-to-end testing will test the experience from the users point of view. 

- What is a mock? What are some things you would mock?
- Mocking allows you to simulate certain variables that would usually be random or unpredictable. Some things that you would mock would be external API's, certain methods (like math.random), and in general anything that wont give a consistant result. 

- What is continuous integration?
- Continuous integration is when you work on a project together with many individuals and ensure you push your code on a consistent basis, that way everyone has the most up to date code. It also ensures that you are up to speed with everyone else's code.  

- What is an environment variable and what are they used for?
- They are used to set certain parameters for your application. Its also used to tell the application whether is running in testing mode, or production mode and which database to access. 

- What is TDD? What are some benefits and drawbacks?
- Test driven development, or TDD, is where you write tests first before you actually write the function. Then when you write the function you do so in a way that it passes the tests. Then you can go and refactor your code and add more complex tests. Some of the benefits are that it really helps you to organize your thoughts before you write the function. It also helps you to understand exactly what your function is doing, therefore you have a deeper understanding of the flow of data in your application. However, some of the drawbacks are increased time for production. It takes much longer to implements a new feature when you have to write tests first. However another argument in favor of TDD is that you will spend less time debugging your code later. 

- What is the value of using JSONSchema for validation?
- It allows you to use Javascript to ensure that your data is correct BEFORE you even send it to the database. It's very easy to set up, and will help to generate readable errors.

- What are some ways to decide which code to test?
- In general you can think about what code seems more prone to errors. How complex is your function? The more complex something, the more likely there could be problems. Therefore you want to spend more time writting tests for those functions. Also, most of your testing should be unit tests. They help ensure that every piece of the app is working individually. This is followed by integration tests, and then end-to-end tests. 

- What does `RETURNING` do in SQL? When would you use it?
- RETURNING will return whatever columns you tell it to return when you insert or update something in a database. This is useful to confirm that the insertion was successful. 

- What are some differences between Web Sockets and HTTP?
- Web Sockets are like a tunnel of continous connection between a client and a server. HTTP is more like a letter. You send information, then wait for a respose back. The Web Sockets the server and push data down to the clients without there being a request. And this can happen vice versa. 

- Did you prefer using Flask over Express? Why or why not (there is no right answer here --- we want to see how you think about technology)?
- I personally prefer Express. Perhaps its simply because of my familiarity with javascript but I do feel that it was easier to use. I also really like the idea of using one language to write both the front end and back end. Also I really liked the ability to use the chrome dev tools with Node js. 

