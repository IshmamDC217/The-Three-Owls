<script>
    // No specific script logic is necessary for this simple layout
</script>

<style>
    /* Reset default margins and padding */
    html, body {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        width: 100%;
        height: 100%;
    }

    /* Remove any default padding/margin from all elements */
    *, *::before, *::after {
        box-sizing: inherit;
        margin: 0;
        padding: 0;
    }

    /* Remove potential webkit-specific padding/margin */
    body {
        -webkit-margin-before: 0;
        -webkit-margin-after: 0;
        -webkit-margin-start: 0;
        -webkit-margin-end: 0;
        -webkit-padding-start: 0;
        -webkit-padding-end: 0;
    }

    /* Remove any potential scrollbar space on body */
    body {
        overflow-x: hidden;
    }

    /* Ensure the body and html take up the full viewport */
    html, body {
        width: 100%;
        height: 100%;
    }

    /* Now continue with your existing styles */
    nav {
        background-color: transparent;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        z-index: 1000;
        margin-top: 10px;
    }

    div {
        font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
    }

    .navbar-container {
        max-width: 1200px;
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: space-between;
        margin: 0 auto;
        padding: 16px;
    }

    .navbar-logo {
        display: flex;
        align-items: center;
    }

    .navbar-logo img {
        height: 32px;
        margin-right: 8px;
    }

    .navbar-logo span {
        font-size: 1.5rem;
        font-weight: 600;
        color: #d2b677;
    }

    .navbar-toggle {
        display: none;
        padding: 8px;
        width: 40px;
        height: 40px;
        justify-content: center;
        text-align: center;
        color: #6b7280;
    }

    .navbar-toggle:hover {
        background-color: #e5e7eb;
    }

    .navbar-menu {
        display: flex;
        flex-direction: column;
        padding: 16px;
        margin-top: 16px;
        background-color: #f9fafb;
    }

    .navbar-menu.show {
        display: block;
    }

    .navbar-menu ul {
        display: flex;
        flex-direction: column;
        list-style: none;
        padding: 0;
        margin: 0;
    }

    .navbar-menu li {
        margin: 8px 0;
    }

    .navbar-menu li a {
        display: block;
        padding: 8px 12px;
        text-decoration: none;
        border-radius: 4px;
    }

    .navbar-menu li a:hover {
        background-color: #e5e7eb;
    }

    .navbar-menu li a.active {
        background-color: #d2b677;
        color: #ffffff;
    }

    @media (min-width: 768px) {
        .navbar-toggle {
            display: none;
        }

        .navbar-menu {
            flex-direction: row;
            margin-top: 0;
            padding: 0;
            border: none;
            background-color: transparent;
        }

        .navbar-menu ul {
            flex-direction: row;
        }

        .navbar-menu li {
            margin: 0 16px;
        }

        .navbar-menu li a {
            padding: 8px 0;
            color: #ffffff;
        }

        .navbar-menu li a:hover {
            background-color: transparent;
            color: #d2b677;
        }

        .navbar-menu li a.active {
            background-color: transparent;
            color: #d2b677;
        }
    }

    .container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100vh;
        text-align: center;
        padding-top: 80px; /* Ensure content is not hidden under the navbar */
    }
</style>


<nav>
  <div class="navbar-container">
    <div class="navbar-logo">
        <span>Knowledge Nest</span>
    </div>
    <button class="navbar-toggle" aria-controls="navbar-default" aria-expanded="false">
        <span class="sr-only">Open main menu</span>
        <svg width="20" height="20" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
        </svg>
    </button>
    <div class="navbar-menu" id="navbar-default">
      <ul>
        <li><a href="#" class="active">Home</a></li>
        <li><a href="#">Github</a></li>
        <li><a href="#">My Website</a></li>
      </ul>
    </div>
  </div>
</nav>

<slot></slot>
