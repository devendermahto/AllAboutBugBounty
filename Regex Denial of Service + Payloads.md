# This is a bug in regex that causes DOS attack, the way server handle regex is tricky and sometimes it give up 100% cpu power to find the match with defined match pattern.

## Resources: 
`https://github.com/harsh-bothra/learn365/blob/main/days/day2.md`
'https://javascript.info/regexp-catastrophic-backtracking'

### How To Identify (as you need to guess how they are handling input in server side and if they use regex then try tasting with different set of payloads or if source code of server side is available then analyse and test it.
### i Commanly review the client side code and try to find if the developers are using regex patterns for anything by this i conclude that it might be possible to find something similar behaviour of developers with server side code.
regexp.test() is used by javascript so don't forget to look for it.<br>and after sending payloads and confirm if it affected the server use time syntax
<br>`time curl --headers <headers> <URL>`

## Payloads

### 1. Pattern for checking email id
`^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$`
### 1. Payload to cause Catastrophic backtracking
`EvilRegexBySilent_@nuke.com26`

