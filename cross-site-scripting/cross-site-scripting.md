# Cross-Site Scripting (XSS)

## What is XSS?
Cross-Site Scripting (XSS) is a type of security vulnerability that allows attackers to inject malicious scripts into web pages viewed by other users. These scripts can be used to steal data, manipulate web page content, or perform other malicious actions. XSS typically occurs when an application includes user-generated content in web pages without properly validating or escaping it.

There are three main types of XSS:
1. **Stored XSS**: The malicious script is permanently stored on the target server (e.g., in a database).
2. **Reflected XSS**: The malicious script is reflected off a web server, often as part of a URL.
3. **DOM-based XSS**: The vulnerability exists in the client-side code, allowing manipulation of the DOM.

---

## 1. Stored XSS

Stored XSS occurs when a malicious script is injected into a website's database and is served to users when they visit certain pages. This type of XSS is more dangerous since the payload is stored on the server and impacts all users visiting the page.

### Example
Imagine a comment section where a user submits a comment. If the application doesn't sanitize the input, an attacker can submit the following:

```html
<script>alert('XSS Attack!');</script>
```
