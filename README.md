# The Last Day - Zombie Survival Adventure

A "Choose Your Own Adventure" style interactive narrative game built with pure HTML for the Web Systems and Technologies course at Universidad del Valle de Guatemala.

## About the Project

This is an interactive zombie apocalypse survival story where your choices determine your fate. Navigate through a post-apocalyptic city, make critical decisions, and try to reach one of three possible endings:

- **Good Ending**: Help researchers find a cure and save humanity
- **Neutral Ending**: Survive day by day in a safe zone
- **Bad Ending**: Make fatal mistakes and face the consequences

## How to Play

### Online (via NGINX)

1. Navigate to `http://localhost/adventure/` in your web browser
2. Start from `index.html` in the `start/` folder
3. Make choices by clicking on the hyperlinks
4. Each decision leads to a different path
5. Reach one of three endings based on your choices

### Local Testing (File System)

1. Clone this repository
2. Open `start/index.html` in your web browser
3. Navigate through the story by clicking links

**Note**: Some relative paths work better when served through a web server (NGINX) rather than directly from the file system.

## Project Structure
```
zombie-adventure/
├── start/              # Beginning of the story
│   └── index.html      # Entry point
├── paths/              # Major decision paths
│   ├── path1.html      # Roof path
│   └── path2.html      # Basement path
├── extras/             # Story development
│   ├── event1.html     # Helicopter escape
│   ├── event2.html     # Supply gathering
│   ├── twist1.html     # Panic room
│   ├── twist2.html     # Weapons
│   └── discovery.html  # The truth about the infection
├── endings/            # Three possible conclusions
│   ├── good.html       # Hope for humanity
│   ├── neutral.html    # Survival mode
│   └── bad.html        # Fatal mistakes
├── .gitignore
└── README.md
```

## Technical Details

**Technologies Used:**
- Pure HTML5 (no CSS or JavaScript as per project requirements)
- Semantic HTML tags: `<header>`, `<footer>`, `<body>`, `<head>`
- Text formatting: `<h1>`, `<h2>`, `<p>`, `<b>`, `<strong>`, `<small>`
- Navigation: `<a>` tags for hyperlinks
- Images: `<img>` tags with Unsplash CDN

**Requirements Met:**
- 11 HTML files total
- Entry point named `index.html`
- Each page has at least 2 decision links
- Three distinct endings (good, neutral, bad)
- All HTML files organized in folders (no HTML in root)
- Each file includes: header, body, footer, title, paragraph, image, and various text styles

## Deployment with NGINX

### Prerequisites
- NGINX installed and running
- WSL (Windows Subsystem for Linux) with Debian or Ubuntu, OR
- A Unix-based terminal (Linux/macOS)

### Deployment Steps

1. **Create the web directory:**
```bash
sudo mkdir -p /var/www/html/adventure
```

2. **Copy project files:**
```bash
sudo cp -r ~/zombie-adventure/* /var/www/html/adventure/
```

3. **Set proper permissions:**
```bash
sudo chmod -R 755 /var/www/html/adventure
```

4. **Access the game:**
Open your browser and navigate to:
- `http://localhost/adventure/start/index.html` or
- `http://localhost:PORT/adventure/start/index.html` (if using a custom port)

### Troubleshooting

**Issue**: "403 Forbidden" error
- **Solution**: Check file permissions with `ls -la /var/www/html/adventure`

**Issue**: "404 Not Found" error
- **Solution**: Verify files were copied correctly and NGINX is running: `sudo systemctl status nginx`

**Issue**: Links not working
- **Solution**: Ensure you're accessing via NGINX (http://localhost) and not directly opening files

## Game Flow
```
START
├─> ROOF
│   ├─> Helicopter
│   │   └─> Research Facility → Discovery → Good/Neutral
│   └─> Supplies → Flare/Escape → Neutral/Bad
└─> BASEMENT
    ├─> Hide → Wait/Signal → Neutral/Bad
    └─> Weapons → Search/Drive → Good/Neutral
```


## RICING - Reddit Matrix Theme

### Before:
![Reddit Before](screenshots/reddit-before.png)

### After:
![Reddit After](screenshots/reddit-after.png)


## STYLING MY GAME

### Before:
![Game Before](screenshots/game-before.png)

### After:
![Game After1](screenshots/game-after1.png)
![Game After2](screenshots/game-after2.png)

## Story Features

- **Multiple Paths**: 11 unique HTML pages with different scenarios
- **Meaningful Choices**: Every decision impacts your journey
- **Plot Twist**: Discover the shocking truth about the infection
- **Replayability**: Multiple routes lead to different endings
- **Atmospheric**: Images and narrative create immersive experience

## Credits

**Developer**: Angel Armas  
**Course**: Sistemas y Tecnologías Web  
**Institution**: Universidad del Valle de Guatemala  
**Semester**: 1, 2026  
**Instructor**: Marlon Fuentes

**Image Credits**: All images sourced from [Unsplash](https://unsplash.com) (free stock photos)


