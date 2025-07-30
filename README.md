Introduction:

1.The web application gives the user two options: Check In and Check Out.
2.Check In: The Visitor is asked to enter his/her and Host's details.Thereafter,a SMS and E-mail is sent to the Host giving the details of the Visitor.
3.Check Out: The Visitor is asked to enter his/her E-mail Id for verification and after it the visitor is checked out.

Workflow:

1.Visitor is given the option to Check-in.
2.Visitor is asked to fill his own details as well as the host's details whom he wants to meet.
3.Visitor is then given the option to Checkout.
4.At the time of checkout, the Visitor is asked to enter his Email-id for verification.
5.After this, the visitor is checked out of the system.
6.A visitor can check-in and checkout at any time irrespective of the other visitors.

Database 'user' and it's Collections are designed as following:

Clients: Contains details specific to the visitors.
|___Clients
        |___name 
        |___email
        |___phone
        
Hosts: Contains details specific to the hosts.
|___Hosts
       |___hname
       |___hemail 
       |___hphone

Visits: Contains details specific to the visits by visitors(Check-in - Check-out).

|___Visits
       |___email
       |___checkin
       |___checkout
       |___hemail

I have made 3 collections so as to reduce redundancy in the database. Even if a visitor has visited the office more than once, his details will only be stored once in the Clients collection. The same goes for the Host's Details.

Corner Cases:
A visitor cannot check-in again if he/she is already checked in and has not checked out.
A visitor cannot checkout with an Email-Id that has not been used to Check-in.
A visitor cannot checkout again if he/she is already been checked out.


Screenshots:
Entry Management System's Home Page.
<img width="1920" height="1030" alt="Home" src="https://github.com/user-attachments/assets/ee823cf8-d878-4a84-9096-ae21d1ccf2c3" />

Check-in Portal.
<img width="1920" height="1027" alt="Checkin" src="https://github.com/user-attachments/assets/c9b0944d-ef10-44e0-bf4f-25b03b6b3651" />

Check-in Success Message.
<img width="1920" height="1027" alt="Success_checkin" src="https://github.com/user-attachments/assets/a1a1a154-e4d2-44b4-a65d-0ef9b522b5b6" />

Check-out Portal.
<img width="1920" height="1027" alt="Checkout" src="https://github.com/user-attachments/assets/2a468f9c-9349-4765-9e6a-b158b6ef88ce" />

Check-out Success Message.
<img width="1920" height="1027" alt="Success_checkout" src="https://github.com/user-attachments/assets/855d586f-f900-4cf6-b12d-8e98dc90d9d6" />

Error Messages.
<img width="1915" height="726" alt="Error1" src="https://github.com/user-attachments/assets/40e54816-fa0b-47bd-9cf4-8d499b83b844" />

<img width="1795" height="682" alt="Error2" src="https://github.com/user-attachments/assets/c3e21e98-6885-4d24-a344-db275c06507a" />

<img width="1445" height="472" alt="Error3" src="https://github.com/user-attachments/assets/a5d861fb-004b-4c00-8436-8e485ce07b4e" />




