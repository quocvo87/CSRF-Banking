| 1. Introduction
----------------
    Package will help you buil list functions global are used usually 

    This package will show how hacker can attack to victim with CSRF


| 2. Directory Struct
-----------------------

    Root
    |__src
    |   |__config
    |   |   |__config.php -> change your user/pass here
    |   |
    |   |__Support      -> Base class
    |       |__helpers.php      -> global functions
    |
    |
    |__index.php -> dashboard page, it need to login first. 
    |__transfer.php -> this form is used to transfer

-----------------------


| 3. Step by step do it
-----------------------

    3.1 Clone/download CSRF_Banking folder to your computer
        3.1.2 Download
            + Goto D:\YourFolder folder, download this CSRF_Banking to D:\YourFolder\

    3.2 Config your user/pass at D:\YourFolder\CSRF_Banking\config\config.php
            + using: crypt('yourpassword');

    3.3 Create virtualhost for this source
        + Example: csrf-banking.local ---mapping---> D:\YourFolder\CSRF_Banking

    3.4 Run for test
        + Open browser and goto http://csrf-banking.local
        + Login: with your user/pass
        + You're see: your account balance: $1.000.000


-----------------------

| 4. Victim site
-----------------------

    4.1 Example: you're on facebook, and you saw a message "click here to get gift"

    4.2 You're login on http://csrf-banking.local and you have session of http://csrf-banking.local

    4.3 You're lost money when you click on link step 4.1, you had attacked with CSRF

    4.4 Example site victim as below
        4.4.1 You're download : https://github.com/quocvo87/CSRF_Injection
        4.4.2 You have: D:\YourFolder\CSRF_Injection
        4.4.3 Create virtualhost for this source
            + Example: csrf-injection.local ---mapping---> D:\YourFolder\CSRF_Injection
        4.4.4 You click on link: You are getting $5,000
        4.4.5 After that: hacker will use your Session from csrf-banking.local to transer money
                from your account to him

        4.4.6 Now: you can check your account balance at: http://csrf-banking.local, 
                you will be lost $10.000

-----------------------

