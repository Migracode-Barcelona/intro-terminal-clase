# Heroku Deployment

## What is Heroku?

{% hint style="info" %}
&#x20;**Heroku is a hosting services platform, and offers free services to allow us to publish our final** projects for free!
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=H2Q4vJrxTwo" %}

## **Heroku Deployment First steps**

### **Register**

First of all register an account in [Heroku Website](https://id.heroku.com/login)

Then install Heroku Command Line Interface (CLI), it makes it easy to create and manage Heroku apps directly from the terminal. It’s an essential part of using Heroku.

[**https://devcenter.heroku.com/articles/heroku-cli#download-and-install**](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)

### Login

After install it, go to the terminal and write:

```bash
heroku login
```

It will open a browser with a button to login if you are already logged, if not you will have to write your credentials:\
****

![](https://lh4.googleusercontent.com/lHXBLBZhz4kRR5UB1KBTr3FDeSKJ0fmEIrZF25ZF3QJ1tpifoOBjjdimLSbrZNlGn3FTp0o8hsnR63t1lMqjp8xoJOFglsnQVyDtZZyjuTnGQ555nqyVO7kNwKe535\_sg0xV94mf)

## **Deploy the project**

In our project we will have to deploy 3 elements:&#x20;

1. Front End Code
2. Back End Code
3. SQL Database

We will divide the Heroku project into 2 applications:&#x20;

1. Front End Application
2. Back End Application

Create the 2 applications!

{% hint style="info" %}
**IMPORTANT: DO NOT USE A CREDIT CARD (IS NOT NEEDED)**\
Create both applications in the “Personal” area, if you create a Team you will have to complete a form with your credit card, and later all the applications will have a monthly cost.
{% endhint %}

### **Front-end Application**

Create an application for the front-end code, click in New button:\
****

![](https://lh3.googleusercontent.com/HMuGY7\_kzXdEDSLavp7II7hFyV4XmFrVKWAf00F5yVHdKoesahbVGrBywQ6u7FWTca4cqf4OW4am\_PARFS\_ry-06ha3J1HZR6w0l3hq62WDhSiwEIMO98wqR8b9any8OqPGpv3wu)

Write an available name, choose a good name because it will publish a unique URL to access to your project like: [https://your-app-name.herokuapp.com](https://your-app-name.herokuapp.com)

Choose Europe as the region:

![](https://lh5.googleusercontent.com/b0\_CON9U3cTQCZ3mxZvyfMKaNZENrFC5Bf\_hVeJwoTl79ZBzgymVMqiwFO4nbf9osAqihFPVxlrIr0RtoGv0dmxkAwzSEGLNWbCFocXnR6Lnx53ZnqH5PvkHiDLfWc\_ghGUH4uS6)

Using your terminal go to the project directory and checkout the branch you want to deploy, normally master or main, then write:

```bash
heroku git:remote -a “your_app_name”
```

It will create a new remote repository, it means that from now you will have two, one for GitHub and a new one for heroku. From now when you push changes again you will have to specify where do you want to push:

To push your commits to Github.com:

```bash
git push origin master
```

To push your commits to Heroku and deploy a new version in the public URL

```bash
git push heroku master
```

To check the deployed version in heroku, you can write:

```bash
heroku open
```

or just put the complete URL in the browser: [https://your-app-name.herokuapp.com](https://your-app-name.herokuapp.com)

![](https://lh4.googleusercontent.com/l2K2MREOAZJNYtoOCYBdSSr96TRehF\_dhZKqCJP9khxvlxBElQO3eVejRqg48844qV9TV3taksNx7dmVJlLckzaPmhVWGA5WgNgxww6Wn02UCkCqgkujnl7DzUOQkJvH-Hkfq43t)

### **Back-end Application**

You have to repeat the same process done in the front-end version.

The only difference is that the public URL that you will choose, you will not have to share it, because normally only you front-end application will access to this URL.

### **Database**

Go to the back-end application in the Heroku platform, and in “Resources” tab, add the Postgres add-on:

![](https://lh5.googleusercontent.com/HzuP6J92oDums1qdRDbQS-eZhKy-9zOYUGSSYCqFfI1pnZH8zm4wDUgVtwv\_eYverfh8S\_-sHQVnHF4kIvOZgp3UjBslkC5quoKi3G9rTzcvPlrVoxetcyU7-O8cs-FIKXob7sI1)

Click in Provision button, then it will appear in the project:

![](https://lh4.googleusercontent.com/6YZcoi5TMpepCiRhS4ENX-Eub6JLEEr0cI2uW-4nOQBk\_HzSWX-en39nKS\_XKPlAnWVtMfxQDYMAWgRWbSDRC5JZ1YpR8x0NpWGerZWpktobLjAImHPw29Qpf7\_7\_8as49ERygrD)

If you click in “heroku Postgres” link you can access to the database information.

![](https://lh5.googleusercontent.com/UAGSncDG\_OwQF5fKAWhqVbwtTN-zUHXObETu4jdUoU5o5o7msukNQq3GRXc6MQ3tWJUgMgSC58aMi8QH\_W9eqBXnALHffNsASMU-Fqp0WIsNwz7EJHo4A-BFT9bHwOPT1kg5XdRD)

Go to Settings and View Credentials button:

![](https://lh3.googleusercontent.com/BmbyOvReCreUgTwOx08ON6elPOmE8OuvA4pvMtxUP6J0Eb3VgnjGF4uKt5i-V7FyqsfQOkFLEwBoflI2BE7G2SZ6IBH1sfqqCUxHdDE--lKiwqlHBzYkudJ6kYzrrJgBuOv7j0VL)

Then you can see the connection information to access the database from your application and from DBeaver:\
****

![](https://lh4.googleusercontent.com/mr1S9ypXA-LCEl6skaQbtZm1KHEKmyi3x3OoOm0CT4-JBWK5GsFUc\_I0WuAbzb\_yD3D4hneStwDSgLGbsNKnophHR\_Iu-IBLCALGjwN3cDJxrCSrsOOY1tXVUJK1bYRb3jaQc0oU)

![](https://lh3.googleusercontent.com/hqFkh\_eFkgm5O8uBppwKVv-Kn3Dt-JuyF7I8XU8SvDgg2Nicgzg4qUeGEhqjyOyof86OwN2z0ARHf18UsxOjFOjHvh3J2ob7ZxCe4iLns6Y6giUTdQqT3udnCO3Ul-oRGk4qkuAU)

So now you can execute your scripts, as if you were working in your computer:

![](https://lh4.googleusercontent.com/8cufF6loPfTEjuRESl8FvsXoZzJE1AfMitepjo5NwFpH1b6oUvSkEB2Fus0FS4Z\_15zTmkNe\_cDz2DlJzUIfsYd59N-GswfXeFeVI7mJwOBgRreyk3Iv69xeY0A1DbcquQ2genoP)

## **Environment variables**

To Link the applications between them (the front-end send a request to the back-end) you will have to configure the new URLs and new ports (the URL will not be localhost and the port will not be 3000)

Also check that the deployed backend to connecting to the deployed Database using a public URL

Use secrets.js or ENV files to configure new addresses.

## **Heroku Extra features**

### **Add a Custom Domain**

Add a custom domain ([www.yourdomain.com](https://www.yourdomain.com)) to your application.

Follow the guide: [Adding your custom domain to heroku app](https://medium.com/@imranhsayed/adding-your-custom-domain-to-heroku-app-cdd68d2db67f)

But also you will have to make some changes in your domain provider webpage, if you are using GoDaddy follos this guide: [Adding a GoDaddy domain to your heroku app](https://tekloon.medium.com/a-beginner-friendly-guide-to-configure-godaddy-custom-domain-names-to-heroku-app-2019-edition-3561c721762)

### **Configure SSL**

\<to be completed>

## **Deployment Guides**

### **Buy a Domain**

\<to be completed>

{% embed url="https://godaddy.com" %}

### **Buy SSL certificate**

**There are a lot of options:**

Buy the SSL with Heroku, which costs if 20$ per month.

Godaddy when I speak with them, they offer a discount, 55,27€ per one year or 118,27€ per two years.

Free SSL with [Zerossl.com](http://zerossl.com/) . They offer a free plan for three months and then you would have to reinstall it again (also free) every three months.

## **** **** **** ****

****

****\
****

****



\


