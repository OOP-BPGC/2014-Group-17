Group-17
========

UML:
----

**Class Diagram:** Each class corresponds to a user interacting with the application. All these users need to sign in to perform the corresponding responsibilities assigned to them. Hence they use the login class. The class dependancies and relationships have been depicted. Hostel representatives are essentially members of some hostel. Hence a generalization is depicted. Similarly, the other real world scenarios have been modelled and depicted.

**Sequence Diagram:** The order in which the application is used,which in turn depicts the order in which the functions are called have been described.

**Collaboration diagram:** Each class functions independantly relying only on it's own functions. Hence the collaberation diagram only has self loops. However all the classes implement the interface login which defines the login function and the check rules function. Hence, ALL classes collaberate with login interface.

**Activity diagram:** The sequence of activities taking place in the working of the application beginiing at the login stage and commencing at the logout stage have been depicted. Once the login activity is completed the actvities are branched out according to the resposibility of the user. Subsequent activities are then depicted. Hostel members however can be exemted from login because general functions like checking event schedule and rules do not need special access.


Junit Tests:
------------

Tests contain the test method of each function the code shall implement. Because these functions are basic and independant of other functions, mock objects haven't been used. The function placebet however depends on checkevent because bets can be placed only on those events which are yet to take place. Conditions like date of the event and presence in the event list have to be checked. A mock object has been used to test this function and is added in the folder named MockObjects.

Some of these functions throw exceptions. User defined exceptions like ScoreNotAvailableException and EventNotOccuredException have been added in a seperate folder.


Submission - 14th November, 2014.
---------------------------------

Classes:
--------

**Complete:** 
* Database
* FinanceHead
* HostelMember
* HostelRepresentative  
* Judge
* Login 
* Sponsors
* Utilities

**Incomplete:**
* Convener 
* EventHead


System Requirements
-------------------

* The project assumes that there is an appropriate mySQL database installed on the system, which is currently hosted on the developers' localhost.
* The project requires JDBC drivers for mySQL which can be installed on an Ubuntu system using the command 'sudo apt-get install libmysql-java'. (Instructions regarding this can be found on: http://marksman.wordpress.com/2009/03/01/setting-up-mysqljdbc-driver-on-ubuntu/)
* The project also needs Apache-Tomcat7 installed to host a server to use JSP (not implemented yet).