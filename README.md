<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Yono Game Zone</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
        }

        body {
            background-color: #f7f7f7;
            color: #333;
            -webkit-text-size-adjust: 100%;
        }

        .header {
            background-color: #009640;
            color: white;
            padding: 8px 12px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-logo {
            display: flex;
            align-items: center;
            gap: 5px;
            font-weight: bold;
            font-size: 16px;
        }

        .header-logo img {
            width: 20px;
            height: 20px;
        }

        .search-container {
            flex-grow: 1;
            margin: 0 15px;
            max-width: 250px;
            position: relative;
        }

        .search-box {
            width: 100%;
            padding: 6px 12px;
            border: 1px solid rgba(255,255,255,0.4);
            border-radius: 4px;
            background-color: rgba(255,255,255,0.2);
            color: white;
            font-size: 14px;
            outline: none;
        }

        .search-box::placeholder {
            color: rgba(255,255,255,0.7);
        }

        .header-menu {
            font-size: 20px;
            cursor: pointer;
        }

        .content-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
            padding: 10px;
        }

        .section-header {
            grid-column: 1 / -1;
            font-size: 16px;
            font-weight: bold;
            color: #009640;
            padding: 5px 0;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .game-card {
            background-color: white;
            border: 1px solid #eaeaea;
            border-radius: 8px;
            overflow: hidden;
            text-align: center;
            text-decoration: none;
            color: inherit;
            display: flex;
            flex-direction: column;
            position: relative;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
            transition: transform 0.2s;
        }

        .game-card:active {
            transform: scale(0.98);
        }

        .rank-badge {
            position: absolute;
            top: 6px;
            left: 6px;
            background-color: rgba(0,0,0,0.8);
            color: white;
            font-size: 10px;
            font-weight: bold;
            padding: 2px 6px;
            border-radius: 4px;
            z-index: 10;
        }

        .card-image-container {
            padding: 20px 20px 10px 20px;
        }

        .game-card img.game-icon {
            width: 100%;
            aspect-ratio: 1/1;
            object-fit: cover;
            border-radius: 50%;
            display: block;
        }

        .card-details {
            padding: 0 10px 10px 10px;
            display: flex;
            flex-direction: column;
            gap: 2px;
            flex-grow: 1;
        }

        .rating-row {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 3px;
            color: #ff9f00;
            font-size: 12px;
            font-weight: bold;
        }

        .game-title {
            font-size: 13px;
            font-weight: bold;
            color: #222;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .card-action-btn {
            background-color: #1e88e5;
            color: white;
            font-size: 12px;
            font-weight: bold;
            padding: 8px;
            border-radius: 4px;
            border: none;
            cursor: pointer;
            margin-top: auto;
            text-align: center;
            width: 100%;
            display: inline-block;
            transition: background-color 0.2s;
        }

        .card-action-btn:hover {
            background-color: #1565c0;
        }
    </style>
</head>
<body>

    <header class="header">
        <div class="header-logo">
            <img src="https://img.icons8.com/material-rounded/24/ffffff/dice.png" alt="Dice Icon">
            <span>Yono Game Zone</span>
        </div>
        <div class="search-container">
            <input type="text" id="gameSearch" class="search-box" placeholder="Search..." onkeyup="searchGames()">
        </div>
        <div class="header-menu">☰</div>
    </header>

    <main class="content-container">
        
        <h2 class="section-header" id="topHeader">🏆 Top 3 Games</h2>
        
        <a href="https://dp92t0mhjbqu9.cloudfront.net/yonorummyagent.apk" class="game-card top-game-item">
            <span class="rank-badge">1</span>
            <div class="card-image-container">
                <img src="https://kommodo.ai/i/7S8lx5PODYclMxvtgyJg/raw" class="game-icon" alt="Yono Rummy">
            </div>
            <div class="card-details">
                <div class="rating-row">
                    <span>⭐</span>
                    <span>9.9</span>
                </div>
                <p class="game-title">Yono Rummy</p>
                <span class="card
