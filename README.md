# Rajesh-Mailing-Service

This is a java library which helps you to send emails from java.

## Installation

Just download the required version from this respository and add this .jar files to build path

## Usage

```java
package com.itsmrajesh.mail;

public interface MailAuth {

	String getHostMailAddress();

	String getHostPassword();

}
```


```java

import com.itsmrajesh.mail.MailAuth;

public class MyMailAuth implements MailAuth {

	@Override
	public String getHostmailaddress() {
		return "example@gmail.com";
	}

	@Override
	public String getHostpassword() {
		return "********"; // your password 
	}

}


```


You need to implement this(MailAuth) interface and invoke following method

```java

//create object for newly implement class and pass it in follwing method

MailAuth mailAuth = new MyMailAuth(); 

boolean status = MailService.sendMail(MailAuth mailAuth, String recipientMailAddress, String mailSubject, String message);

```

status will be true when your mail sent is succesfull.
