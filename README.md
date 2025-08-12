# iCapital Identity Integration - Solutions Engineer Challenge

This repository contains my submission for the iCapital Identity Solutions Engineer challenge.

## 📁 Deliverables

### Part One - Email Responses
- **File**: `part_one_responses.md`
- **Content**: Professional responses to two customer technical support inquiries about Parallel Markets SDK integration issues

### Part Two - Integration Demo
- **File**: `index.html`
- **Purpose**: Demonstrates Parallel Markets JavaScript SDK integration for identity collection

## 🚀 Quick Start - Local Deployment

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, or Edge)
- Python 3 or Node.js (for local server)
- Client ID from Parallel Markets dashboard (or use the pre-configured one)

### Step 1: Clone the Repository
```bash
git clone https://github.com/isaacbuz/iCapital.git
cd iCapital
```

### Step 2: Start a Local Web Server

Choose one of these options:

**Option A - Python (Recommended)**
```bash
python3 -m http.server 8000
```

**Option B - Node.js**
```bash
npx http-server -p 8000
```

**Option C - PHP**
```bash
php -S localhost:8000
```

### Step 3: Open in Browser
Navigate to: http://localhost:8000

## 📋 How to Test the Integration

1. **Initialize the SDK**
   - The page loads with a pre-configured Client ID
   - Click the "Initialize SDK" button
   - You should see a success message

2. **Start Identity Verification**
   - After initialization, a Parallel button appears
   - Click the Parallel button to open the identity collection overlay
   - Fill out the test form with any test data

3. **View Results**
   - Open your browser's Developer Console (F12 or Cmd+Option+I)
   - Submit the form in the overlay
   - The console will display:
     - Authentication response parameters
     - User profile information
     - Parallel ID for the session

## 🔧 Technical Implementation

### Features Implemented
- ✅ Parallel Markets JavaScript SDK v2 integration
- ✅ Renders the Parallel button for identity collection
- ✅ Opens overlay flow when button is clicked
- ✅ Logs complete identity results to developer console
- ✅ Configured for sandbox environment (demo.parallelmarkets.com)
- ✅ Error handling and status messages
- ✅ Clean, professional UI

### Configuration Details
- **Environment**: Sandbox (`demo`)
- **Client ID**: Pre-configured for testing
- **Redirect URI**: `http://localhost:8000/`
- **SDK Version**: v2
- **Scopes**: `['profile', 'accreditation_status']`

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

## ⏱️ Time Spent

Approximately 2 hours:
- 30 minutes: Research and documentation review
- 30 minutes: Part One email responses  
- 45 minutes: Part Two implementation
- 15 minutes: Documentation and testing

## 📧 Submission Details

**To**: dev-admin@parallelmarkets.com  
**From**: Isaac Buziba (isaacbuz@gmail.com)  
**Repository**: https://github.com/isaacbuz/iCapital

### Submission Contents:
1. Part One responses: See `part_one_responses.md`
2. Part Two integration: See `index.html` 
3. Git commit history: Available in repository
4. Local deployment instructions: This README

## Important Notes

- The integration is configured to work with `http://localhost:8000/` as the redirect URI
- The Client ID is pre-configured in the HTML for easy testing
- All code follows the patterns shown in the official Parallel Markets SDK examples
- The solution focuses on the core requirements without unnecessary complexity

Thank you for considering my application for the Solutions Engineer role at iCapital!