### GUI Test Cases

| Case                      | Expected Outcome                                                                 | Actual Outcome            | QA Status | Comments                                                                 |
|--------------------------|----------------------------------------------------------------------------------|---------------------------|-----------|--------------------------------------------------------------------------|
| Login button visibility  | "Login" button should be visible on the top-right of the application             | Visible                   | Pass      |                                                                          |
| Login button text        | Button text should be exactly "Login"                                            | Shows "Login"             | Pass      |                                                                          |
| Login button alignment   | Button should be properly aligned and not overlap with other elements            | Properly aligned          | Pass      |                                                                          |
| Login modal/page layout  | Login screen should be clean, with phone number and OTP input fields clearly visible | Phone and OTP fields shown | Pass      |                                                                          |
| Login screen responsiveness | Login screen should adjust correctly on mobile screens                      | Mobile responsive         | Pass      | On mobile view, the "Login" option is accessible via hamburger menu under "Create Account." |

### Functional Test Cases

| Case                         | Expected Outcome                                                                 | Actual Outcome             | QA Status | Comments |
|-----------------------------|----------------------------------------------------------------------------------|----------------------------|-----------|----------|
| Clicking Login redirects correctly | Clicking Login should open the phone number input screen                 | Opens login input screen   | Pass      |          |
| Valid login flow works      | Enter valid phone number and 6-digit OTP, then click "Verify"                   | Logged in successfully     | Pass      |          |
| OTP input appears after phone | After entering phone, OTP field should appear or page should change           | OTP field shown            | Pass      |          |
| Resend OTP works            | After OTP is sent, "Resend OTP" option should appear (after timeout)            | Appears after timeout      | Pass      |          |
| OTP expiry is handled       | Expired OTP should not be accepted                                               | Shows error                | Fail      |          |
| Error shown for wrong OTP   | Entering wrong OTP should show error message                                    | Shows "Invalid OTP"        | Fail      |          |
| Already logged-in state     | If already logged in, user should not be redirected back to login               | Skips login and redirects  | Pass      |          |
| Login state persists        | After login, navigating back should not require login again                     | Logged-in state retained   | Pass      |          |

### Field Validation Test Cases

| Case                         | Expected Outcome                                                              | Actual Outcome           | QA Status | Comments |
|-----------------------------|-------------------------------------------------------------------------------|--------------------------|-----------|----------|
| Phone number required        | Submitting empty phone number should show validation error                   | Shows “Enter phone number” | Pass      |          |
| Phone number must be 10 digits | Entering less/more than 10 digits should show validation error             | Shows “Invalid phone number” | Pass      |          |
| Phone number must be numeric | Entering alphabets/special chars should show validation error               | Only digits allowed       | Pass      | It's good - we have restriction on alphabets on first place itself. |
| OTP required                 | Submitting without OTP should show validation error                          | “Enter OTP” shown         | Pass      | We are allowed to enter OTP only after clicking "Get OTP" |
| OTP must be 6 digits         | OTP field must only accept exactly 6 digits                                  | Only 6 digits accepted    | Pass      |          |
| OTP input must be numeric    | Alphabetical input in OTP field should be restricted                         | Only digits allowed       | Pass      |          |

The following test cases have been documented in excel sheet [here](https://docs.google.com/spreadsheets/d/11nhrYHY-EBhT6sWdex27_Df46-2VOIaUdtUAHqwWpIM/edit?gid=0#gid=0)
