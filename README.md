# EXP-3-PROMPT-ENGINEERING-
```
MOHAMED ABRAR M
212223040111
```
## Aim: 
Evaluation of 2024 Prompting Tools Across Diverse AI Platforms: 
ChatGPT, Claude, Bard, Cohere Command, and Meta
Experiment:
Within a specific use case (e.g., summarizing text, answering technical questions), compare the performance, user experience, and response quality of prompting tools across these different AI platforms.

## Algorithm:
1. Define the Use Case: oSelect a specific task for evaluation across platforms (e.g., summarizing a
document, answering a technical question, or generating a creative story / Code).  Ensure the use
case is applicable to all platforms and will allow for comparison across response quality, accuracy,
and depth.
2. Create a Set of Prompts:  Prepare a uniform set of prompts that align with the chosen use case. 
Each prompt should be clear and precise, ensuring that all platforms are evaluated using the same
input.  Consider multiple prompts to capture the versatility of each platform in handling different
aspects of the use case.
 3. Run the Experiment on Each AI Platform:  Input the prompts into each AI tool (ChatGPT,
Claude, Bard, Cohere Command, and Meta) and gather the responses.  Ensure the same conditions
are applied for each platform, such as input format, time to respond, and prompt delivery.  Record
response times, ease of interaction with the platform, and any technical issues encountered.
 4. Evaluate Response Quality: Assess each platform’s responses using the following criteria:
Accuracy,Clarity,Depth,Relevance
 5. Compare Performance: Compare the collected data to identify differences in performance across
platforms.  Identify any platform-specific advantages, such as faster response times, more accurate
answers, or more intuitive interfaces. 
## Prompt
Given a string. the task is to check if the string is symmetrical and palindrome or not. A string is said to be symmetrical if both the halves of the string are the same and a string is said to be a palindrome string if one half of the string is the reverse of the other half or if a string appears the same when read forward or backward. Use python and get input from user .
## Output
### Chat-GPT:
```py
# Program to check if a string is symmetrical and palindrome

# Taking input from user
string = input("Enter a string: ")

# Check for symmetrical
mid = len(string) // 2

if len(string) % 2 == 0:
    first_half = string[:mid]
    second_half = string[mid:]
else:
    first_half = string[:mid]
    second_half = string[mid+1:]   # skip middle char for odd length

if first_half == second_half:
    print("The string is Symmetrical")
else:
    print("The string is Not Symmetrical")

# Check for palindrome
if string == string[::-1]:
    print("The string is Palindrome")
else:
    print("The string is Not Palindrome")
```
<img width="392" height="148" alt="image" src="https://github.com/user-attachments/assets/b21a7a68-b031-4f39-9c29-ebdfb6a424e4" />


### Gemini:
```py
def check_symmetrical_and_palindrome(input_string):
    """
    Checks if a string is symmetrical and/or a palindrome.

    Args:
        input_string: The string to be checked.

    Returns:
        A tuple containing two boolean values: (is_symmetrical, is_palindrome).
    """
    n = len(input_string)
    
    # Check for palindrome
    is_palindrome = input_string == input_string[::-1]

    # Check for symmetrical
    is_symmetrical = False
    if n % 2 == 0:
        mid = n // 2
        if input_string[:mid] == input_string[mid:]:
            is_symmetrical = True
    else:
        mid = n // 2
        if input_string[:mid] == input_string[mid+1:]:
            is_symmetrical = True
    
    return is_symmetrical, is_palindrome

# Get input from the user
user_input = input("Enter a string: ")

# Check the string
symmetrical, palindrome = check_symmetrical_and_palindrome(user_input)

# Print the results
if symmetrical and palindrome:
    print("The string is both symmetrical and a palindrome.")
elif symmetrical:
    print("The string is symmetrical but not a palindrome.")
elif palindrome:
    print("The string is a palindrome but not symmetrical.")
else:
    print("The string is neither symmetrical nor a palindrome.")
```
<img width="529" height="140" alt="image" src="https://github.com/user-attachments/assets/483eeff7-c1cd-4d72-a575-a48eae99b1d4" />

### Copilot:
```py
def check_symmetry_and_palindrome(s):
    length = len(s)
    mid = length // 2

    # For symmetry, compare both halves
    if length % 2 == 0:
        first_half = s[:mid]
        second_half = s[mid:]
    else:
        first_half = s[:mid]
        second_half = s[mid+1:]

    is_symmetrical = first_half == second_half
    is_palindrome = s == s[::-1]

    # Output results
    print(f"\nString: '{s}'")
    print("Symmetrical:", "Yes" if is_symmetrical else "No")
    print("Palindrome:", "Yes" if is_palindrome else "No")

# Get input from user
user_input = input("Enter a string: ")
check_symmetry_and_palindrome(user_input)
```
<img width="372" height="206" alt="image" src="https://github.com/user-attachments/assets/b09bbe9a-46a8-409b-ad0d-54dfd03c6799" />

## SUMMARY::
1. ChatGPT:
    1. Strengths: Provides clear explanations and is good for general coding assistance, but may not
  always deliver the most accurate or optimized code on the first attempt.
     2. Experience: Likely found it helpful for understanding concepts and getting stepby-step
  guidance but needed adjustments for the code to work perfectly.
2. Gemini:
   1. Strengths: Provides a clean, modular function (check_symmetrical_and_palindrome) with clear docstrings and returns values in a structured way (tuple). Code readability is high, and the separation of logic (function + user         interaction) makes it reusable. The symmetry check correctly handles both even and odd lengths, and the palindrome check is concise using slicing.
    2. Experience: Likely found it very professional and easy to integrate into larger projects because of its function-based design. The tuple return allows flexible usage, not just direct printing. However, it might feel slightly more complex for beginners compared to a straightforward script, since it uses function returns and branching logic.

3. Copilot:
   1. Strengths: Generates a straightforward and concise implementation. The function directly handles both symmetry and palindrome checks, then prints results in a user-friendly format without extra branching. Very beginner-friendly since it avoids tuples, docstrings, or modular returns, and instead outputs clear "Yes/No" answers. Great for quick testing and immediate results.

   2. experience: You likely found it very fast to test with minimal complexity. Easy to understand for small scripts or classroom assignments. However, it is less modular than Gemini’s version—since results are printed inside the function, it’s harder to reuse in larger projects where return values would be needed. It also lacks comments or structured documentation, so while concise, it may not teach concepts as clearly as ChatGPT’s or Gemini’s versions.
## Result
Thus successfully evaluated all the AI models based on prompting with coding scenario.
