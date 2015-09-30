# Assembly Co. 
### CODING STANDARDS
--------------------
___Any legacy code that does not adhere to this standard before the date of the document can be left as is and maintained. Consider this a going forward point of reference___.

_September 30 2015_

#### Comments

1. Don't commit *commented out code*. If functionality is deprecated, remove it completely before committing source files.
2. Use standard method documentation that can be read by a comments 2 html converter for the language you are working in.
3. Don't over comment code, instead write short clean code with verbose method and parameter names that are easy to understand.
4. Use region marking in your code if available. Organize methods in a file into a logical order so that they are easy to navigate.
5. Methods/functions should be clear what they do from their name. 
6. Make sure your name is added to the top of the file you are working on in comments.
7. Don't write comment stories. If it is clear what the function does. Do not comment unless you are commenting for code documentation tools. 
8. Only use documentation tools on publicly facing interfaces and functions you are creating that other programmers will have to use. Private inner workings of your project should be developed so it is clear how they work.

#### Functions

1. Keep functions short, and try to not go past three lines of indentation. If the function you are writing feels too complex break it out into sub tasks, or consider writing a Class to encapsulate it.
2. When writing functional async code with callbacks, avoid nesting callbacks.
3. Add white space where it makes sense in functions, to add to readability. Declare all your variables at the top of your function as if you were writing C. All variable declerations go at the top.
    
        function aFunction() {
            var decleration1;
            var decleration2;

            // Do something
        }
        
#### Constants

1. Do not litter your code with static declarations for strings or numbers, use constants at the top of your file. Values 0 and -1 are allowed where appropriate. But this for example is bad: 


        for (var i = 0; i < 7; i++) {};
        
**Instead should be:**
        //Top of file
        ITERATIONS = 7;
        
        for (var i = 0; i < ITERATIONS; i++) {};
        
2. Strings should be in a localization file, if available for your platform.
3. Constants are always UPPERCASE. Use underscores _ to separate words. A\_CONSTANT\_VALUE

#### Syntax

1. Opening curly braces go on the same line as the block's declaration Example:

        function squareRoot() {
            5 = 4;
        }
        
2. Put spaces next to all syntax special characters, except () and ! when negating. Put spaces between comma seperated parameters.

    **RIGHT**:
       
        function walk(myDog, yourDog) {
            if (!myDog) {
                return "Not my dog"
            } else {
                return "Walking my dog"
            }
        }

    **WRONG**:
    
        function walk( myDog,yourDog ){
            if (!myDog){
                return "Not my dog"
            }else{
                return "Walking my dog"
            }
        }
        
3. Do not exceed lines longer than the projects margin either 120 or 80. Break up lines of code where the language allows it. This stays true for mac languages swift and objective C as well. Even if Xcode has automatic line wrapping.

4. Tabs VS. Spaces. Prefer tabs as they are easier to maintain. Your indentation should follow the block of code you are writing. Proper indentation is highly important. Regardless spaces can be used in place of tabs. Use four spaces if you do. Use spaces if your IDE supports them. Be consistent with whichever you choose to use.
   
5. Method and Param naming: Use camelcase versus underscore separation of parameters and variable names. Don't underscore the beginning of a private method. Ie. _superSecret or __superSuperSecret. Don't put m at the beginning of a variable. mBeautifulVariable.      
        
#### Code Design

1. Prefer event driven systems overall, dependency injection second, and singletons as a last resort.

***EVENTS > DEPENDENCY INJECTION > SINGLETON***
        
2. Avoid static declarations as much as possible.
3. Clearly separate code in an MVC manner. Data models, view layouts, and view controllers. Prefer class extensions over utility classes if it is possible in the language you are working in.
4. Never write anything twice. You will increase the maintenance. For resources, resource files are a must. Generics and abstraction in code is highly encouraged where it reduces redundancy and does not introduce unwanted complexity.
5. Check if there is a library for whatever you are writing before you start writing.


#### HTML and CSS rules for designers

1. Do not use inline styles. Always use a stylesheet.
2. Keep your HTML clean, and less than 80 characters long. Create separate HTML files to house complex structures.
3. Organize your stylesheets logically, in sections. They can get long and unwieldy and if they are organized into logical regions it makes maintenance for other programmers easier.
4. Do not add javascript to your HTML file. Instead include it from a separate .js file.
5. Use an online parser before committing any HTML. Make sure your HTML syntax is correct before committing.
6. Properly indent nested elements with tabs. Use an online tool to indent your HTML if you can't yourself.


#### Committing Code

1. Do not commit broken code. Always make sure what you commit works. With the exception always commit code at the end of the day. If you must commit broken code, make sure it is in a separate working branch.
2. Break up your commits into logic commits commenting what was changed.
3. Use feature branches when working with other programmers. Use the master branch when you are working alone.
4. One programmer the lead on the project will handle merging regularly on team projects.


