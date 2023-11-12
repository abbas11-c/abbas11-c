<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Restaurant Menu</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: url('bck1.jpg') no-repeat center center fixed;
            background-size: cover;
            color: white; /* Font color for general text */
        }

        header {
            background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent black background for header */
            color: white;
            text-align: center;
            padding: 10px;
        }

        nav {
            display: flex;
            justify-content: space-around;
            background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent black background for navigation */
            padding: 10px;
        }

        section {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin: 20px;
            display: none; /* Hide sections by default */
            background: rgba(255, 255, 255, 0.8); /* Semi-transparent white background for sections */
            padding: 20px;
            border-radius: 10px;
            max-width: 80%; /* Adjust the maximum width of the sections */
            margin: 0 auto; /* Center the sections */
        }

        h2 {
            color: red; /* Red font color for category names */
            cursor: pointer; /* Add cursor pointer for clickable effect */
        }

        ul {
            list-style: none;
            padding: 0;
        }

        li {
            margin-bottom: 10px;
            color: blue; /* Blue font color for item names */
        }

        img {
            max-width: 100px; /* Set the maximum width of the images */
            height: auto;
            border-radius: 5px; /* Optional: Add border-radius for rounded corners */
            margin-right: 10px; /* Optional: Add margin to separate the image from text */
        }
    </style>
</head>

<body>

    <header>
        <img src="logo1.png" alt="Restaurant Logo" style="max-width: 100px;">
        <h1>Your Restaurant Name</h1>
    </header>

    <nav>
        <h2 onclick="toggleSection('eat')">Eat</h2>
        <h2 onclick="toggleSection('drink')">Drink</h2>
    </nav>

    <section id="eat">
        <h2>Eat</h2>
        <ul>
            <li>
                <h3>Burgers</h3>
                <ul>
                    <li>
                        <img src="hq720.jpg" alt="Original Burger">
                        Original Burger - 3000 CFA
                    </li>
                    <li>
                        <img src="The-Best-Classic-Hamburgers-550.jpg" alt="Lebanese Burger">
                        Lebanese Burger - 5000 CFA
                    </li>
                </ul>
            </li>
            <!-- Add other Eat categories and items here -->
            <li>
                <h3>shawarma</h3>
                <ul>
                    <li>
                        <img src="hq720.jpg" alt="Original Burger">
                        Original chicken - 2000 CFA
                    </li>
                    <li>
                        <img src="The-Best-Classic-Hamburgers-550.jpg" alt="Lebanese Burger">
                        original beef - 5000 CFA
                    </li>
                </ul>
            </li>
            <!-- Add other Eat categories and items here -->
        </ul>
    </section>

    <section id="drink">
        <h2>Drink</h2>
        <ul>
            <li>
                <h3>Hot</h3>
                <!-- Add Hot drink items here -->
            </li>
            <li>
                <h3>Soft</h3>
                <!-- Add Soft drink items here -->
            </li>
        </ul>
    </section>

    <script>
        function toggleSection(sectionId) {
            var sections = document.querySelectorAll('section');
            sections.forEach(function (section) {
                if (section.id === sectionId) {
                    section.style.display = (section.style.display === 'none') ? 'flex' : 'none';
                } else {
                    section.style.display = 'none';
                }
            });
        }
    </script>

</body>

</html>
