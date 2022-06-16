# Finance
This is a Financial Web App: you can search, buy, and sell any share available in the market.

This is a [guided project](https://cs50.harvard.edu/x/2022/psets/9/finance/) from CS50 course. My solution to the project is available [here](https://github.com/stefanogrillo/CS50-s-Introduction-to-Computer-Science-2021-2022/tree/main/pset9/finance). My core objectives were: create a Register Page for new users, a Log In, an Index, a page to see current Quotations, a Buy page, a Sell page, an History of transactions, an Add/Withdraw Cash, and the possibility to Change the Password for the user. 

This Web Application is developed using <i>Python's Flask</i> for the backend, and using <i>Python's Jinja</i>, <i>HTML</i>, <i>CSS</i>, <i>JavaScript</i> and <i>Bootstrap</i> for the webpage. The webapp has a database in <i>SQLite</i>, and uses an <i>API</i> to retrieve information about the shares' quotations from <i>IEX</i>.

The application starts asking to the user to <i>Register</i> his/her own account. The <i>Registering</i> process requires the user to insert a password with some constraints: a Lowercase Letter, an Uppercase Letter, a Number, and a total Length of 8 Characters. This is implemented in <i>JavaScript</i>. Once the requirements are met, the password should be rewritten so to check if there are typos. When password match, the registration is completed inserting the username and the encrypted password in the <i>SQLite</i> database. This will allow the user to enter the application.

![](https://github.com/stefanogrillo/Finance/blob/ae6896c73ef93c783e117d5411a7368507dbb76e/register.gif)

The <i>Log In</i> process is easier: it only requires the username and the password. Without this step, no other branches of the application are reachable: each new page requires Log In by backend.

![](https://github.com/stefanogrillo/Finance/blob/2f50b2816f9b24987c184d2741b81677de43bfc5/login.png)

After these steps, the user is welcomed into an <i>Index</i> where his/her transactions are shown, grouped by Symbol/Name. The total amount of shares on hand are shown, their value at aquisition, and the total amount spent. Here I added hyperlinks to Buy and Sell pages. Moreover, the total amount of cash inserted in the Webapp is visible in down-left corner outside the striped table. In the striped table is visible how much cash is available yet.

![](https://github.com/stefanogrillo/Finance/blob/2f50b2816f9b24987c184d2741b81677de43bfc5/home.png)

The quote page is where the user can look for the current price of shares of a specific company, by knowing the Symbol. A must-do step before buying.

![](https://github.com/stefanogrillo/Finance/blob/43211ac751ab3b7edce6b3ed0f4e0935a92fe402/quote.gif)

The successive step is to actually Buy the stocks. The transaction will be immediately recorded in the <i>SQLite</i> database. 

![](https://github.com/stefanogrillo/Finance/blob/1cad0265b936e2db2c3b084e479f5f918d99fe91/buy.gif)

However, the user can also sell his/her shares in the Sell page. Here a dropdown <i>Jinja</i> menu will allow the user to choose the shares' Symbol, then he/she is allowed to change the quantity to be sold.

![](https://github.com/stefanogrillo/Finance/blob/1cad0265b936e2db2c3b084e479f5f918d99fe91/sell.gif)

Then, a History page is necessary to show every transaction ever occurred. Here the list starts from the oldest to the newest.

![](https://github.com/stefanogrillo/Finance/blob/68407c76b49da92479d640a8b2251851ce022504/history.gif)

THe user is also allowed to insert his/her own money in the Add/Withdraw page. Here the user has to insert an IBAN between 11 and 14 characters long, with the first two characters being letters. It is a way to mimic actual IBANs, yet I have a [python code](https://github.com/stefanogrillo/CS50-s-Introduction-to-Computer-Science-2021-2022/blob/beae58af3d5e4f14de0f357948f07b400dd1c264/pset6/credit.py) to check if the IBAN exists as a MasterCard, American Express, Visa, or Invalid. This is Luhn's algorithm, which I did not implement in this Webapp. 

![](https://github.com/stefanogrillo/Finance/blob/68407c76b49da92479d640a8b2251851ce022504/addwithdraw.gif)

Finally, the user can also Change his/her Password. Here, the user must insert his/her username and old passwords, that will be chached in th database. If username and  password are already in the database (thus meaning the current user has not stolen the account of someone else), then the new password can be inserted. This follows the same constraints as in the Register phase an must be checked against the repeated new password. If these constraints are met, the new password is inserted in the database (encrypted) instead of the old password.

![](https://github.com/stefanogrillo/Finance/blob/1e8d3d8fcc9e936f6014ae5db831846436056350/changepassword.png)

In case of error, the Webapp will show an auto-update message with a meme. The following is an example.

![](https://github.com/stefanogrillo/Finance/blob/243005a920eb564454917b09ec8514b3f3990e0d/error.gif)

So that's my project. There are a few personal touches here and there that I wanted to implement in the page, like a JavaScript for the password checking, the possibilities to add/withdraw cash, or the welcoming message when you first enter the app (the blue line with "Welcome Back!").
Thank you for watching this. 
