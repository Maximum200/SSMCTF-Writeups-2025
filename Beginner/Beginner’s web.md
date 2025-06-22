### Beginner’s web



![alt_text](images/image5.png "image_tooltip")


This website is a simple way to learn the beginning of web problems in CTFs. 


![alt_text](images/image14.png "image_tooltip")


The challenge is split up into 4 easy parts. The 1st part is to find a flag part hidden in the console of the developer tools.



![alt_text](images/image3.png "image_tooltip")


The 2nd part of the flag is shown here:



![alt_text](images/image17.png "image_tooltip")


To find the next part of the flag, we need to check the cookies of the page.




![alt_text](images/image18.png "image_tooltip")


The cookie is stored under the “applications” tab, under the cookies tab. The name of the cookie is “MXNfczA”.

Placing this through Cyberchef ([https://gchq.github.io/CyberChef/](https://gchq.github.io/CyberChef/)), we get this output: 



![alt_text](images/image6.png "image_tooltip")


Now, we need to find the 3rd part of the flag.


![alt_text](images/image4.png "image_tooltip")


For this task, we need to use Burpsuite ([https://portswigger.net/burp](https://portswigger.net/burp)). We will use this to change the submit request into a POST request. 


![alt_text](images/image12.png "image_tooltip")


Using Burpsuite, I changed the ‘GET’ request into a ‘POST’ request. This yielded the following output: 



![alt_text](images/image2.png "image_tooltip")


Now, it’s time to find the last part of the flag. 



![alt_text](images/image16.png "image_tooltip")


First, we’ll try the stated endpoint, /read?file=blogs1.txt. This yielded this output:



![alt_text](images/image9.png "image_tooltip")
 Instead, let’s try a more common endpoint, which is often flag.txt. 




![alt_text](images/image11.png "image_tooltip")


Flag: SSMCTF{W3b_1s_s0_f4n_64cf55}