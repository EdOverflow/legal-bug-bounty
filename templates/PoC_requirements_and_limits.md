# Bug bounty proof of concept requirements and limits

Minimization of legal risks in bug bounties also means conveying as clear as possible not only what are the rules and limitations on handling users’ data and safeguarding the systems integrity, but also what are the program expectations of a valuable proof of concept (PoC) that demonstrates the impact of vulnerability and allows reproducibility -- but doesn’t cross the line in terms of exploitation and access to users’ data. In the past confusion as to where the bug bounty policy draws that line has created potential legal implications. 

On this issue the DOJ Framework explicitly provides guidelines: “describe authorized and unauthorized conduct in plain, easily understood terms”, “clearly explain any limitations on accessing, copying, using, or retaining the organization’s data in relation to vulnerability disclosure activities” and “avoid using vague jargon or ambiguous technical language to describe critical aspects of the policy, such as acceptable and unacceptable conduct.” 

To this end, #legalbugbounty suggests you use examples to explain what is the ideal PoC you are looking for in each bug, that doesn’t cross any red lines. Examples help to communicate to the community what are the best practices. You can continue to update these examples based on your interaction with the crowd. Here is one suggested template do just that, that you can adjust to your needs. Other programs that provide examples include Yahoo (https://hackerone.com/yahoo). 

If you are looking for useful language on minimization of harm for users’ data, check out [Uber's bug bounty policy](https://hackerone.com/uber).

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

## ⚖ Legal disclaimer

**⚠ You must consult with a lawyer before implementing any language!**

_This report does not constitute legal advice and the author is not admitted to practice law in the U.S. The information contained herein is for general guidance on matters of interest only. The application and impact of laws can vary widely based on the specific facts involved. Given the changing nature of laws, terms, rules and regulations, there may be delays, omissions or inaccuracies in information contained herein. Accordingly, the information is provided with the understanding that the author is not herein engaged in rendering legal or other professional advice and services. As such, it should not be used as a substitute for consultation with professional legal or other competent advisers. Before making any decision or taking any action, you should consult a professional. All information is provided “as is”, with no guarantee of completeness, accuracy, timeliness or of the results obtained from the use of this information, and without warranty of any kind, express or implied, including, but not limited to warranties of performance, merchantability and fitness for a particular purpose. In no event will the author be liable to you or anyone else for any decision made or action taken in reliance on the information herein or for any consequential, special or similar damages._
