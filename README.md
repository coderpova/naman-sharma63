# naman-sharma63
this is my 20th repository
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spotify Style UI</title>
    <style>
        :root {
            --spot-black: #121212;
            --spot-dark-grey: #181818;
            --spot-light-grey: #282828;
            --spot-green: #1DB954;
            --spot-white: #FFFFFF;
            --spot-text-muted: #B3B3B3;
        }

        body {
            font-family: 'Circular', 'Helvetica Neue', Helvetica, Arial, sans-serif;
            background-color: #000;
            color: var(--spot-white);
            margin: 0;
            display: flex;
            height: 100vh;
        }

        /* Side Navigation */
        .sidebar {
            width: 240px;
            background-color: #000;
            padding: 24px 12px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .nav-link {
            color: var(--spot-text-muted);
            text-decoration: none;
            font-weight: bold;
            font-size: 14px;
            display: flex;
            align-items: center;
            gap: 15px;
            transition: color 0.2s;
        }

        .nav-link:hover, .nav-link.active { color: #fff; }

        /* Main View */
        .main-view {
            flex: 1;
            background: linear-gradient(to bottom, #222, var(--spot-black) 40%);
            overflow-y: auto;
            border-radius: 8px;
            margin: 8px 8px 80px 0;
            padding: 20px 30px;
        }

        .header { font-size: 24px; font-weight: bold; margin-bottom: 20px; }

        /* Content Grid */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 24px;
        }

        .card {
            background-color: var(--spot-dark-grey);
            padding: 16px;
            border-radius: 8px;
            transition: background-color 0.3s;
            cursor: pointer;
            position: relative;
        }

        .card:hover { background-color: var(--spot-light-grey); }

        .card-img {
            width: 100%;
            aspect-ratio: 1/1;
            background-color: #333;
            border-radius: 4px;
            margin-bottom: 16px;
            box-shadow: 0 8px 24px rgba(0,0,0,0.5);
            overflow: hidden;
        }

        .card-img iframe { width: 100%; height: 100%; border: none; }

        .card-title { font-size: 16px; font-weight: bold; margin-bottom: 8px; }
        .card-desc { font-size: 14px; color: var(--spot-text-muted); line-height: 1.4; }

        /* Play Button Overlay */
        .play-btn {
            position: absolute;
            bottom: 85px;
            right: 25px;
            width: 48px;
            height: 48px;
            background-color: var(--spot-green);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transform: translateY(10px);
            transition: all 0.3s;
            box-shadow: 0 8px 16px rgba(0,0,0,0.3);
        }

        .card:hover .play-btn { opacity: 1; transform: translateY(0); }

    </style>
</head>
<body>

    <nav class="sidebar">
        <div style="font-size: 24px; font-weight: bold; margin-bottom: 10px; padding-left: 12px;">Spotify</div>
        <a href="#" class="nav-link active"><span>🏠</span> Home</a>
        <a href="#" class="nav-link"><span>🔍</span> Search</a>
        <a href="#" class="nav-link"><span>📚</span> Your Library</a>
    </nav>

    <main class="main-view">
        <div class="header">Made For You</div>
        
        <div class="grid">
            <div class="card">
                <div class="card-img">
                    <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ?controls=0" title="Video"></iframe>
                </div>
                <div class="play-btn">▶</div>
                <div class="card-title">Daily Mix 1</div>
                <div class="card-desc">The perfect beats for your C++ coding sessions.</div>
            </div>

            <div class="card">
                <div class="card-img">
                    <iframe src="https://www.youtube.com/embed/377pxMNUTwo?controls=0" title="Video"></iframe>
                </div>
                <div class="play-btn">▶</div>
                <div class="card-title">SSB Prep Radio</div>
                <div class="card-desc">Stay focused for your Bangalore trip.</div>
            </div>
        </div>
    </main>

</body>
</html>
