### ``` Collection of Everything related to BugBounty Stuffs in Organized Manner```

------



> ### Point to Remember =>
>
> > Recon is the Game => Dig more to the Targets
>
> > Hunting on Target as SCOPE Base =>
> >
> > ​	Small Scope | Medium Scope | Large Scope
> >
> > * **Small Scope** => Specific set of Single URLs/Sandbox/QA/Staging Environment
> > * **Medium Scope** => Specific set of  `***.target.com**`
> > * **Large Scope** => Complete Internet Presence including Acquisitions & Copyrights
>
> > Understand Application Business Logic
>
> > Do Application Specific Attacks
>
> > Make Document Notes of Targets
>
> > Keep Update to Latest Vulnerabilities , CVEs, News, WAF Bypasses from Community
>
> > Learn Manual Hunting => Be a BurpSuite Ninja
> >
> > 
> >
> > * Walk Through to Applications
> > * List all Component & Functionality 
> > * Write Theoretical Attack Scenarios for Each Functions
> > * Remember CRUD Scenarios => Create , Read, Update, Delete
> > * Experiment with Parameters  | Headers | Reqeust + Response Manipulation | VERB Tamperng [GET | POST | OPTIONS etc]
> > * Figure Out Various Possible Flows os Same Feature [ Example => password reset feature, email setting feature etc]
> > * Try To Break the Application FLOW
>
> > Web Security Learning PATH =>
> >
> >
> > https://portswigger.net/web-security/learning-path





### SCOPE Based RECON =>

================================





### Small Scope =>



- [ ] Directory Enumeration/Bruteforcing
- [ ] Service Enumeration
- [ ] CVEs
- [ ] Port Scanning
- [ ] Broken Link Hijacking
- [ ] JS Files for Hardcoded APIs & Secrets
- [ ] Parameter Discovery
- [ ] Wayback History & WaybackURLs
- [ ] Google Dork + Shodan + Other Online Service
  - [ ] Look for Juicy  Info related to Scope Domains
- [ ] Potential  URL Extraction for Vulnerability Automation 
  - [ ] GF Patterns











### Medium Scope =>



- [ ] Subdomain Enumeration
  - [ ] Amass + Subfinder + Findomain + Assetfinder
- [ ] Subdomain Takeovers
  - [ ] subjack
  - [ ] subover
- [ ] Misconfigured  3rd Party Services
- [ ] CVEs
- [ ] Port Scanning
  - [ ] Naabu + Masscan + Nmap + Rustscan
- [ ] Misconfigured Storage Options [S3 Buckets]
- [ ] Broken Link Hijacking
- [ ] Directory Enumeration
  - [ ] FFUF + Turbo Intruder
- [ ] Service Enumeration
- [ ] JS Files for Domains , Sensitive Information [ Hardcoded APIs & Secrets]
- [ ] GitHub RECON
- [ ] Wayback History
- [ ] Google Dork for Increasing Attack Surface
- [ ] Internet Search Engine Discovery
  - [ ] Shodan
  - [ ] Censys
  - [ ] FOFA
  - [ ] BinaryEdge
  - [ ] Spyse etc
- [ ] Potential URL Extraction for Vulnerability Automation
  - [ ] GF Pattern & Automation Scripts





### Large Scope =>



- [ ] Tracking & Tracing every Possible signatures of the Target Application
- [ ] Subsidiary & Acquisition Enumeration [Depth - Max]
- [ ] DNS & SSL Enumeration
- [ ] CVEs
- [ ] ASN & IP Space Enumeration and Service Identification
- [ ] Subdomain Enumeration
- [ ] Subdomain Takeovers
- [ ] Misconfigured 3rd Party Services
- [ ] Misconfigured Storage Options [S3 Buckets]
- [ ] Broken Link Hijacking
- [ ] Directory Enumeration
- [ ] Service Enumeration
- [ ] JS Files for Domains, Sensitive Information [Hardcoded APIs & Secrets]
- [ ] GitHub Recon
- [ ] Parameter Discovery
- [ ] Waybackurls
- [ ] Goole Dork
- [ ] Internet Search Engine
- [ ] Potential URL Extraction for Vuln Automation
- [ ] And Any Possible Recon Vector [Network/Web]



------



## Following are the Important Links + Writeups + Tips



###  #1. RECON Game



> Check AllThingsRecon.md File





------



## #2. All Things IDOR 



> Check AllThingsIDOR.md File





------



### #3. All About Injection 



Command Injection + SQL Injection

> Check AllThingsInjection.md File





### #4. All Things XSS



> Check AllThingsXSS.md File



### #5. All Things Account Takeover



> Check AllThingsATO.md File





### #6. All Things Race Condition



> Check AllThingsRaceCondition.md File





### #7. All Things Open Redirect



> Check AllThingsOpenRedirect.md File



### #8. All Things SSRF



> Check for AllThingsSSRF.md File





### #9. All Things SSTI



> Check for AllThingsSSTI.md File





### #10. All Things Subdomain Takeover



> Check for AllThingsSubdomainTakeover.md File









