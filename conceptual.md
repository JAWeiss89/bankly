### Conceptual Exercise

Answer the following questions below:

- What is a JWT? ---- JWT is a way to authenticate users and information sent between user and server. It uses a secret key to sign the token and verify the authenticity of the request however unlike Flask Sessions, it doesn't use cookies.

- What is the signature portion of the JWT?  What does it do? --- The signature portion is what is used to authenticate the request by using it to make sure the message wasn't modified along the way. 

- If a JWT is intercepted, can the attacker see what's inside the payload? --- Yes, the payload is not encrypted and uses a common algorithm to reverse the payload portion of the token into the string. 


- How can you implement authentication with a JWT?  Describe how it works at a high level. --- Once it is installed as a depenedency, you require it in your application and set it to a variable. It comes with a method to sign a piece of information. The method requires you use a secret key as this is what will be used to compare future incoming requests with tokens. By comparing the token, you can see if it originally was signed by our servers, thus authenticating the request.

- Compare and contrast unit, integration and end-to-end tests.--- Unit test is used to test a component of an application. Usually this means a function but it isn't restricted to it as long it can still be considered a unit of the application with expected inputs and outputs. Integration tests is used to test how multiple units work together to assess if they are functioning as intended. For example, in the case of routes, if there are functions used within the route to process a request, we can use unit tests to ensure they work properly. We can then use integration tests to see if those same functions are working in the context of where they are being used by checking what type of response is sent by the server given a certain request. End-to-end tests are made to ensure the application works as intended when a user is interacting with it. For example, if a certain button is clicked on the site, does our application respond in the way we intend? This is what end-to-end checks for. 

- What is a mock? What are some things you would mock? --- Mock simulates a user's action with the application.

- What is continuous integration? --- Continuous integration is when developers are pushing code into a repository and the owner is constantly implementing it into the main code. 

- What is an environment variable and what are they used for? --- Environment variables live on the server machine and are not accessible by users of an application. Because of this, it is a way to store private information that the app depends on. Things like secret keys or API keys can be stored as environment variable. 

- What is TDD? What are some benefits and drawbacks? --- TDD or test-driven development is an approach to programming in which you first write the tests for a function or application before actually writing the code for it. As you begin to develop the app or function, more tests begin passing and it becomes a way to measure progress on the devevelopment of the program you are writing. It is useful in many ways. For one, it's a way to throughly plan out the app you will be creating by describing the expected inputs and outputs so there is more of an investment to planning out functionality. The down side is that it takes time to do this and often times, as you progress through the development process, you may realize that things should work a different way and so those tests you initially wrote will no longer work. 

- What is the value of using JSONSchema for validation? --- Using JSONSchema for validation is a very efficient and easy way to check that the request body is formatted correctly thus providing us with a way to handle one errors with the request. 

- What are some ways to decide which code to test? --- You should be testing all functions you create. All routes should also be tested including requests that are made correctly and ones that are not as a way to show you are handling errors in the application. When interacting with a database, it's better to test the application itself rather than the database directly. 

- What are some differences between Web Sockets and HTTP? --- With HTTP, a server responds to requests and will never respond unless a request was sent to it. The channel of communication is opened and closed as requests get made. With Web Sockets, however, those channels stay open and a server is able to send information to a client even if it didn't request it. Web sockets allow for real-time updates that are very useful in live gaming and chat applications as well as GPS - all situations where data is frequently changing and the server needs to let the client know of these changes the moment they happen. 

- Did you prefer using Flask over Express? Why or why not (there is no right 
  answer here --- we want to see how you think about technology)? --- When I first started using Flask and Python, I really enjoyed it because it seemed so straightforward, however, I've gotten more appreciation for Express with time. To the point now where I actually prefer using Express. It is more files and requires a bit more code but I feel like I am able to follow more closely what exactly is happening at every step. 
