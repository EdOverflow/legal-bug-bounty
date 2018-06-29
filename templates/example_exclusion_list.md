## Example vulnerability exclusion list for you program

Taken from https://hackerone.com/liberapay (Written by @EdOverflow). This list can help reduce noise and ensure that hackers know what the technical boundaries are.

| Description | Reason |
|-------------|--------|
| Network-level Denial of Service (DoS/DDoS) vulnerabilities. | We do not want you to disrupt any of our services. |
| Low severity issues that can be detected with tools such as [Hardenize](https://www.hardenize.com/) and [Security Headers](https://securityheaders.io/). | We run regular scans with these services and try to improve our score gradually. |
| Content injection issues. | The severity of this issue is so low that it does not warrant a report. |
| Cross-site Request Forgery (CSRF) with minimal security implications (Logout CSRF, etc.). | In order for CSRF to be a valid issue it must affect some important action such as deleting one's account. |
| Missing cookie flags on non-security-sensitive cookies. | These type of issues do not present a major risk and are usually picked up by scanners. |
| UI and UX bugs (including spelling mistakes). | No comment. |
| 401 injection. | This is usually an accepted risk and we are already aware of this issue: https://github.com/liberapay/liberapay.com/issues/504. |
| Stack traces that disclose information. | All of our projects are open-source therefore this information is usually public knowledge. **That said, if you discover a stack trace that discloses information which is not located in our GitHub repositories, please do submit a report.** |
| Host header issues without an accompanying proof-of-concept demonstrating vulnerability. | We require a clear proof of concept. |
| Open ports without an accompanying proof-of-concept demonstrating vulnerability. | Same as above. |
| Banner grabbing issues (figuring out what web server I use, etc.). | We will happily share what web servers we are running. |
| Missing `X-Frame-Options` header (Clickjacking) | The lack of `X-Frame-Options` does not always indicate that a security vulnerability is present. This is an optional header that is only necessary on endpoints where there UI is rendered to invoke state changing actions. I recommend reading this informative post by David Ross: https://plus.google.com/u/0/+DavidRossX/posts/jVrtTRd5yKP |
| Cross-site tracing | In order for Cross-Site Tracing (XST) to really be a significant issue you would need to find an endpoint vulnerable to Cross-site Scripting (XSS). |
| CSP uses `unsafe-inline` | The fact that a CSP includes `unsafe-inline` is not an issue in itself. In order for you to demonstrate the actual impact of this value, we highly recommend you look for an XSS vulnerability. Try to trigger `alert(document.domain)`. |
| Disclosure of robots.txt file | We are aware that in some cases robots.txt files have been known to disclose sensitive information. In our case we have determined that our robots.txt files do not contain any information that poses a potential security risk. |
| Email spoofing (SPF misconfigurations) | We have accepted the risk that this issue poses and do not believe that it warrants an immediate fix. |
| Open redirect using `Host` header | Open redirects in the `Host` header are not exploitable. |
