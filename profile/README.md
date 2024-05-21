<h1><b>Magicbooks.io Rewarded Book Preview API</b></h1>
<a href="https://www.npmjs.com/package/magicbooks-api">NPM Package - Wrapper Around API</a><br/>
<a href="https://bookboostpro.magicbooks.io/books.html">Demo One</a><br/>
<a href="https://apidemo.magicbooks.io/">Demo Two(using npm package)</a><br/>

https://github.com/Magicbooks-io/.github/assets/62707165/85a64062-2796-44a3-8e4e-617476d3c79a









<p>Something magical happens when humans are rescued from the endless scrolling feeds of social media and brought into the simple and ancient book-like format.  
 Add music and media, create a pivotal role for the great developers of the world, and this project which started as a shot towards the 'unreachable star' gets very interesting. What is outlined here is a quick view of the engine.</p>


<p>The Magicbooks.io API hopes to create a vast new income stream for developers and bloggers by making it easy for ordinary people to monetize with rewarded book previews while creating a better way for authors and creators to monetize books and any valuable content.</p>

<img src="https://github.com/Magicbooks-io/.github/assets/62707165/b0dc6974-9259-46ef-af77-4cc2fa844e65">

 <h1>MagicBooks API Documentation</h1>

<h2>Introduction</h2>
<p>Welcome to the MagicBooks API, a platform that allows third-party developers to integrate rewarded book previews and contribute data to strengthen the book chain.</p>

<h2>Table of Contents</h2>
    <ol>
        <li><a href="#introduction">Introduction</a></li>
        <li><a href="#getting-started">Getting Started</a>
            <ul>
                <li><a href="#install-via-npm">Install Via NPM</a></li>
                <li><a href="#api-endpoint">API Endpoint</a></li>
                <li><a href="#authentication">Authentication</a></li>
            </ul>
        </li>
        <li><a href="#creating-book-sessions">Creating Book Sessions</a>
            <ul>
                <li><a href="#request">Request</a></li>
                <li><a href="#response">Response</a></li>
            </ul>
        </li>
        <li><a href="#monetizing-with-rewarded-book-previews">Monetizing with Rewarded Book Previews</a></li>
        <li><a href="#contributing-data">Contributing Data</a>
            <ul>
                <li><a href="#create-an-app">Create An App</a></li>
                <li><a href="#session-events">Session Events</a></li>
            </ul>
        </li>
        <li><a href="#examples">Examples</a></li>
    </ol>

 <h2>Introduction</h2>
 <p>MagicBooks.io API allows game and app developers, bloggers, and website owners to integrate rewarded book preview ads into mobile applications and websites.</p>
  
 </p>Rewarded Book Preview Ads is a new category of rewarded ad format which includes multiple goal-oriented delivery-methods and strategies.</p>
 <p>For example:</p>
 <ul>
  <li>1. Authors can monetize digital books by allowing readers to read a preview, then direct the reader to purchase a book or allow them to continue reading in exchange for viewing a relavent and data-driven advertisement.  Advertisers purchase ad slots, pay for each verified engagement, can opt into paying commissions for sales and/or elect custom strategies based on the advertising goals. The author or creator of the magicbook earns 100% of this direct ad-revenue and can elect to share said revenue with third-party developers who display the magicbook and ads, contribute ephemereal data to the book chain to improve targeting, and enhance engagement and ad-displays through skilled ux design and creativity.</li>
  
  <p>Note: Our studies show authors and creators can viably earn many times the amount they would for a book under the primitive model of only buying and selling books; and developers can earn many-times more than with adsense or comparable global ad-networks, while continuing to utilize any ad-server with the freedom all developers should enjoy.</p>
 
 <li>2: Businesses can create product catalogs, whitepapers, and any content-oriented marketing, setting per click bids and real-time header bidding.</li>
 
 <li>3:Developers can sell and mediate first-party ads, earn for contributing valuable data to the decentralized bookChain,
  and participate in the development and growth of a new method and channel for online advertising while creating 
  a source of wealth controlled by ordinary people, authors, creators, educators, musicians, and developers, free from harsh censorship and poised to attract a new generation of small businesses embracing the creator-driven online ad market.</p>

 <h2>Getting Started</h2>
 <h3>Install Via NPM</h3>
 <p>We created a simple wrapper around the API you can install via NPM:</p> 
 <code>npm install magicbooks-api</code>
 <h3>API Endpoint</h3>
 <p>The base API endpoint for all Magicbooks.io api calls is:</p>
 <code>https://api.magicbooks.io/{endpoint}</code>

 <h3>Authentication</h3>
    <p>To use the API, include the following parameters in the URL:</p>
    <ul>
        <li><code>appId</code>: Unique identifier for the developer's application.</li>
        <li><code>key</code>: API key associated with the provided <code>appId</code>.</li>
    </ul>

 <h3>Retreiving A List of Books</h3>
   <h3>Request</h3>
   <p>Make a GET request to the below endpoint with the required parameters:</p>
   <pre>GET https://api.magicbooks.io/getBooks?appId=[appid-string]&amp;key=[apikey-string]</pre>

 <h3>Response</h3>
    <p>The API will respond with a JSON object containing the following information:</p>
    <ul>
    <li><code>books</code>: Array containing published book objects.</li>
     <br/>
        <pre>{
            "id": "BmGUwGXVQlUnBPvAFRe8",
            "title": "Magicbooks.io For Smarthomes",
            "author": "Magicbooks4Smarthomes",
            "coverImage": "https://res.cloudinary.com/wikacy-com/image/upload/v1688345016/book-covers/smacdoubovpvy1srvvhl.jpg"
        }</pre>
        <br/>
        <p>Display the books however you like.  Members can create, sell, and monetise all kinds of templates, interactions, automations, and plugins to extend the value of each book app/channel.</p>
     
    
   <li>Information regarding prior bookSessions, first-party ads, bid-amount, payout amounts, top-performing books, ad-slot-trading, and user-keys(ephemereal) can be configured by each developer by contributing to the bookChain(see documentation in Magicbooks.io for more details)</li>
   
   </ul>

<h2>Creating Book Sessions</h2>
    <h3>Request</h3>
    <p>Add a click-event listener to  each item to trigger e a GET request to the API endpoint with the below parameters:</p>
    <pre>GET https://api.magicbooks.io/bookSession/create?appId=[appid-string]&amp;key=[apikey-string]&amp;=bookId=[bookId-string]</pre>

 <h3>Response</h3>
    <p>The API will respond with a JSON object containing the following information:</p>
    <ul>
        <li><code>bookSessionId</code>: Unique identifier for the created book session.</li>
        <li><code>bookId</code>, <code>adId</code>, <code>advertId</code>, <code>category</code>, <code>userId</code>: Information about the book session.</li>
        <li><code>loadUrl</code>: URL to load the rewarded book preview.</li>
    </ul>
<p>(see also the Magicbooks-API NPM Package</p>
 <h2>Monetizing with Rewarded Book Previews</h2>
    <p>Developers can monetize applications by displaying the rewarded book previews loaded from the provided URL. Users will be rewarded for engaging with these previews in multiple ways, and all session events are logged and made available via the sessionEvents/{sessionId} endpoint as well as a Magicbooks.io Developers Dashboard</p>

 <h2>Examples</h2>
    <h3>Creating a Book Session</h3>
    <p>Sample JavaScript code to create a book session:</p>
   <pre>
   const fetch = require('node-fetch');
   const appId = 'developerAppId';
   const apiKey = 'developerApiKey';

   fetch(`https://api.magicbooks.io/bookSession/create?appId=${appId}&amp;key=${apiKey}`)
        .then(response =&gt; response.json())
            .then(data =&gt; console.log(data))
            .catch(error =&gt; console.error(error));
   </pre>

  <h2>Developers Selling and Managing Ads</h2>
    <p>One unique feature of MagicBooks API is the singular feature which allows developers to take full control of the advertising strategy. By submitting the <code>advertId</code> and <code>adId</code> parameters, developers can:</p>
    <ul>
        <li>Create and sell their own ads directly through the API.</li>
        <li>Generate dynamic ads using the <code>ad/create</code> endpoint.</li>
        <li>Sign up new advertisers using the <code>advertiser/create</code> endpoint.</li>
        <li>Access the whitelabeled ad portal to manage creatives, products, brand guidelines, and analyze campaign results.</li>
    </ul>
    <p>Developers have the flexibility to:</p>
    <ul>
    <li>Collect independent payments for their ads.</li>
    
   <li>Write their own rules and guidelines governing earnings for contributors to the display and engagement with first-party ads.</li>

   <li>Production members can configure their app to provide an advertising client-portal, sell ads, buy and sell ad slots, and much more.</li>
    </ul>

  <h2>Get Involved in Personalization and Segmentation</h2>
    <p>We encourage developers to get involved and unite behind a way to personalize and segment users without jeopardizing their privacy or exposing their identity.</p>

   

  

   <h2>Create An App</h2>

   <img src="https://github.com/Magicbooks-io/.github/assets/62707165/6bacc4d0-157f-4103-87f2-545b627c54e8">

   <img src="https://github.com/Magicbooks-io/.github/assets/62707165/91e68215-29a4-424d-b616-9bbb75181764">


  <img src="https://github.com/Magicbooks-io/.github/assets/62707165/e5168989-c7f3-428f-bd8b-88fc505a291e">

  <h2>Setup and Display a Book Feed On Any Site</h2>

  ![scrnli_2_5_2024_9-07-42 PM](https://github.com/Magicbooks-io/.github/assets/62707165/c678a2d2-c731-42c9-be7b-70dd60353b16)
  ![scrnli_2_5_2024_9-07-11 PM](https://github.com/Magicbooks-io/.github/assets/62707165/e23fdbc2-c9c6-4be5-9ca5-54814994d8eb)

  <p>Simple and unobtrusive promos can be displayed between pages, on pages, or in any slot you or the bookChain create.  Earn commissions on book sales, products, and promote your own clients, music partners, or anything in a manner which enhances focus and is proven to greatly increase roi. Authors can write books and allow readers to enjoy them for free and earn far more than they ever could under the old primitive model of buying and selling, and developers share in a vast new market and sustain a better way for businesses to connect with consumers.<p>

  

https://github.com/Magicbooks-io/.github/assets/62707165/d1f116e8-1a02-4b95-92b3-6921e6d7ea39



![Untitled design - 2023-11-11T220241 282](https://github.com/Magicbooks-io/.github/assets/62707165/6bacc4d0-157f-4103-87f2-545b627c54e8)
-->
<p>Third Party Apps/Websites</p>
<br/>

![Huawei-P30-PRO-localhost (6)](https://github.com/Magicbooks-io/.github/assets/62707165/ef14ca71-09c1-4448-a74a-f31896aa9313)
<br/>

![Huawei-P30-PRO-localhost (7)](https://github.com/Magicbooks-io/.github/assets/62707165/48463166-6604-402d-8e75-1fe95684c897)

The trail of <a href="https://magicbooks.io/m-page.Page7.html?theme=dark&bookId=tbGRrhhWNXaM9vBReW5p&postType=book">#DonQuixote</a>





