# Part One - Email Responses

## Response to First Email - Tony Wonder

Subject: Re: Sandbox Environment Setup Issue - Client ID Configuration

Hi Tony,

Thank you for reaching out! I can see the issue with your integration setup.

The problem is that you're using the production SDK URL (`https://app.parallelmarkets.com/sdk/v1/parallel.js`) while trying to connect to the sandbox environment. For the sandbox environment, you need to make two adjustments:

1. Update your SDK URL to use version 2: `https://app.parallelmarkets.com/sdk/v2/parallel.js`
2. Add the `environment: 'demo'` parameter to your `Parallel.init()` call

Here's the corrected code:

```html
<div class="parallel-login-button"></div>
<script src="https://app.parallelmarkets.com/sdk/v2/parallel.js"></script>
<script>
  Parallel.init({ 
    client_id: '2ja98wfawefbascdiu', 
    environment: 'demo',  // This tells the SDK to use the sandbox environment
    flow_type: 'overlay' 
  })
  Parallel.subscribeWithButton(() => console.log('done'), (e) => console.error(e))
</script>
```

The `environment: 'demo'` parameter is crucial as it directs the SDK to communicate with demo.parallelmarkets.com instead of the production environment. Without this parameter, the SDK attempts to validate your client_id against production, where it doesn't exist.

Please give this a try and let me know if you encounter any other issues. We're here to help!

Best regards,  
Isaac Buziba  
Solutions Engineer  
iCapital Identity Team

---

## Response to Second Email - Maggie Lizer

Subject: Re: Prefilling User Information in Parallel Flow

Hi Maggie,

Thanks for reaching out! I can help you with prefilling the user information.

The issue you're experiencing is due to a small but important detail in the parameter naming. The email field should be lowercase `email` rather than `Email` (with a capital E).

Here's the corrected function call:

```javascript
Parallel.login({ 
  first_name: first, 
  last_name: last, 
  email: user_email  // Changed from 'Email' to 'email'
})
```

JavaScript is case-sensitive, and the Parallel SDK expects the email parameter to be all lowercase. This is why the email field appears empty in the overlay despite your other fields potentially working correctly.

As a best practice, all parameter names in the Parallel SDK use lowercase with underscores for multi-word parameters (snake_case), such as `first_name`, `last_name`, and `email`.

Please update your code with the lowercase `email` parameter, and the prefill should work as expected. If you have any other questions or need further assistance, please don't hesitate to reach out!

Best regards,  
Isaac Buziba  
Solutions Engineer  
iCapital Identity Team