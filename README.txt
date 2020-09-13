l12-hw05
* Status: In Progress
* CodePen: <https://codepen.io/chindraba-ga/pen/eYZrOJv>
* Live page: <https://www.chindraba.work/fewd/l12-hw05.html>

Contents
================================================================================

* Description
* Copyright and License
  * The MIT License

Description
================================================================================

Lesson 12: Assignment: Rebuild a Navbar from Slack

We're giving you the layout of the page with the header already in there. Your
job is to get the menus working, both for desktop and for mobile. You will have
to use responsive design, the position property, and build the menus in the
HTML. All the other HTML, baseline CSS and SVG icons are being provided.

The starter code is:

- HTML

    <!doctype html>
    <html class="no-js" lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="x-ua-compatible" content="ie=edge">
            <title>Slack header / navigation</title>
            <meta name="description" content="Slack exercise">
            <meta name="viewport" content="width=device-width, initial-scale=1">

            <link rel="manifest" href="site.webmanifest">
            <link rel="apple-touch-icon" href="icon.png">
            <!-- Place favicon.ico in the root directory -->

            <link href="https://fonts.googleapis.com/css?family=Lato" rel="stylesheet">

        </head>
        <body>

          <!-- Top nav -->
          <header class="global-header" id="top-nav">
            <section class="nav-left">
              <div class="logo">
                <svg xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 240 60"
                    shape-rendering="geometricPrecision"
                    width="100"
                    height="25"
                    aria-label="Slack"
                    class="c-slacklogo--white svg-replaced">
                    <path d="M75.663 47.477l2.929-6.846c3.207 2.375 7.39 3.632 11.574 3.632 3.068 0 5.02-1.187 5.02-3.003-.07-5.03-18.477-1.118-18.617-13.764-.07-6.427 5.648-11.387 13.737-11.387 4.81 0 9.622 1.188 13.038 3.913l-2.737 6.992c-3.143-2.021-7.025-3.43-10.72-3.43-2.51 0-4.184 1.187-4.184 2.725.07 4.96 18.618 2.235 18.827 14.322 0 6.567-5.579 11.178-13.528 11.178-5.856 0-11.225-1.397-15.34-4.332m116.629-9.325a8.498 8.498 0 0 1-7.405 4.33c-4.698 0-8.506-3.816-8.506-8.523s3.808-8.523 8.506-8.523a8.498 8.498 0 0 1 7.405 4.33l8.143-4.52c-3.05-5.451-8.868-9.137-15.548-9.137-9.839 0-17.815 7.991-17.815 17.85 0 9.858 7.976 17.85 17.815 17.85 6.68 0 12.498-3.686 15.548-9.137l-8.143-4.52M109.814 51.11h10.18V1.25h-10.179zm95.761-49.86v49.86h10.18V36.172l12.063 14.938h13.012l-15.34-17.746 14.224-16.559H227.26l-11.505 13.767V1.25h-10.18M151.357 16.807v4.053c-1.673-2.795-5.787-4.751-10.11-4.751-8.925 0-15.967 7.895-15.967 17.815 0 9.92 7.042 17.885 15.967 17.885 4.323 0 8.437-1.956 10.11-4.751v4.052h10.18V16.807h-10.18zm0 21.414c-1.464 2.445-4.532 4.26-7.948 4.26-4.699 0-8.507-3.815-8.507-8.522 0-4.707 3.808-8.523 8.507-8.523 3.416 0 6.484 1.886 7.948 4.4v8.385z"></path>
                    <path d="M21.902.148c-3.299 0-5.973 2.68-5.973 5.985a5.979 5.979 0 0 0 5.973 5.985h5.974V6.133A5.98 5.98 0 0 0 21.902.148m0 15.96H5.973C2.674 16.108 0 18.788 0 22.094c0 3.305 2.674 5.985 5.973 5.985h15.93c3.298 0 5.973-2.68 5.973-5.985 0-3.306-2.675-5.986-5.974-5.986" fill="#36C5F0"></path>
                    <path d="M59.734 22.094c0-3.306-2.675-5.986-5.974-5.986-3.299 0-5.973 2.68-5.973 5.986v5.985h5.973a5.98 5.98 0 0 0 5.974-5.985M43.805 22.094V6.133A5.98 5.98 0 0 0 37.831.148c-3.299 0-5.973 2.68-5.973 5.985v15.96c0 3.307 2.674 5.987 5.973 5.987a5.98 5.98 0 0 0 5.974-5.985" fill="#2EB67D"></path><path d="M37.831 60a5.98 5.98 0 0 0 5.974-5.985 5.98 5.98 0 0 0-5.974-5.985h-5.973v5.985c0 3.305 2.674 5.985 5.973 5.985M37.831 44.04h15.93c3.298 0 5.973-2.68 5.973-5.986a5.98 5.98 0 0 0-5.974-5.985H37.831c-3.299 0-5.973 2.68-5.973 5.985a5.979 5.979 0 0 0 5.973 5.985" fill="#ECB22E"></path>
                    <g>
                      <path d="M0 38.054a5.979 5.979 0 0 0 5.973 5.985 5.98 5.98 0 0 0 5.974-5.985v-5.985H5.973C2.674 32.069 0 34.749 0 38.054m15.929 0v15.96c0 3.306 2.674 5.986 5.973 5.986a5.98 5.98 0 0 0 5.974-5.985V38.054a5.979 5.979 0 0 0-5.974-5.985c-3.299 0-5.973 2.68-5.973 5.985" fill="#E01E5A"></path>
                    </g>
                </svg>
              </div>
              <ul class="nav">
                <li id="menu-1-button">Why Slack?</li>
                <li id="menu-2-button">Solutions</li>
                <li id="menu-3-button">Resources</li>
                <li>Pricing</li>
              </ul>
            </section>
            <div class="nav-right">
              <p class="workspaces">Your Workspaces</p>
              <div class="hamburger-menu" id="menu-trigger">
                <img src="img/hamburger.svg" alt="Hamburger icon">
              </div>
            </div>
          </header>

          <!--Main content-->
          <section class="placeholder"></section>

          <!--Side menu goes here-->
          <!--You'll need these assets-->
          <!-- 'X Icon': https://s3-us-west-2.amazonaws.com/s.cdpn.io/2522641/x.svg -->
          <!-- 'Hamburger Icon': https://s3-us-west-2.amazonaws.com/s.cdpn.io/2522641/hamburger.svg -->
          <!--

          <!--Dropdown Menus also go here, but why? They are absolutely positioned, so it doesnt matter where they are in the DOM if you remember.... -->
        </body>
    </html>

- CSS

    /* ==========================================================================
       Author's custom styles
       ========================================================================== */

    body {
      font-family: 'Lato', sans-serif; /* Lato font was a close match */
      color: #454545;
    }

    .placeholder {
      background: lightslategray;
      height: 100vh;
    }

    /**
      * Notice how you have to put a width on fixed elements
      * They aren't by default width: 100% when they are block level elements
      */
    .global-header {
      background-color: white;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      height: 40px;
      padding: 15px 25px;
      width: calc(100% - 50px);
    }

    /**
     * =============
     * NAV
     * =============
     * Notice how I want the items to be flex-start, so I don't put anything
     * Remember, by default, flex gives us justify-content: flex-start
     */
    .nav-left {
      align-items: center;
      display: flex;
    }

    /**
     * I've got the SVG inside a flex container, so I align it into the middle
     */
    .logo {
      display: flex;
      align-items: center;
    }

    .logo svg {
      width: 150px; /* Gives logo enough room to breathe */
    }

    .nav {
      display: none;
      flex-direction: row;
      align-items: center;
      margin: 0;
      padding-left: 0;
    }

    @media (min-width: 1085px) {
      .nav {
        display: flex;
      }
    }

    ul {
      list-style: none;
    }

    .nav li {
      font-size: 14px;
      margin: 0 20px;
      cursor: pointer;
    }

    .nav-right {
      align-items: center;
      display: flex;
      justify-content: flex-end;
      margin-right: 45px;
    }


    /* Dropdown menus */
    /* Sidebar menu */
    /* This is the background Slack is using: https://s3-us-west-2.amazonaws.com/s.cdpn.io/2522641/sidebar-background.png */


    /* ==========================================================================
       Helper classes
       ========================================================================== */

    /*
     * Hide visually and from screen readers
     */

    .hidden {
        display: none !important;
    }

    /*
     * Hide only visually, but have it available for screen readers:
     * https://snook.ca/archives/html_and_css/hiding-content-for-accessibility
     *
     * 1. For long content, line feeds are not interpreted as spaces and small width
     *    causes content to wrap 1 word per line:
     *    https://medium.com/@jessebeach/beware-smushed-off-screen-accessible-text-5952a4c2cbfe
     */

    .visuallyhidden {
        border: 0;
        clip: rect(0 0 0 0);
        -webkit-clip-path: inset(50%);
        clip-path: inset(50%);
        height: 1px;
        margin: -1px;
        overflow: hidden;
        padding: 0;
        position: absolute;
        width: 1px;
        white-space: nowrap; /* 1 */
    }

    /*
     * Extends the .visuallyhidden class to allow the element
     * to be focusable when navigated to via the keyboard:
     * https://www.drupal.org/node/897638
     */

    .visuallyhidden.focusable:active,
    .visuallyhidden.focusable:focus {
        clip: auto;
        -webkit-clip-path: none;
        clip-path: none;
        height: auto;
        margin: 0;
        overflow: visible;
        position: static;
        width: auto;
        white-space: inherit;
    }

    /*
     * Hide visually and from screen readers, but maintain layout
     */

    .invisible {
        visibility: hidden;
    }


Copyright and License
================================================================================

The MIT license applies to all the code within this repository.

Copyright © 2020  Chindraba (Ronald Lamoreaux)
            <upskill@chindraba.work>
- All Rights Reserved

The MIT License

Permission is hereby granted, free of charge, to any person obtaining a
copy of this software and associated documentation files (the "Software"),
to deal in the Software without restriction, including without limitation
the rights to use, copy, modify, merge, publish, distribute, sublicense,
and/or sell copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included
in all copies or substantial portions of the Software

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGE MENT. IN NO EVENT SHALL
THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
DEALINGS IN THE SOFTWARE.
