## Important Topics Covered
1. Dependencies, Package Manager, Bundlers
2. Responsive Grids
3. Infix and Modifiers in Bootstrap
4. Static and Dynamic Content, Caching
5. Single Page Applications
6. Virtual DOM
# Intro to UI Frameworks and Libraries

### Working with Libraries
##### What are dependencies? 
Packages and other libraries you use are dependencies because your application depend on them to properly work. 
##### Why do you use Package Manager? 
Package Manager specifies the versions of packages you wanna use and then download them for you in your repository. This also helps maintaining the versions between your collaborators so that everyone stays on the same page. Package Manager takes care of the dependency tree (A tree containing all the dependencies and sub-dependencies)

The most common package manager is npm (Node Package Manager)
##### JavaScript Bundlers
A bundling tool gathers all your dependencies and combines them so that they can be referenced from your HTML file.

### Responsiveness
Basically responding and changing the styles according to the screen the content is being displayed on.
##### Combination of three things:
1. Flexible Grids
2. Fluid Images
3. Media Queries

##### 1. Flexible Grids
##### Gutters:
Spaces between the columns in a grid is called gutter. Not based on pixels but on percentage values.

##### 2. Fluid Images
##### Max-Width: 100%
By setting this rule, the image can become smaller if the container of the image becomes smaller but never grow larger than the container.

##### 3. Media Queries
Depending on the display size, orientation(landscape or portrait), and aspect ratio, conditionally apply styling to the elements.

If the screen is smaller or equal to 700px apply the following rule.
```
@media only screen and (max-width: 700px){
	body{
		background-color: blue;
	}
}
```

##### Breakpoint
A point where the layout changes and adapt to the screen and provide the best style to the user. Basically a point where the style/layout changes.

##### Three types of grids in Responsive Grids
##### 1. Fixed Grids
The size of the columns remain the same and are fixed.
##### 2. Fluid Grids
The size of the columns resize to fill the available space.
##### 3. Hybrid Grids
Containing both fixed and fluid grids

### Bootstrap
A way to build fast responsive sites. It is a library of pre-written code in CSS and JavaScript. Bootstrap comes with multiple components for very fast construction of websites. Another important feature is responsive grids, Bootstrap comes with a pre-made set of CSS rules for building a responsive grid.

##### Important Bootstrap Classes
##### 1. Container 
It is a responsive container
##### 2. Row
##### 3. Col
##### 4. Img-Fluid
The image will resize to the size of the parent container (responsiveness)
##### 5. Table

##### Breakpoints in Bootstrap

Infix is used to indicate the breakpoints.

![Breakpoints in Bootstrap](https://raw.githubusercontent.com/HibbanHaroon/meta-frontend-development-course/main/1.%20Introuction%20to%20Frontend%20Development/Notes/Screenshots/Pasted%20image%2020230921021045.png)

Extra small is the default breakpoint since bootstrap is mobile first.

Example:
```
<div class="container">
	<div class="row">
		<div class="col-12 col-lg-6">
			<h1>Menu</h1>
		</div>
		<div class="col-12 col-lg-6">
			<h1>Prices</h1>
		</div>
	</div>
</div>
```

So now on mobiles both the divs will be stacked as exceeding the columns 12 will result in stacking the two divs for mobile layout as extra small is default. But for lg devices the screen or 12 columns will be divided between the two i.e., 6 columns each.
##### Modifiers in Bootstrap
Adds a CSS class to give visual style to the components.

![Modifiers in Bootstrap](https://raw.githubusercontent.com/HibbanHaroon/meta-frontend-development-course/main/1.%20Introuction%20to%20Frontend%20Development/Notes/Screenshots/Pasted%20image%2020230921021326.png)

##### Alerts 
Alerts in Bootstrap used to show messages on which we requires user's immediate attention. 
##### Primary Alert - Blue Color
##### Danger Alert - Red Color

Example:
```
<div class="container">
	<div class="row">
		<div class="col-lg-6">
			<div class="alert alert-primary" role="alert">
				A message
			</div>
		</div>
	</div>
</div>
```

# Introduction to React

### Static and Dynamic Content

##### Static Content
Static Content is basically the content that is shown to the user as in the form which was uploaded. 
##### Dynamic Content
Dynamic Content on the other hand is the content which is displayed on user's activity. When the HTTP request is made from the browser to the Server, it is then sent to the Application Server. The Application Server then sends the response back to the server which is turned send back to the browser to be displayed on the browser.
##### Application Servers
Application Servers perform more complex login than Web Server. They run application run, communicate with database, etc. 
##### Caching
In order to solve the problem of delays and inability to handle more requests in a given time. Caching is used by web servers. Instead of going to the application server to ask for content on every request. Web Severs has a copy of the dynamic content ready to be displayed on every request - which is called caching. 

So now, on a new request first it is checked whether the web server has the cached copy of the dynamic content, if it doesn't it asks the application server for the content and then the web server caches the content. Upon another request, it checks whether it has the copy of the content, if it has it simply returns it back otherwise it asks the application server for it and caches it for later use. It also updates the cache with the latest content.

### Single Page Applications
Many web developers build SPAs as multi-page applications can be slower and take time to load. SPAs offer speedy and fast web applications which has only one page of content - one HTML page. Instead of asking more pages and the need to download more pages, it simply asks for more content that updates on that one page. 

In SPAs, there are two approaches to serving content:
##### 1. Bundling
When the browser makes a request to the server, all the content is received immediately. The problem occurs when the website is complex, the bundles becomes very large in size and then the site becomes slow.
##### 2. Lazy Loading
However, in Lazy Loading, upon the request the server only returns the minimal HTML, CSS, JavaScript code as needed to load the application. Additional resources are downloaded as required. 

In SPAs, we use templates or json, the server returns json instead of another HTML page like in a traditional website.

### React
A JavaScript library. React is useful as it utilizes components so that you can build apps for your mobile and web(single page applications). 
##### React Components
React component is a small piece of UI. Components are useful because they can be developed and tested in isolation. Another useful feature is reusing components.

##### The Virtual DOM and how does React work?
Each React component corresponds to an HTML element on the page. 
1. When a web browser receives an HTML page, it creates something called the DOM  to represent that page. But updating DOM again and again is slow.
2. Here Virtual DOM comes into play. Virtual DOM is a copy of the browser's DOM but in memory. React uses this virtual DOM to decide when and what to update in the real DOM.
3. When you make changes in your React app (like clicking a button), React updates its virtual DOM first. Then, React compares this new virtual DOM to the previous one to see what's different. 
4. Only the parts of the virtual DOM that have changed are updated in the real DOM. This process of checking and updating only what needs to be changed is called reconciliation.  So, React updates only the components that needs to be updated and not the whole page. 

##### React Fiber Architecture

```
This is the principle of the React Fiber Architecture. React can optimize when and where updates occur to the browser DOM to significantly improve application performance and responsiveness to user input. Think of it as a priority system. The highest priority changes, the elements visible to the user, are updated first. While lower priority changes, the elements not currently displayed, are updated later.

```


