# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with Flexbox & Grid</title>
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: #333;
            background-color: #f4f4f4;
        }
        
        /* Navigation Bar - Flexbox */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: #333;
            color: white;
            padding: 1rem 2rem;
        }
        
        .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 1.5rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: #4CAF50;
        }
        
        /* Main Content Layout - Grid */
        .container {
            display: grid;
            grid-template-columns: 1fr;
            gap: 1.5rem;
            padding: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .card {
            background: white;
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .card h2 {
            margin-bottom: 1rem;
            color: #4CAF50;
        }
        
        /* Footer - Flexbox */
        footer {
            background-color: #333;
            color: white;
            padding: 1.5rem;
            text-align: center;
            margin-top: 2rem;
        }
        
        /* Media Queries for Responsiveness */
        
        /* Tablet View */
        @media (min-width: 768px) {
            .container {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .navbar {
                padding: 1rem 3rem;
            }
        }
        
        /* Desktop View */
        @media (min-width: 1024px) {
            .container {
                grid-template-columns: repeat(3, 1fr);
            }
            
            .hero {
                grid-column: span 3;
                text-align: center;
                padding: 3rem;
                background: #4CAF50;
                color: white;
            }
            
            .hero h1 {
                font-size: 2.5rem;
                margin-bottom: 1rem;
            }
        }
        
        /* Mobile View Adjustments */
        @media (max-width: 600px) {
            .navbar {
                flex-direction: column;
                padding: 1rem;
            }
            
            .nav-links {
                margin-top: 1rem;
                flex-direction: column;
                align-items: center;
            }
            
            .nav-links li {
                margin: 0.5rem 0;
            }
            
            .container {
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation Bar -->
    <nav class="navbar">
        <div class="logo">FlexGrid</div>
        <ul class="nav-links">
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>
    
    <!-- Main Content -->
    <div class="container">
        <div class="card hero">
            <h1>Welcome to My Website</h1>
            <p>Discover the power of responsive design with Flexbox and Grid</p>
        </div>
        
        <div class="card">
            <h2>Flexbox</h2>
            <p>Flexbox is a one-dimensional layout method for arranging items in rows or columns. Items flex to fill additional space or shrink to fit into smaller spaces.</p>
        </div>
        
        <div class="card">
            <h2>CSS Grid</h2>
            <p>CSS Grid Layout is a two-dimensional system, meaning it can handle both columns and rows, unlike flexbox which is largely a one-dimensional system.</p>
        </div>
        
        <div class="card">
            <h2>Responsive Design</h2>
            <p>Responsive web design makes your web page look good on all devices. It uses only HTML and CSS to automatically resize, hide, shrink, or enlarge elements.</p>
        </div>
        
        <div class="card">
            <h2>Media Queries</h2>
            <p>Media queries allow you to apply CSS styles depending on a device's general type or specific characteristics like screen resolution or browser viewport width.</p>
        </div>
        
        <div class="card">
            <h2>Modern Layouts</h2>
            <p>Combining Flexbox and Grid gives you the power to create complex, responsive layouts that were difficult to achieve with older CSS methods.</p>
        </div>
    </div>
    
    <!-- Footer -->
    <footer>
        <p>&copy; 2025 Responsive Layout Demo. All rights reserved.</p>
    </footer>
</body>
</html>
