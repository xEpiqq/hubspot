<script>
    let email = '';
    let successMessage = '';
  
    const subscribe = async () => {
      if (email) {
        // Placeholder for the subscription logic (e.g., an API call)
        successMessage = `You're now subscribed to CRM Tips! Keep an eye out for our weekly newsletter sent straight to ${email}.`;
        email = '';
      }
    };
  </script>
  
  <section class="container">
    <!-- Header Section -->
    <div class="header">
      <h1>CRM Tips</h1>
      <p>
        Get the best CRM insights straight to your inbox every week. Boost your customer relationships, streamline workflows, and stay ahead with our actionable tips, tools, and strategies.
      </p>
    </div>
  
    <!-- Subscription Form -->
    <div class="form-container">
      <h2>Sign up for CRM Tips</h2>
      <p>Join thousands of subscribers who receive exclusive CRM insights!</p>
  
      <form on:submit|preventDefault={subscribe}>
        <input 
          type="email"
          bind:value={email}
          placeholder="Enter your email"
          class="email-input"
          required
        />
        <button class="submit-btn">
          Subscribe
        </button>
      </form>
  
      <!-- Success Message -->
      {#if successMessage}
        <p class="success-message">{successMessage}</p>
      {/if}
    </div>
    
    <!-- Footer -->
    <footer class="footer">
      <p>Stay tuned for weekly updates from CRM experts.</p>
    </footer>
  </section>
  
  <style>
    body {
      font-family: 'Inter', sans-serif;
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    .container {
      background: linear-gradient(135deg, #2c7a7b, #2d3748);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      color: white;
      padding: 20px;
    }
    .header {
      text-align: center;
      max-width: 600px;
      margin-bottom: 20px;
    }
    .header h1 {
      font-size: 3rem;
      font-weight: bold;
      margin-bottom: 15px;
    }
    .header p {
      font-size: 1.2rem;
      line-height: 1.6;
    }
    .form-container {
      background-color: white;
      color: black;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      text-align: center;
      width: 100%;
      max-width: 400px;
    }
    .form-container h2 {
      font-size: 1.8rem;
      margin-bottom: 10px;
    }
    .form-container p {
      margin-bottom: 20px;
      font-size: 1rem;
    }
    .email-input {
      width: 100%;
      padding: 12px;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 1rem;
      margin-bottom: 15px;
    }
    .submit-btn {
      width: 100%;
      background-color: #2c7a7b;
      color: white;
      padding: 12px;
      font-size: 1rem;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .submit-btn:hover {
      background-color: #285e61;
    }
    .success-message {
      margin-top: 15px;
      color: #38a169;
      font-weight: bold;
    }
    .footer {
      margin-top: 20px;
      text-align: center;
      font-size: 0.9rem;
    }
  </style>
  