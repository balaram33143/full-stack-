<!DOCTYPE html>
<html lang="en">

<head>
    <title>Full Stack Experiment</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        .big-heading {
            font-size: 5rem;
            color: #2c3e50;
            margin: 30px 0;
            text-transform: uppercase;
            text-align: center;
            font-weight: bold;
            text-shadow: 2px 2px 4px rgba(11, 167, 184, 0.3);
            padding-top: 20px;
            background: linear-gradient(to right, #3498db, #96edba);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .list-container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        
        ul {
            list-style-type: none;
            padding: 0;
        }
        
        li {
            background: rgba(255, 255, 255, 0.9);
            margin: 20px 0;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        li:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
        }
        
        h2 {
            color: #2c3e50;
            font-size: 2rem;
            margin-bottom: 20px;
            text-transform: uppercase;
            font-weight: bold;
            border-bottom: 2px solid #008fef;
            padding-bottom: 10px;
            display: inline-block;
        }
        
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 12px 20px;
            margin-right: 10px;
            border-radius: 6px;
            cursor: pointer;
            font-size: 16px;
            transition: all 0.3s ease;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        
        button:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        .home-button {
            background-color: #2ecc71;
        }
        
        table {
            font-family: arial, sans-serif;
            border-collapse: collapse;
            width: 100%;
            margin-top: 20px;
            display: none;
            /* Initially hide the table */
        }
        
        td,
        th {
            border: 1px solid #dddddd;
            text-align: left;
            padding: 8px;
        }
        
        tr:nth-child(even) {
            background-color: #dddddd;
        }
        
        .highlight {
            background-color: #ffeb3b;
        }
        
        .special {
            background-color: #4CAF50;
            color: white;
        }
    </style>
    <script>
        const showTimetable = () =>
            (document.querySelector('table').style.display = 'table');

        const hideTimetableAndReturnHome = () => {
            const timetable = document.querySelector('table');
            timetable.style.display = 'none';
            window.location.href = 'index.html';
        };
    </script>
</head>

<body>
    <header>
        <h1 class="big-heading">FULL STACK EXPERIMENT</h1>
    </header>

    <main>
        <div class="list-container">
            <ul>
                <li>
                    <h2>Wikipedia</h2>
                    <button onclick="window.location.href='https://en.wikipedia.org/wiki/Category:Artificial_intelligence_researchers'">Visit
                        Wikipedia</button>
                    <button class="home-button" onclick="window.location.href='index.html'">Return Home</button>
                </li>

                <li>
                    <h2>Sports</h2>
                    <button onclick="window.location.href='sports.html'">View Sports Details</button>
                    <button class="home-button" onclick="window.location.href='index.html'">Return Home</button>
                </li>

                <li>
                    <h2>Time Table</h2>
                    <button onclick="showTimetable()">View Time Table</button>
                    <table>
                        <tr>
                            <th>Day/Period</th>
                            <th>I<br>10:00-10:10:50</th>
                            <th>II<br>10:50-11:40</th>
                            <th>III<br>11:40-12:30</th>
                            <th>IV <br>12:30-1:20</th>
                            <th>1:20-2:10</th>
                            <th>V<br>2:10-3:00</th>
                            <th>VI<br>3:00-3:50</th>
                            <th>VII<br>4:00-4:50</th>

                        </tr>
                        <tr>
                            <td class="highlight"><b>Monday</b></td>
                            <td colspan="2" class="special">full stack</td>
                            <td>sds</td>
                            <td>pai</td>
                            <td rowspan="6" class="highlight"><b>lunch</b></td>
                            <td colspan="3" class="special">ids</td>
                        </tr>
                        <tr>
                            <td class="highlight"><b>Tuesday</b></td>
                            <td>dlco</td>
                            <td>pai</td>
                            <td colspan="2" class="special">idt</td>
                            <td>ids</td>
                            <td>mefa</td>
                            <td>dlco</td>
                        </tr>
                        <tr>
                            <td class="highlight"><b>Wednesday</b></td>
                            <td colspan="2" class="special">weekly test</td>
                            <td>mefa</td>
                            <td>ids</td>
                            <td>pai</td>
                            <td>dlco</td>
                            <td colspan="2">coun</td>
                        </tr>
                    </table>
                    <button class="home-button" onclick="hideTimetableAndReturnHome()">Return Home</button>
                </li>

                <li>
                    <h2>Registration Form</h2>
                    <button onclick="window.location.href='registration.html'">Go to Registration</button>
                    <button class="home-button" onclick="window.location.href='index.html'">Return Home</button>
                </li>

                <li>
                    <h2>Programming Concepts</h2>
                    <button onclick="window.location.href='programming.html'">Learn Programming</button>
                    <button class="home-button" onclick="window.location.href='index.html'">Return Home</button>
                </li>
            </ul>
        </div>
    </main>

    <script src="script.js"></script>
</body>

</html>
