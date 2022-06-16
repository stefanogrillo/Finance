# Finance
This is a Financial Web App: you can search, buy, and sell any share available in the market.

This is a [guided project](https://cs50.harvard.edu/x/2022/psets/9/finance/) from CS50 course. My solution to the project is available [here](https://github.com/stefanogrillo/CS50-s-Introduction-to-Computer-Science-2021-2022/tree/main/pset9/finance). My core objectives were: create a Register Page for new users, a Log In, an Index, a page to see current Quotations, a Buy page, a Sell page, an History of transactions, an Add/Withdraw Cash, and the possibility to Change the Password for the user. 

This Web Application is developed using <i>Python's Flask</i> for the backend, and using <i>HTML</i>, <i>CSS</i>, <i>JavaScript</i> and <i>Bootstrap</i> for the webpage. The webapp has a database in <i>SQLite</i>, and uses an <i>API</i> to retrieve information about the shares' quotations from <i>IEX</i>.

The application starts asking to the user to <i>Register</i> his/her own account. The <i>Registering</i> process requires the user to insert a password with some constraints: a Lowercase Letter, an Uppercase Letter, a Number, and a total Length of 8 Characters. This is implemented in <i>JavaScript</i>. Once the requirements are met, the password should be rewritten so to check if there are typos. When password match, the registration is completed inserting the username and the encrypted password in the <i>SQLite</i> database. This will allow the user to enter the application.

![](https://github.com/stefanogrillo/Finance/blob/ae6896c73ef93c783e117d5411a7368507dbb76e/register.gif)

The <i>Log In</i> process is easier: it only requires the username and the password. Without this step, no other branches of the application are reachable: each new page requires Log In by backend.

![](https://github.com/stefanogrillo/Finance/blob/2f50b2816f9b24987c184d2741b81677de43bfc5/login.png)

After these steps, the user is welcomed into an <i>Index</i> where his/her transactions are shown, grouped by Symbol/Name. The total amount of shares on hand are shown, their value at aquisition, and the total amount spent. Here I added hyperlinks to Buy and Sell pages. Moreover, the total amount of cash inserted in the Webapp is visible in down-left corner outside the striped table. In the striped table is visible how much cash is available yet.

![](https://github.com/stefanogrillo/Finance/blob/2f50b2816f9b24987c184d2741b81677de43bfc5/home.png)

The quote page is where the user can look for the current price of shares of a specific company, by knowing the Symbol.

![](https://github.com/stefanogrillo/Finance/blob/43211ac751ab3b7edce6b3ed0f4e0935a92fe402/quote.gif)

