# Code Review Guidelines

"There is not one right way to do everything, only better ways and worse ways."

## Purpose of Code Reviews

While the following items are not the only reasons for a code review, they are important.

### Cross Training Development Team

- Get everyone familiar with the code, increasing the project's bus factor.
- Developers can learn new things from senior developers, increasing velocity.
- Senior developers can mentor developers, reducing technical debt.

### Finding Defects or Opportunites for Improvement

- Finding defects early in the development process, reducing cost of bugs and technical debt.
- Identification of possible enhancements.
- Improve readability of the code by following team style guidelines; enhances maintainability and reduces technical debt.

How do you know if your code is easily readable and understandable?

> Your peer tells you after reviewing the code. 
> 
> You cannot determine this yourself because you know more as the author than the code says by itself. A computer cannot tell you, for the same reasons that it cannot tell if a painting is art or not. Hence, you need another human - capable of maintaining the software - to look at what you have written and give his or her opinion. The formal name of said process is Peer Review."
 
[Reference](http://programmers.stackexchange.com/questions/141005/how-would-you-know-if-youve-written-readable-and-easily-maintainable-code/141010#141010)

## What Is **Not** The Purpose Of A Code Review?

- Nitpicking code. It's OK to say, "This looks good."
- Watching over developers. Trust developers.
- Arguing about style differences. Document them in style guides as a team.

## Checklist

### General

- Does the code work? Does it perform its intended function, the logic is correct etc.
- Is all the code easily understood?
- Does it conform to your agreed coding conventions and style guides?.
- Does the code follow the guidelines of SOLID, DRY, and YAGNI?
- Is there any commented out code?
- Can any of the code be replaced with built in functions?
- Can any logging or debugging code be removed?
- Does it have a low cyclomatic complexity?
- Are there any warnings or errors in the build?

### Security

- Are all data inputs checked (for the correct type, length, format, and range) and encoded?
- Where third-party utilities are used, are returning errors being caught?
- Are output values checked and encoded?
- Are invalid parameter values handled?
- Is all user input sanitized?

### Documentation

- Do comments exist and describe the intent of the code?
- Is any unusual behavior or edge-case handling described?
- Is the use and function of third-party libraries documented?
- Is there any incomplete code? If so, should it be removed or flagged with a suitable marker like ‘TODO’?

#### Testing

- Is the code testable? i.e. don’t add too many or hide dependencies, unable to initialize objects, test frameworks can use methods etc.
- Do tests exist and are they comprehensive? i.e. has at least your agreed on code coverage.
- Do unit tests actually test that the code is performing the intended functionality?

#### References 

http://blog.fogcreek.com/increase-defect-detection-with-our-code-review-checklist-example/
http://smartbear.com/SmartBear/media/pdfs/11_Best_Practices_for_Peer_Code_Review.pdf
http://programmers.stackexchange.com/questions/141005/how-would-you-know-if-youve-written-readable-and-easily-maintainable-code/141010#141010