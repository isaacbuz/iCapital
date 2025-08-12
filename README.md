# iCapital Identity Integration - Solutions Engineer Challenge

This repository contains my submission for the iCapital Identity Solutions Engineer challenge.

## Contents

1. **part_one_responses.md** - Email responses to customer inquiries (Part One)
2. **index.html** - Parallel Markets SDK integration demo (Part Two)
3. **README.md** - This file with setup and usage instructions

## Part Two - Integration Demo

### Features Implemented

- ✅ HTML web page with Parallel SDK integration
- ✅ Renders the Parallel button to initiate identity collection
- ✅ Opens Parallel overlay when button is clicked
- ✅ Prints identity results to developer console
- ✅ Supports credential configuration (client_id and API key)
- ✅ Includes manual login option with prefilled user data
- ✅ Proper error handling and status messages
- ✅ Clean, professional UI with clear instructions

### Running the Integration Locally

1. **Simple HTTP Server (Python)**
   ```bash
   # Python 3
   python3 -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   ```
   Then open: http://localhost:8000

2. **Node.js HTTP Server**
   ```bash
   # Install http-server globally (one time)
   npm install -g http-server
   
   # Run server
   http-server -p 8000
   ```
   Then open: http://localhost:8000

3. **Direct File Access**
   - Simply open `index.html` directly in your browser
   - Note: Some browsers may have CORS restrictions for local files

### Using the Integration

1. **Enter Credentials**
   - Input the client_id provided for the sandbox environment
   - Enter the API key if you have one (optional for basic flow)

2. **Initialize SDK**
   - Click "Initialize SDK" button
   - You should see a success message

3. **Start Identity Flow**
   - Click the Parallel button that appears
   - Complete the identity form in the overlay
   - Submit the information

4. **View Results**
   - Open browser Developer Console (F12)
   - Identity results will be logged after successful submission
   - The console will show the Parallel ID and any available profile data

### Technical Implementation Notes

- Uses Parallel SDK v2 with sandbox environment configuration
- Implements proper error handling for SDK initialization and API calls
- Includes both automatic button subscription and manual login methods
- Attempts to fetch full identity details via API (may be limited by CORS in browser)
- Provides clear console logging for debugging and result viewing

### What I Would Add With More Time

1. **Backend Integration**
   - Create a Node.js/Express backend to handle API calls securely
   - Implement proper credential management without exposing keys
   - Add endpoints for fetching and storing identity data

2. **Enhanced UI/UX**
   - Add loading spinners during API calls
   - Display identity results in the UI (not just console)
   - Implement a results table showing verification status
   - Add form validation for credential inputs

3. **Additional Features**
   - Webhook integration for async updates
   - Session management and user persistence
   - Multiple flow types (KYC, KYB, accreditation)
   - Export functionality for identity data

4. **Testing & Documentation**
   - Unit tests for SDK integration
   - End-to-end testing with Cypress or Playwright
   - API documentation with examples
   - Video walkthrough of the integration

## Time Spent

Approximately 2 hours total:
- 30 minutes: Research and documentation review
- 30 minutes: Part One email responses
- 45 minutes: Part Two implementation
- 15 minutes: Documentation and final review

## Contact

For any questions about this submission, please contact me at [your email].

Thank you for considering my application!