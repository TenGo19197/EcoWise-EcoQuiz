# EcoWise – EcoQuiz Testing Report
**Project:** EcoWise – Sustainable Development Goal 12: Responsible Consumption and Production
**Developer:** Tenkhiz Sichinava
**Module:** Web Design and Development
**Educational Institution:** National College of Ireland (NCI)

## 1. Testing Objectives
This test aims to verify the correct functionality of the "EcoQuiz" feature, the accuracy of feedback, the precision of score calculations, and proper display across both desktop and mobile devices.
The test includes 10 questions on sustainable development; 5 questions are randomly selected for each game session.

## 2. Functional Testing
| Test Item | Expected Result | Status |
|---|---|---|
| Start Quiz | Displays the first question; score is set to "0/5" | Completed |
| Random Question Selection | Randomly selects a question from a pool of 10 | Completed |
| Next Question | Advances to the next question after an answer is submitted | Completed |
| Correct Answer | Displays an encouraging message and adds 1 point | Completed |
| Incorrect Answer | Displays an error message and shows the correct answer | Completed |
| No Answer Selected | Displays "Please select an answer!" | Completed |
| Answer Locking | The answer cannot be changed once submitted | Completed |
| Progress Indicator | Updates as each of the 5 questions is answered | Completed |
| Results Interface | Displays the final score after 5 questions have been answered | Completed |
| Score-Based Information | Displays different information based on the final score | Completed |
| Try again | Resets the score, returns to question 1 and starts a new game | Passed |

## 3. Results Testing
The following results were tested:
- **0/5:** Displays the correct score and an encouraging message.
- **1/5:** Displays the correct score and an encouraging message.
- **2/5:** Displays the correct score and an encouraging message.
- **5/5:** Displays "Perfect score! You are an environmental expert!"
The scoring system awards 1 point for each correct answer, with a maximum possible score of 5/5. ## 4. Responsive Design Testing
The website was tested using Google Chrome Developer Tools.
**Device:** iPhone 16 (emulated)
**Screen width:** 393 pixels
The following elements were verified:
- Responsive navigation menu
- Quiz layout
- Answer selection area
- Progress bar
- Final results page
- "Try Again" and "Return to Home" buttons
**Result:** Each layout displayed correctly at the emulated mobile screen width, with no unexpected horizontal overflow.

## 5. Bugs Discovered and Fixes
### Bug 1 – Duplicate "Next Question" Button
**Issue:** Due to a duplicate `id="nextBtn"` element in the HTML, two buttons were being displayed.
**Fix:** The duplicate button was removed, and the buttons that toggle content based on the current state ("Check Answer," "Next Question," "View Results") were consolidated into a single button.
**Result:** Fixed. ### Bug 2 – Results page not displaying
**Issue:** After answering all 5 questions, the quiz section would disappear, but the results page failed to appear.
**Cause:** A missing closing `</section>` tag caused the results section to be incorrectly nested within the quiz section.
**Fix:** Added the missing closing tag, correctly separating the quiz section from the results section.
**Result:** Fixed. The final score is now correctly displayed on the results page.
### Bug 3 – Incorrect results message
**Issue:** The results page consistently displayed the same positive message, regardless of the actual score.
**Fix:** Implemented JavaScript conditional statements (`if`, `else if`, and `else`) to display different messages based on the final score.

**Result:** Fixed. ## 6. Technologies Used for Testing
- Google Chrome
- Chrome DevTools
- HTML5
- CSS3
- Bootstrap 5.3.8
- JavaScript

## 7. Conclusion
Testing confirms that the core functions of "Eco Quiz"—such as question selection, answer validation, score calculation, feedback display, and the final results page—are working correctly.
We also conducted testing in a simulated mobile environment. Further testing will be performed once "Eco Quiz" is integrated into the main "EcoWise" group website.
