# Security Policy

## Supported Versions

We release patches for security vulnerabilities. Currently supported versions:

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

We take the security of Omnifood Landing Page seriously. If you believe you have found a security vulnerability, please report it to us as described below.

### Where to Report

**Please do NOT report security vulnerabilities through public GitHub issues.**

Instead, please report them via:
- Email: [Your contact email - if you want to provide one]
- GitHub Security Advisory: [Create a private security advisory](https://github.com/barisariburnu/omnifood-landing-page/security/advisories/new)

### What to Include

Please include the following information in your report:

1. **Type of vulnerability** (e.g., XSS, CSRF, injection, etc.)
2. **Full path** of the affected source file(s)
3. **Location** of the affected code (tag/branch/commit or direct URL)
4. **Step-by-step instructions** to reproduce the issue
5. **Proof-of-concept or exploit code** (if possible)
6. **Impact** of the vulnerability
7. **Suggested fix** (if you have one)

### Response Timeline

- **Initial Response**: We will acknowledge receipt of your vulnerability report within 48 hours
- **Status Update**: We will send you regular updates about our progress every 5-7 days
- **Resolution**: We aim to resolve critical vulnerabilities within 30 days

### What to Expect

After submitting a vulnerability report, you can expect:

1. **Confirmation**: We'll confirm receipt of your vulnerability report
2. **Investigation**: We'll investigate and validate the reported vulnerability
3. **Fix Development**: If confirmed, we'll develop a fix
4. **Disclosure**: We'll coordinate the disclosure with you
5. **Credit**: We'll acknowledge your contribution (if you wish)

## Security Best Practices for Users

While using this project, please follow these security best practices:

### For Developers

1. **Keep dependencies updated**: Regularly update jQuery and other libraries
2. **Validate user input**: If you add forms with backend integration, always validate and sanitize input
3. **Use HTTPS**: Always serve the website over HTTPS in production
4. **Content Security Policy**: Implement CSP headers to prevent XSS attacks
5. **Sanitize output**: If displaying user-generated content, sanitize it properly

### For Deployment

1. **Server Security**: Keep your web server and OS updated
2. **File Permissions**: Set appropriate file permissions (644 for files, 755 for directories)
3. **HTTPS Only**: Use HTTPS and enable HSTS
4. **Security Headers**: Implement security headers:
   - `X-Content-Type-Options: nosniff`
   - `X-Frame-Options: DENY`
   - `X-XSS-Protection: 1; mode=block`
   - `Referrer-Policy: strict-origin-when-cross-origin`

### Configuration Examples

**Apache (.htaccess):**
```apache
# Security Headers
Header set X-Content-Type-Options "nosniff"
Header set X-Frame-Options "DENY"
Header set X-XSS-Protection "1; mode=block"
Header set Referrer-Policy "strict-origin-when-cross-origin"

# Redirect HTTP to HTTPS
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST%{REQUEST_URI} [L,R=301]
```

**Nginx:**
```nginx
# Security Headers
add_header X-Content-Type-Options "nosniff" always;
add_header X-Frame-Options "DENY" always;
add_header X-XSS-Protection "1; mode=block" always;
add_header Referrer-Policy "strict-origin-when-cross-origin" always;

# Redirect HTTP to HTTPS
server {
    listen 80;
    server_name example.com;
    return 301 https://$server_name$request_uri;
}
```

## Known Security Considerations

### Third-Party Dependencies

This project uses the following third-party libraries:

- **jQuery 1.11.2**: This is an older version. While sufficient for this project's needs, consider upgrading to jQuery 3.x for better security
- **CDN Resources**: We load some resources from CDNs. Consider using Subresource Integrity (SRI) hashes

#### Adding SRI Hashes

For enhanced security, add SRI hashes to external resources:

```html
<script 
  src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"
  integrity="sha384-[HASH]"
  crossorigin="anonymous">
</script>
```

### Form Validation

If you implement backend form processing:

1. **Server-side validation**: Never trust client-side validation alone
2. **CSRF protection**: Implement CSRF tokens for form submissions
3. **Rate limiting**: Implement rate limiting to prevent abuse
4. **Email validation**: Use proper email validation libraries

## Disclosure Policy

- We follow coordinated vulnerability disclosure
- We'll work with you to understand and validate the issue
- We'll develop and test a fix
- We'll release a security update
- We'll publicly disclose the vulnerability (crediting you if desired)

## Security Update Process

When we release security updates:

1. The fix will be committed to a private branch
2. A new version will be tagged and released
3. The CHANGELOG will be updated with security fix details
4. A security advisory will be published
5. The community will be notified

## Comments on This Policy

If you have suggestions on how this process could be improved, please submit a pull request or open an issue.

## Recognition

We appreciate security researchers who help keep Omnifood Landing Page and its users safe. Hall of Fame will be maintained here for security researchers who have responsibly disclosed vulnerabilities:

<!-- Hall of Fame -->
*No security vulnerabilities have been reported yet.*

---

**Thank you for helping keep Omnifood Landing Page and its users safe!**
