# Example proof of concept rules table

Taken from https://hackerone.com/liberapay (Written by @EdOverflow). This list can help reduce noise and ensure that hackers know what the technical boundaries are.

| Issue type | When to report the issue |
|------------|--------------------------|
|  XSS      |     For XSS, a simple `alert(document.domain)` should suffice. |
|  RCE     |  Please only execute harmless code. Simply printing something or evaluating an expression should be enough to demonstrate the issue.  |
|   SQLi         |   Report it as soon as you have a SQL error that indicates SQL injection or you are able to disclose the SQL server's version number.       |
| Unvalidated redirect | Set the redirect endpoint to http://example.com if possible. |
| CSRF | Either attach a file to demonstrate the issue or paste the code in a code block in your report. |
| SSRF | Do not go playing around on any internal networks. Report as soon as you believe that you have a potential SSRF issue and we will look into it for you. |
| LFI | The same applies here — please do not go against the guideline listed in the *Disclosure policy* section. We investigate LFI reports in a dev environment to make sure it is valid. |
