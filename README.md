# Project 0

This project is an assignment for the class Web Programming with Python and JavaScript.

The general layout and verbal contents of this project is adapted from my [Biblical Greek Program](https://biblicalgreekprogram.org) website, though none of the code has come from that site. 

Each page contains a `nav` and a `div.footer` which are identical on each page. Each page also contains a `div.main` in which the unique content of each page is placed.

The footer at the bottom of each page is a call to action and a Bootstrap sign up form that can be used to opt in to receiving future emails.

## index.html

The home page of the website is index.html. This file features a three-item list with custom "bullet points", a table to display the tuition for the classes, and a Boostrap grip layout with three columns for the three class packages.


## resources.html

The resource page contains a Bootstrap grid with columns to display 6 products.

Above the grid layout is a Boostrap alert component that opens a Bootstrap modal that would display a QR code to scan and download the BGP study app. This alert component has the id of "mobile-off". A css selector turns this component off when the site is on a mobile device.

## about.html

The about page contains two Bootstrap grid layout components with two columns each. The list items in the grid have checkbox bullets made with material-icons.

## faq.html

The faq page has a Bootstrap collapse component that contains four frequently asked questions with their answers. There is a Bootstrap submit form near the bottom of the page where custom questions can be asked.

## style.scss

There are several things to point out in the style.scss file. 

1. The @media queries change the margins around each page as the viewport changes, as well as adjusting the vertical spacing between each immediate child `div` inside the `div.main` as the viewport changes.
2. One of the @media queries is used to query if the pointer used in the viewport. If the pointer is "none" and "course" then the device is most likely a mobile device. This is used to style mobile-only / non-mobile elements.
3. The list-style for each `li` is none. The `span` in each `li` has a material-icons icon as the bullet point. In order for this icon to style like a bullet point, the before selector is used with content:"" and a left margin of -2em. This has the affect of placing the icon left of the main `li` body as normal and the first line in the `li` (which is an `h3` tag) to align properly.