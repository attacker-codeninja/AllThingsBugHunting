## All-Things-IDOR

------





[My Bug Hunting Journey with IDORs Part 1 ]: https://dewcode.medium.com/my-bug-bounty-journey-with-idors-part-1-d97cf187729

* Found base64 things in GET URL 
* Found that it was ID of his Application
* Changed Application ID of his own to another User and got IDOR





[ My Bug Hunting Journey with IDORs Part 2 ]: https://dewcode.medium.com/my-bug-hunting-journey-with-idors-part-2-422a737fb733

* Introduction to IDOR ->

  * ```
    Insecure Direct Object References (IDOR) occurs when a developer forgets to validate the objects-based user inputs, it allows a malicious user to access other user's data directly from the database server. This type of vulnerability considers as an Access Control failure. Insecure Direct Object Reference is one of the most common vulnerabilities. It is listed on OWASP TOP 10 2013 and 2017 (Merged with Broken Access Control) list.
    ```

* Types of IDOR ->

  * ```
    Common IDOR
    Base64 based IDOR
    GUID/UUID based IDOR
    
    
    Common IDOR =>
    
    This type of IDOR can easily detect to looking in the URL or body of the POST request. for finding IDORs you have to check all the parameters passing through the Post request or URL. Just modify the value of the parameter and monitor the responses of the application.
    
    
    Base64 based IDOR =>
    
    This type of IDOR is similar to Common IDOR but the parameter is passed in base64 format. For testing this type of issue you need to decode base64 first and after modification, encode into base64, and put into URL parameter. you can perform this action using Burp Suite. First, select the value and press Ctrl+Shiift+B to decode and Ctrl+B to encode.
    
    
    GUID/UUID based IDOR =>
    
    This type of IDOR is difficult to exploit because of nature. The server generates GUID/UUID for each user that can not be predictable. to exploiting this type IDORs you have to create another account and swap the GUID/UUID. Many bug bounty program does not consider that type of bug as a security issue. Before reporting this type IDOR you have to find another endpoint where you can able retrieve other users UUID then definitely, it should be considered as P1.
    
    
    ```

* **Endpoint for IDOR :**

  * > *Always look at in *
    >
    > *id, uid, name, role, email, appid, invoice_id, and any CRUD(Create, Read, Update, Delete) operations. You must have to monitor all requests and parameters to detect IDOR while testing.*

* REFERENCES:

  * > https://www.bugcrowd.com/blog/how-to-find-idor-insecure-direct-object-reference-vulnerabilities-for-large-bounty-rewards/

  * > https://blog.detectify.com/2016/05/25/owasp-top-10-insecure-direct-object-reference-4/

  * > https://blog.intigriti.com/hackademy/idor/









> ### IDOR Bypasses => 	

 - Change Method GET/POST 

 - Parameter Pollution 

 - Wrapping in Array => https://twitter.com/traceableai/status/1221704446880518144

    - Wrap ID with an array {“id”:111} --> {“id”:[111]}
    - JSON wrap {“id”:111} --> {“id”:{“id”:111}}
    - Send ID twice URL?id=<LEGIT>&id=<VICTIM>
    - Send wildcard {"user_id":"*"}

 - Go for the “hidden” features. CSV import, user avatars or hidden photos, the aftersales processes,...

 - Path Traversal

    -  http://target/change/MY_ID/../VICTIM_ID

- Same name tip

  - > Lets say victims group name is hello123
    > you will create a group named hello123 
    > Now you can try to delete it





> ### Some BugBountyTips  & POCs & Writeups

### 1. Tip

```
1. Intercept every request on each button. 
2. Find request that is vulnerable to IDOR. 
3. Change attacker name to victim name. 
4. IDOR, lead to know victim data. 
```

### 2. Tip

```
Bypassed #IDOR protection using URL Shorteners

https://blog.detectify.com/2019/07/03/lerhan-bypassing-idor-protection-with-url-shorteners/
```



### 3. Writeups

```
https://twitter.com/Mah3Sec_/status/1332353437439127554

https://medium.com/@aysebilgegunduz/everything-you-need-to-know-about-idor-insecure-direct-object-references-375f83e03a87

https://corneacristian.medium.com/top-25-idor-bug-bounty-reports-ba8cd59ad331?source=social.tw

https://medium.com/bugbountywriteup/all-about-getting-first-bounty-with-idor-849db2828c8

https://medium.com/bugbountywriteup/a-short-story-of-idor-to-account-takeover-b36f3983ecba

https://medium.com/@swapmaurya20/a-simple-idor-to-account-takeover-88b8a1d2ec24

https://sushantdhopat.medium.com/all-about-my-finding-last-week-idor-insecure-direct-object-reference-2ff221c9a329

https://xploitprotocol.medium.com/hunt-for-the-idor-automation-using-burp-suit-a09f004a9d9d

https://medium.com/@abhiunix/idor-on-api-endpoints-e08c740e87a2

https://medium.com/@cobrabaghdad1/idor-lead-to-personally-identifiable-information-pii-leakage-fb2b1b4be93f

https://jeyaseelans.medium.com/

https://medium.com/bugbountywriteup/pii-leakage-via-idor-weak-passwordreset-full-account-takeover-58d159f88d73

https://mustafakemalcan.com/insecure-direct-object-reference-idor-tips/
```





### 4. Tip

```
Simple Bash-Command for Finding "Insecure Direct Object Referencing"

cat urls.txt | grep "id=[\id]*" | tee idor.txt
```







### # 5. Tip

```
A simple IDOR after account takeover.
```



![Image](https://pbs.twimg.com/media/Eb3BcM0UwAAI0gu?format=jpg&name=large)





```
Mass account takeover 
```

![Image](https://pbs.twimg.com/media/EaidWiHUwAAk48e?format=jpg&name=medium)





### #6. 



























































