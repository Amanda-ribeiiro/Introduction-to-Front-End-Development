# Working with Bootstrap components

## Instructions

### Introduction

In this exercise, you will practice adding Bootstrap components to a webpage.

### Goal

Update the Little Lemon website to use Bootstrap Components.

### Objectives

- Add a Badge component to the page to notify customers of the new falafel dish.
- Add an Alert component to the page to notify customers that the restaurant will be closed on New Year's Day.
- Add a Button component to the page with the text Order Online.

### Step-by-step Instructions

Step 1: Open `index.html`

Step 2: Add another `div` element below the `Our Menu` `text-center` `div` element.

Step 3: Add a `class` attribute to the element with the value `alert alert-info`.

Step 4: Add a `role` attribute to the element with the value `alert`.

Step 5: Add the message Our restaurant will be closed on New Year's Day, inside the `div` element.

```html
<div class="row">
    <div class="col-12">
        <div class="text-center">
            <h1>Our Menu</h1>
        </div>
        <div class="alert alert-info" role="alert">
            Our restaurant will be closed on New Year's Day
        </div>
    </div>
</div>
````

Step 6: Add a `span` element inside the Falafel h2 element, before the closing h2 tag.

Step 7: Add a `class` attribute to the span element, with the value `badge bg-secondary`.

```html
<h2>Falafel <span class="badge bg-secondary">New</span></h2>
````

Step 8: Add another `div` element after the last row element.

Step 9: Add a `class` attribute with the value `row` to the div element.

Step 10: Add a div element inside the `row` `div` element.

Step 11: Add a `class` attribute with the value col-12 to the div element.

Step 12: Add another `div` element inside the col-12 div element.

Step 13: Add a `class` attribute with the value `text-center` to the div element.

Step 14: Add a `button` element inside the text-center div element.

Step 15: Add a `type` attribute with the value `button`.

Step 16: Add a `class` attribute with the value `btn btn-primary`.

Step 17: Add the text `Order Online` inside the button element.

````html
<div class="row">
    <div class="col-12">
        <div class="text-center">
            <button type="button" class="btn btn-primary">Order Online</button>
        </div>
    </div>
</div>
````

Step 18: Save the file.

Step 19: Click on 'Go live', which is at the bottom right of your editor.

> Once the server is up and running you'll see the exposed port.

Step 20: Now click on browser preview.

> Enter the url as `http://localhost:<exposed port>`

Step 21: Verify that the alert is displayed on the web page.

Step 22: Verify at the **new** badge is displayed on the Falafel header.

Step 23: Verify that the Order Online button is displayed.

Step 24: Make sure to close the server by clicking on exposed Port number (e.g. 5500) after completing the lab.

> You should see a notification like this which confirms the server has been stopped.

#### Tips

- Make sure to add your columns to row elements.
- Remember that Bootstrap uses a 12 column grid system
- There are plenty of examples in the Bootstrap documentation.
- Review the lessons Using Bootstrap Styles and Bootstrap Components.
