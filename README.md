# att-xss
An XSS Vulnerability for AT&amp;T

Status: Reported to https://bugbounty.att.com/ 
and remediated.

Type of Issue: XSS on AT&T “M2X product pages”.

POC/Link Vulnerable: https://m2x.att.com/jumpstart?type=startup"><script> for(var i=0;i>=0;i++){alert(Math.random()); alert(document.cookie);} </script> 

Sub-domain: m2x.att.com 

Login Required: Reproducible with and without Login. 

Tested on: Mozilla Firefox 38. xx. It is reproducible on all other major browsers as well. 

Impact: · If Login exists, stealing the cookie can be used to get the session active again. · Manipulating the client page to perform some malicious action. · Recording KeyStrokes is possible as the JS is injectable. · Phishing, UrlRedirection. · Brute forcing the password through the compromised browser.
