## Week Four - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's your favorite project management tool?
I tend to prefer Waffle because of its simplicity and easy girhub integration, can also effectively
get around Pivitol tracker if neccessary.

2. Why do we create staging environments?
We create staging environments to give us as close to a true production environment as possible
where we can test new features and bug fixes without effecting our users. It is ideal for getting
feedback at closer to scale as opposed to a local development environment.

3. What are the characteristics of a good README (in your opinion)?
A good readme will ideally have:
* clear instructions for installation on common environments
* clear explanation of what the application does
* list technologies used in the stack
* code examples
* instruction for setting up a local dev environment
* screeb shots or gifs when applicable

4. What's one main improvement you're going to make to your code regarding accessibility issues?
I am going to be more diligent about alt text and labels for images and links as well as implementing
tabibdex in form heavy pages.

5. What are some basic security concerns to be aware of when building applications?
* cross site scripting
* cross site request forgery
* click jacking(be wary of iframes)
* injection attacks(caredul with sql)
* man in the middle attacks(encrypt things)

6. Why is continuous integration helpful/important?
Continuous integration is important because it gives us an automated safety net. It helps us make sure
that code we push passes our test suite before every merge and holds us accountable to those tests. It
also improves development flow wheb it incorporates continuous deployment by automatically performing
common operations in sequence.

7. What are some continuous integration tools?
* Travis CI
* Jenkins
* Circle CI

#### Review  

8. What are some characteristics of "good" git workflow?
* Commiting often with detailed and contextual comments
* One branch per feature
* Addressing merge conflicts locally
* Using rebase when appropriate(such as when the branch above your current working one has been updated)

9. What are the four fundamental concepts of object oriented programming?
* Abstraction
* Encapsulation
* Inheritence
* Polymorphism

10. What's a module in Ruby and what's the difference between a class and a module?
A module in ruby is a place you store code that will be shared in multiple places. It can also be used to create a namespace
for multiple classes and methods. It can be either extended(provides class methods) or included(provides instance methods) in a class. The core differebce vetween a module and class is that a class can ben instantiated but a module cannot, it is simply a collection of things.
