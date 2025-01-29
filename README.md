<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Language Skills</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #121212;
            color: #fff;
            text-align: center;
            padding: 20px;
        }
        h1 {
            font-size: 28px;
            margin-bottom: 10px;
        }
        .container {
            max-width: 800px;
            margin: auto;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 30px;
        }
        canvas {
            max-width: 100%;
            background: #1e1e1e;
            padding: 15px;
            border-radius: 8px;
        }
        .chart-wrapper {
            width: 100%;
            max-width: 600px;
        }
        .footer {
            margin-top: 40px;
            font-size: 14px;
            opacity: 0.7;
        }
    </style>
</head>
<body>

    <h1>🚀 My Language Skills</h1>
    <p>Here is a visual representation of my programming skills.</p>

    <div class="container">
        <div class="chart-wrapper">
            <h2>📊 Bar Chart</h2>
            <canvas id="barChart"></canvas>
        </div>

        <div class="chart-wrapper">
            <h2>🎯 Doughnut Chart</h2>
            <canvas id="doughnutChart"></canvas>
        </div>
    </div>

    <div class="footer">
        <p>Created by <strong>Faizan</strong> | Hosted on <a href="https://github.com/repostery" target="_blank" style="color: #4db8ff;">GitHub</a></p>
    </div>

    <script>
        // Bar Chart
        const barCtx = document.getElementById('barChart').getContext('2d');
        new Chart(barCtx, {
            type: 'bar',
            data: {
                labels: ['HTML', 'CSS', 'JavaScript', 'Bootstrap', 'React', 'Python'],
                datasets: [{
                    label: 'Skill Level (%)',
                    data: [95, 90, 85, 80, 70, 75], // Adjust skill levels
                    backgroundColor: ['#E44D26', '#1572B6', '#F7DF1E', '#7952B3', '#61DBFB', '#306998'],
                    borderColor: ['#E44D26', '#1572B6', '#F7DF1E', '#7952B3', '#61DBFB', '#306998'],
                    borderWidth: 1
                }]
            },
            options: {
                responsive: true,
                scales: {
                    y: {
                        beginAtZero: true,
                        max: 100
                    }
                },
                animation: {
                    duration: 2000,
                    easing: 'easeOutBounce'
                }
            }
        });

        // Doughnut Chart
        const doughnutCtx = document.getElementById('doughnutChart').getContext('2d');
        new Chart(doughnutCtx, {
            type: 'doughnut',
            data: {
                labels: ['HTML', 'CSS', 'JavaScript', 'Bootstrap', 'React', 'Python'],
                datasets: [{
                    label: 'Skill Level (%)',
                    data: [95, 90, 85, 80, 70, 75],
                    backgroundColor: ['#E44D26', '#1572B6', '#F7DF1E', '#7952B3', '#61DBFB', '#306998'],
                    borderWidth: 1
                }]
            },
            options: {
                responsive: true,
                animation: {
                    duration: 2000,
                    easing: 'easeInOutQuart'
                }
            }
        });
    </script>

</body>
</html>
