# Assembly Co. 
### CODING STANDARDS
--------------------
___Any legacy code that does not adhere to this standard before the date of the document can be left as is and maintained. Consider this a going forward point of reference___.

_September 30 2015_

#### Comments

1. Don't commit *commented out code*. If functionality is deprecated, remove it completely before commiting source files.
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

#### Syntax

1. Opening curly braces go on the same line as the block's decleration Example:

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
4. Add white space where it makes sense in functions, to add to readability. Declare all your variables at the top of your function as if you were writing C. All variable declerations go at the top.
    
        function aFunction() {
            var decleration1;
            var decleration2;

            // Do something
        }
        
5. Tabs VS. Spaces. Prefer tabs as they are easier to maintain. Your indentation should follow the block of code you are writing. Proper indentation is highly important. Regardless spaces can be used in place of tabs. Use 4(four) spaces if you do. Use spaces if your IDE supports them. Be consitant with which ever you choose to use.
        
        
#### Code Design

1. Prefer event driven systems over all, dependecy injection second, and singletons as a last resort.

***EVENTS > DEPENDECY INJECTION > SINGLETON***
        
2. Avoid static declerations as much as possible.
3. Clearly seperate code in an MVC maner. Data models, view layouts, and view controllers. Prefer class extensions over utility classes if it is possible in the language you are working in.
4. Never write anything twice. You will increase the maintenance. For resources, resource files are a must. Generics and absrtaction in code is highly encouraged where it reduces redundancy and does not introduce unwanted complexity.
5. Check if there is a library for whatever you are writing before you start writing.


#### HTML and CSS rules for designers

1. Do not use inline styles. Always use a stylesheet.
2. Keep your HTML clean, and less than 80 characters long. Create seperate HTML files to house complex structures.
3. Organize your stylesheets logically, in sections. They can get long an unweidly and if they are organized into logic regions it makes maintenance for other programmers easier.
4. Do not add javascript to your HTML file. Instead include it from a seperate .js file.
5. Use an online parser before commiting any HTML. Make sure your html syntax is correct before commiting.
6. Properly indent nested elements with tabs. Use an online tool to indent your HTML if you can't yourself.
