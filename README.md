HTML and CSS guidelines
=======================

#### Pointers to Remember When Coding HTML:

1) Indent your html codes properly, consider parent-child relationship, (use tabs for indention).

In the example below, notice how img, h1, ul are indented inside their parent element (div#header). Same concept applies to the li’s of ul.

**Bad Coding:**
***
```html
<div id=”header”>
<img src=”logo.png” alt=”Logo” />
     <h1>Sample Website</h1>
<ul>
<li><a href=”“>My Profile</a></li>
<li><a href=”“>Logout</a></li>
</ul>
</div>
```

**Good Coding:**
***
```html
<div id=”header”>
     <img src=”logo.png” alt=”Logo” />
     <h1>Sample Website</h1>
     <ul>
          <li><a href=”“>My Profile</a></li>
          <li><a href=”“>Logout</a></li>
     </ul>
</div>
```

2) Use lower case for HTML and CSS tags.

**Bad Coding:**
***
```html
<DIV ID=”HEADER”></DIV>
```

**Good Coding:**
***
```html
<div id=”header”></div>
```

3) Use names, id names and class names that are readable, descriptive and easy to understand.

**Bad Coding:**
***
```html
<div id=“division_x”>
     <form id=“542_xyz” action=””>
          <p>First Name</p>
          <input type=“fname”></input>
          <input type=“submit”>
     </form>
</div>
```

**Good Coding:**
***
```html
<div id=“right_content”>
     <form id=“registration” action=“process.php”>
          <label for=“first_name”>First Name:</label>
          <input type=“text” name=“first_name” id=“first_name”>
          <input type=“submit”>
     </form>
</div>
```

> *Notice how &lt;label&gt; tag is used instead of &lt;p&gt;.*

4) Properly close HTML elements. The example below shows how to close an input element:

**Bad Coding:**
***
```html
<input type=”submit”></input>
```

**Good Coding:**
***
```html
<input type=”submit”>
```

5) Validate your HTML codes thru http://validator.w3.org. 

6) Use XHTML 1.0 Transitional doctype for now. 

Common errors in validation are related to label and placeholder attributes. For label tags, make sure that the ‘for’ it is referring/pointing to a specific element id of the input element attached to the label. For example:
***

```html
<label for=”first_name”></label>
<input type=”text” id=”first_name” name=”first_name” placeholder=”Your first name”>
```

7) Use id for elements that are unique and class for elements that are usually repeated/reused.

**Bad Coding:**
***
```html
<div id=”main_content”>
     <div id=”info_box”>
          <h1>My essay</h1>
          <p>This is a simple paragraph, some text here.</p>
     </div>
     <div id=”info_box”>
          <h1>My essay</h1>
          <p>This is a simple paragraph, some text here.</p>
     </div>
</div>
```

**Good Coding:**
***
```html
<div id=”main_content”>
     <h1>Articles</h1>
     <div class=”info_box”>
          <h2>My essay</h1>
          <p>This is a simple paragraph, some text here.</p>
     </div>
     <div class=”info_box”>
          <h2>My Codes</h1>
          <p>This is a simple paragraph, some text here.</p>
     </div>
</div>
```

8) Avoid using style tags in your HTML code. (e.g. &lt;br&gt;, &lt;b&gt;, &lt;strong&gt;, &lt;u&gt;, &lt;i&gt;, &lt;hr /&gt;). Maximize CSS.

9) Make sure to use heading tags properly. The &lt;h1&gt; to &lt;h6&gt; tags are used to define HTML headings. &lt;h1&gt; defines the most important heading. &lt;h6&gt; defines the least important heading. 

**Bad Coding:**
***
```html
<div id=”tools”>
     <p>Automotive Tools</p> 
     <ul>     
          <li>Wrenches</li>
          <li>Compressor</li>
          <li>Voltmeter </li>
     </ul>
</div>
```

**Good Coding:**
***
```html
<div id=”tools”>
     <h2>Automotive Tools</h1>
     <ul>
          <li>Wrenches</li>
          <li>Compressor</li>
          <li>Voltmeter </li>
     </ul>
</div>
```

10) Span is an inline element. It is usually used for styling texts inside block elements like p and heading tags. It must not be use as container of block elements.

**Bad Coding:**
***
```html
<h2>My <span class=”red”>essay</h2></span>
<span><p>This is village88.com, lessons are very good and I learn how to code faster.</p></span>
```

**Good Coding:**
***
```html
<h2>My <span class=”red”>essay</span></h2>
<p><span class=”blue”>This is village88.com<span>, where I learn how to code faster and cleaner.</p>
```

11) HTML has block elements that have default css properties such as padding and margin and will always move to the next line such as div, h1, h2, h3, h4, h5, h6, p, table, form, frameset, ul, ol. Meanwhile, inline elements such as a, img, input, span and textarea are displayed in one line but cannot be placed directly inside the body element, they must be within block elements.

**Bad Coding:**
***
```html
<body>
     <a href=”“>Home Page/a>
     <a href=”“>My Profile</a>
     <a href=”“>Logout/a>
     <span>My Advise</span>
     <span>Hello Village88.com student, always follow clean coding</span>
     <p>Leave reply</p>
     <textarea name=”” id=”” cols=”30” rows=”10”></textarea>
     <input type=”submit” />
</body>
```

**Good Coding:**
***
```html
<body>
     <div id=”wrapper”>
          <div id=”navigation”>
               <ul>
                    <li><a href=”“>Home Page</a></li>
                    <li><a href=”“>My Profile</a></li>
                    <li><a href=”“>Logout</a></li>
              </ul>
          </div>
          <div id=”advise_reply”>
               <h2>My Advise</h2>
               <p>Hello Village88.com student, always follow clean coding</p>
              <h3>Leave reply</h3>
              <form id=”reply” action=”process.php” method=”post”>
                     <textarea name=”reply” class=”reply_message”></textarea>
                     <input type=”submit” value=”Save”/>
              </form>
          </div>
     </div>
</body>
```

12) It is better to create a separate CSS file for your page. Put all the styles on that .css file rather that putting the styles inline to the HTML elements.

**Bad Coding:**
***
```html
<div id=”header” style=”border:1px solid #000; margin-top: 15px;”></div>
```

13) For reserved characters in HTML, visit http://www.w3schools.com/tags/ref_entities.asp. These can be used for symbols like » (&raquo).

14) Tables should only be used for data presentation. It should not be used to layout a form nor for designing a web page.

**Proper table format:**
***
```html
<table>
    <thead>
        <tr>
            <th>Last Name</th>
            <th>First Name</th>
            <th>Email</th>
            <th>Due</th>
            <th>Web Site</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Smith</td>
            <td>John</td>
            <td>jsmith@gmail.com</td>
            <td>$50.00</td>
            <td>http://www.jsmith.com</td>
        </tr>
        <tr>
            <td>Bach</td>
            <td>Frank</td>
            <td>fbach@yahoo.com</td>
            <td>$50.00</td>
            <td>http://www.frank.com</td>
        </tr>
    </tbody>
</table>
```

**Helpful Videos:**
***
* <a href="http://vimeo.com/42749532">HTML coding guidelines</a>
* <a href="https://vimeo.com/44226088">Indentation</a>
* <a href="https://vimeo.com/44226809">Naming Convention</a>
* <a href="https://vimeo.com/44228562">Block and inline elements</a>
