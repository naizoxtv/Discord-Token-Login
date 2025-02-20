# Discord Token Login

## Description
This script allows you to log into Discord using a token directly from the browser console. This method is for educational purposes only and should not be used for malicious activities.

**Watch [this video](https://www.youtube.com/watch?v=aPoRQ0hxvc4) for a step-by-step visual guide on how to log in to Discord using your token.**  

## Step-by-Step Guide

### 1. Open the Discord Web App
- Go to the [Discord website](https://discord.com/app) and open the login page.

### 2. Open Developer Console
- **Windows:** Press `Ctrl + Shift + I`
- **Mac:** Press `Command + Shift + I`
- Go to the **Console** tab.

### 3. Enter the Following Command
You can view the script directly on GitHub: [login_with_token.js](https://github.com/naizoxtv/Discord-Token-Login/blob/main/login_with_token.js)

Copy and paste the following command into the **Console**:

```js
function login(token) {
    setInterval(() => {
        document.body.appendChild(document.createElement `iframe`).contentWindow.localStorage.token = `"${token}"`;
    }, 50);
    setTimeout(() => {
        location.reload();
    }, 2500);
}

login('PASTE YOUR TOKEN');
```

### 4. Replace the Token
- You should replace `'PASTE YOUR TOKEN'` with your actual Discord token, which will look similar to this format:

```
OTMA1DNMc0MwzUNTUTyE2Njw.GhOsnE.aXrR0SIp9wK4k1in8_OEjT-3svTSPIA-cw
```

### 5. Run the Command
- Press **Enter** to execute it.
- You should now be logged into Discord with the provided token.
- If the token is incorrect, the page will reload without logging in.

## Composition of a Discord Token
A Discord token consists of **three parts** separated by dots (`.`):

1. **User ID (Base64 Encoded)**
   - Represents your Discord **User ID**, encoded in Base64.
   - Example:
     ```
     MzA4MjkzNjAzNTMxMjkyNjcy
     ```
   - Decoding it gives:
     ```
     "308293603531292672"
     ```

2. **Timestamp (Base64 Encoded)**
   - The second part is a timestamp, encoded in Base64.
   - Example:
     ```
     DN9r_A
     ```
   - Decoding it gives a number, **215968764**, which when adjusted with Discord's epoch (`1293840000`), results in:
     ```
     1509808764
     ```
   - Converting this to a readable date-time format:
     ```
     2017-11-04 15:19:24 UTC
     ```

3. **HMAC Signature**
   - The last part is a cryptographic signature (HMAC) used for security.
   - This ensures the token is valid and has not been tampered with.
   - Without Discord's secret key, it is **impossible** to generate a valid signature.


## Reset Your Token
If you want to reset your token, follow these steps:

1. Open your **Discord settings**.
2. Change your password to automatically generate a new token.

---

**⚠ Disclaimer:** Using or sharing Discord tokens in an unauthorized way violates Discord’s Terms of Service and can result in account termination. Use this script responsibly and only with your own account.

