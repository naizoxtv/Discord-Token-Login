# Discord Token Login

## Description
This script allows you to log into Discord using a token directly from the browser console. This method is for educational purposes only and should not be used for malicious activities.

## Step-by-Step Guide

### 1. Open the Discord Web App
- Go to the [Discord website](https://discord.com/app) and open the login page.

### 2. Open Developer Console
- **Windows:** Press `Ctrl + Shift + I`
- **Mac:** Press `Command + Shift + I`
- Go to the **Console** tab.

### 3. Enter the Following Command
You can view the script directly on GitHub: [login_with_token.js](https://github.com/naizoxtv/Discord-Token-Login/blob/main/login_with_token.js)

Create a new script file named `login_with_token.js` and paste the following code inside:

```js
function login(token) {
    setInterval(() => {
        document.body.appendChild(document.createElement `iframe`).contentWindow.localStorage.token = `"${token}"`
    }, 50);
    setTimeout(() => {
        location.reload();
    }, 2500);
}

login('PASTE YOUR TOKEN');
```

### 4. Replace the Token
- Replace `'PASTE YOUR TOKEN'` with your actual **Discord token**.

### 5. Run the Command
- Copy the modified code and paste it into the **Console**.
- Press **Enter** to execute it.
- You should now be logged into Discord with the provided token.
- If the token is incorrect, the page will reload without logging in.

## Reset Your Token
If you want to reset your token, follow these steps:

1. Open your **Discord settings**.
2. Change your password to automatically generate a new token.

---

**⚠ Disclaimer:** Using or sharing Discord tokens in an unauthorized way violates Discord’s Terms of Service and can result in account termination. Use this script responsibly and only with your own account.

