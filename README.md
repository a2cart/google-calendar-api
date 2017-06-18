# google-calendar-api

For more information: http://www.a2cart.com/gmail-api-and-google-calendar-api-spring-boot-and-oauth2/

Demo Project for Google Calendar API Using Spring Boot Rest API with OAuth2

This guide shows you how to build a sample app doing various things with "Google APIs" using OAuth2 and Spring Boot. It starts with a simple, single-provider single-sign on, and works up to a self-hosted OAuth2 Authorization Server with a choice of authentication providers (Fitbit or Facebook or Github). The samples are all single-page apps using Spring Boot and Spring OAuth on the back end. They also all use AngularJS on the front end, but the changes needed to convert to a different JavaScript framework or to use server side rendering would be minimal.

Google Calendar API  - Spring Boot and OAuth2

1) Spring Boot
2) Rest API
3) Google Calendar API
4) OAuth2

<h2>What do I do?</h2>

I am simple Spring Boot application which secured by Spring Security. Instead of using simple form based security, I am secured by Spring Security OAuth2 and the OAuth provider is Google.

Why am I required?

Developing a Spring Boot web application with Security enabled and integrated with Google is hard to implement. So this is a sample implementation of Spring Boot + Spring Security OAuth2 + Google Provider.

<h2>Get it up and runnning</h2>

The project is built with Maven so you can run the build using mvn clean build

The application.properties (in src/main/resources) contains the details of the Google application which it uses to authenticate details. Change the values of the following attributes to the values for your application google.client.id google.client.secret and etc.,

###To register a Google App perform the following steps

Go to https://console.developers.google.com and login with your Google account (this will be the developer account and the email of this account will be published when someone tries to authenticate with the Google application)

If you don't have a project create a new one and then click into the project.

In the menu on the left side select "APIs & auth" --> "Credentials" --> "Create a new client ID"

In the popup select the following

Application Type = SpringBoot Web Application

Authorized Javascript Origins = ,

Authorized Redirect URI = , the URI for our application is http://localhost:9000/login/google on different lines.

Copy the client ID and client Secret and update the application.properties

Make sure you update the mandatory values on the "APIs & auth" --> "Consent screen" page as the application will not work without it.

When you have a the Google App configured and the Spring boot application and you navigate to http://localhost:9000/login/google. It will redirect you to a Google login page. Upong login it will ask you to authorize your application for access to your account to get email and profile data. On successful login it will render the basic HTML page which means the authentication was sucessful.

<!-- Google Calendar Maven Dependency-->

		<dependency>
			<groupId>com.google.apis</groupId>
			<artifactId>google-api-services-calendar</artifactId>
			<version>v3-rev224-1.22.0</version>
		</dependency>

		<!-- Gmail Maven Dependency-->
		<dependency>
			<groupId>com.google.apis</groupId>
			<artifactId>google-api-services-gmail</artifactId>
			<version>v1-rev65-1.18.0-rc</version>
		</dependency>


That’s it. Thank you for reading this post.

Enjoy!!!

www.a2cart.com
