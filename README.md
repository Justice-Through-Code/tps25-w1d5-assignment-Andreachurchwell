# TPS25 - W1D5 - Python APIs: Dog Image Browser

## Assignment Overview

You will build a Python script that interacts with the Dog CEO REST API to create a Dog Image Browser. The application allows users to view a list of all available dog breeds, get random images of specific breeds, and get random images of specific sub-breeds. You'll use the `requests` library to make HTTP requests and handle API responses using `try/except` blocks.

## Learning Objectives

- Use the `requests` library to make HTTP GET requests to a REST API  
- Parse JSON responses from API calls  
- Handle API errors and connection issues using `try/except` blocks  
- Work with nested data structures (dictionaries and lists)  
- Write clean, modular, and testable code  
- Run and understand test results using `unittest`  
- Recognize pass/fail status from GitHub Classroom autograding

---

## Getting Started with GitHub Classroom and Codespaces

### Accepting the Assignment

1. Click on the GitHub Classroom assignment link provided by your instructor  
2. Authorize GitHub Classroom if prompted  
3. Accept the assignment  
4. Wait for your repository to be created  

### Opening the Assignment in Codespaces

1. Once your repository is ready, click the "Code" button  
2. Select the "Codespaces" tab  
3. Click **Create codespace on main**  
4. Wait for the Codespace to set up — this may take a few minutes

---

## Files Included

Your Codespace contains:

- `dog_api.py` — Starter file with comments to guide your implementation  
- `dog_api_tests.py` — Test suite to validate your logic (**do not modify**)  
- `.github/` — GitHub Classroom autograding configuration (**do not modify**)  
- `README.md` — This file  
- `.gitignore` — Standard Python ignore file  
- `requirements.txt` — Declares the `requests` dependency  

---

## Instructions

### Complete the following in `dog_api.py`:

#### Implement the following functions:

- `get_random_image(breed)`  
  - Calls `https://dog.ceo/api/breed/{breed}/images/random`  
  - Returns the image URL or an appropriate error message  

- `get_random_sub_breed_image(breed, sub_breed)`  
  - Calls `https://dog.ceo/api/breed/{breed}/{sub_breed}/images/random`  
  - Returns the image URL or handles errors  

- `show_breeds()`  
  - Fetches all breeds and prints them sorted, 5 per line  

#### Complete the main menu logic:

- Display a menu with options to view breeds or fetch images  
- Validate user input (e.g., check if breed or sub-breed exists)  
- Handle errors gracefully and allow the user to try again  
- Use `try/except` blocks to handle request and input errors  

---

## Example Output

```
What would you like to do?
1. Show all breeds
2. Get a random image from a breed
3. Get a random image from a sub-breed
4. Exit

Enter your choice (1-4): 2
Enter breed name: husky
Random image URL for husky: https://images.dog.ceo/breeds/husky/n02110185_10047.jpg
```

---

## Error Handling

Your application should handle the following gracefully:

- Invalid menu options  
- Invalid or non-existent breeds  
- Breeds with no sub-breeds  
- Invalid sub-breed names  
- API connection errors or unexpected responses  

Display helpful error messages and allow the user to try again.

---

## Testing

### Run the test suite:

```bash
python -m unittest dog_api_tests.py -v
```

### Manually test your program:

```bash
python dog_api.py
```

---

## GitHub Classroom Autograding

GitHub Classroom automatically runs your test suite after every push.

### To trigger autograding:

```bash
git add .
git commit -m "Complete Dog API Browser"
git push
```

### Then return to your GitHub repository:

- ✅ You will see a **green check mark** if all tests pass  
- ❌ You will see a **red X** if any test fails  

> ⚠️ You must push your code before GitHub Classroom can grade it.  
> You do **not** need to use the GitHub "Actions" tab.

---

## Submission Guidelines

1. Complete your implementation in `dog_api.py`  
2. Commit and push all changes to your GitHub Classroom repository  
3. Run `python -m unittest dog_api_tests.py -v` in your terminal to confirm tests pass  
4. Take **two screenshots**:
   - ✅ One showing the passing test output in your terminal  
   - ✅ One showing the green check mark in your GitHub repo after pushing  
5. Submit both your GitHub repository link and the screenshots through Canvas


### Citing:
### This project was completed with assistance from ChatGPT (OpenAI),
### used for guidance on Python syntax, error handling, and API integration.
## Acknowledgments

This project was created using the Dog CEO API. I received guidance and code assistance from ChatGPT (OpenAI) for writing functions, handling errors, and structuring the main program logic.

