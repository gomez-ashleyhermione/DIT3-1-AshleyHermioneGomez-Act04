---

### Reflection Questions

#### 1. How did you implement event handling for user actions?

For this activity, I implemented event handling by using the `setOnClickListener()` method on the Submit button. Basically, when the user taps the button, it calls a function I created called `handleSubmit()`. 

Inside that function, I first get the text from both input fields using `getText().toString().trim()`. The `.trim()` part removes any extra spaces at the beginning or end. Then I check if the fields are empty, and if they're not, I try to convert the age to a number. If everything is valid, the app shows the information in the TextView at the bottom. If something's wrong, it shows a Toast message telling the user what went wrong.

At first, I wasn't sure how to connect the button click to actually doing something, but after reading the documentation and trying it out, I realized `setOnClickListener()` is like telling the app "hey, when this button gets clicked, run this code." It's pretty straightforward once you understand the concept.

#### 2. What techniques ensured smooth and stable interaction?

To make sure the app doesn't crash and works smoothly, I used a few different techniques:

**First, I validated the inputs before processing them.** I check if the fields are empty right away, so the app doesn't try to process nothing. This prevents errors later on.

**Second, I used a try-catch block** when converting the age from text to a number. This was really important because if someone types letters instead of numbers, the app would normally crash. But with try-catch, it just catches the error and shows a friendly message instead.

**Third, I added an age range check (1-150)** because even though someone might enter a number, it doesn't mean it's realistic. So if they put 999 or 0, the app tells them to enter a valid age.

**Lastly, I used Toast messages** to give immediate feedback. Instead of making users guess what went wrong, the app tells them exactly what to fix. For example, "Please fill in all fields" or "Please enter a valid number for age." This makes the user experience way better.


#### 3. What improvements would you add in future versions?

If I had more time to work on this app, here are some things I'd definitely add:

Better input validation:
- Add an email field with proper validation to check if it's a real email format
- Add real-time validation that checks the input as you type, not just when you click submit
- Maybe add a password field with a strength meter to show if it's strong enough

More input options:
- Add radio buttons for selecting gender
- Include a dropdown (Spinner) for selecting your city or province
- Add checkboxes for things like agreeing to terms and conditions
- Use a DatePicker instead of typing age manually - it would be more accurate and user-friendly
  
Better design:
- Add some animations when showing success or error messages to make it more engaging
- Support dark mode because a lot of people prefer it
- Make the error messages appear directly under the input fields instead of just Toast messages
- Add icons next to the input fields to make it clearer what each field is for

Accessibility features:
- Make sure the app works well with TalkBack for visually impaired users
- Add support for larger text sizes for people who need it
- Make sure all colors have good contrast


Overall, this activity taught me a lot about how Android apps handle user input and respond to errors.

