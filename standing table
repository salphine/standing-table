<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Salphine Premier League Standings Table</title>
    <script src="https://d3js.org/d3.v7.min.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f8f9fa;
            text-align: center;
            padding: 20px;
        }
        table {
            width: 80%;
            margin: auto;
            border-collapse: collapse;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
            background-color: white;
        }
        th, td {
            padding: 12px;
            text-align: center;
            border: 1px solid #ddd;
        }
        th {
            background-color: #343a40;
            color: white;
            text-transform: uppercase;
        }
        tr:nth-child(even) {
            background-color: #f2f2f2;
        }
        tr:hover {
            background-color: #ffeb3b;
            transition: 0.3s;
        }
    </style>
</head>
<body>

    <h1>Premier League Standings</h1>
    <div id="standings"></div>

    <script>
        // Sample EPL standings data (replace with live API data)
        const standingsData = [
            { position: 1, team: "Arsenal", played: 24, won: 14, drawn: 8, lost: 2, gf: 49, ga: 22, gd: 27, points: 50 },
            { position: 2, team: "Liverpool", played: 23, won: 17, drawn: 5, lost: 1, gf: 56, ga: 21, gd: 35, points: 56 },
            { position: 3, team: "Man City", played: 23, won: 16, drawn: 4, lost: 3, gf: 55, ga: 23, gd: 32, points: 52 },
            { position: 4, team: "Chelsea", played: 24, won: 13, drawn: 6, lost: 5, gf: 47, ga: 29, gd: 18, points: 45 },
            { position: 5, team: "Man United", played: 23, won: 12, drawn: 6, lost: 5, gf: 42, ga: 27, gd: 15, points: 42 }
        ];

        // Define column headers
        const columns = ["Position", "Team", "Played", "Won", "Drawn", "Lost", "GF", "GA", "GD", "Points"];

        // Select table container
        const table = d3.select("#standings").append("table");
        const thead = table.append("thead");
        const tbody = table.append("tbody");

        // Append table header
        thead.append("tr")
            .selectAll("th")
            .data(columns)
            .enter()
            .append("th")
            .text(d => d);

        // Append table rows
        const rows = tbody.selectAll("tr")
            .data(standingsData)
            .enter()
            .append("tr");

        // Append table cells
        rows.selectAll("td")
            .data(row => [
                row.position, row.team, row.played, row.won, row.drawn, 
                row.lost, row.gf, row.ga, row.gd, row.points
            ])
            .enter()
            .append("td")
            .text(d => d);
    </script>

</body>
</html>
