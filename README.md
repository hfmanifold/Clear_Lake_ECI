# Clear Lake Monitoring

This project monitors Clear Lake Monitoring using Campbell Scientific data loggers.

## Setup Complete! ✓

Your project structure is ready. Follow these steps:

### 1. Edit Config File
Open and customize:
```
C:/Users/ECI_LLC/Desktop/Live Data/configs/clearlake_config.yaml
```

Update:
- Site names
- Data file names (CSV filenames from Campbell logger)
- Parameter names (column names in your CSV)
- Parameter display names and units

### 2. Create GitHub Repository

1. Go to https://github.com/
2. Create new repository
3. Make it PUBLIC
4. Copy the URL
5. Update in your config file

### 3. Initialize Git Repository

```batch
cd "C:/Users/ECI_LLC/Desktop/Live Data/projects/ClearLake/repo"
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin YOUR_GITHUB_URL
git push -u origin main
```

### 4. Test Sync Script

```batch
cd "C:/Users/ECI_LLC/Desktop/Live Data"
C:/Users/ECI_LLC/Desktop/Live Data/sync_clearlake.bat
```

### 5. Create Symbolic Link for Shiny App

Run Command Prompt as Administrator:
```batch
cd "C:/Users/ECI_LLC/Desktop/Live Data/shiny_apps/clearlake"
mklink clearlake_config.yaml "..\..\configs\clearlake_config.yaml"
```

### 6. Test Shiny App Locally

```r
setwd("C:/Users/ECI_LLC/Desktop/Live Data/shiny_apps/clearlake")
shiny::runApp()
```

### 7. Deploy to shinyapps.io

```r
setwd("C:/Users/ECI_LLC/Desktop/Live Data/shiny_apps/clearlake")
source("deploy_clearlake.R")
```

### 8. Set Up Task Scheduler

1. Open Task Scheduler
2. Export Blue River task as XML
3. Edit XML - replace "blue_river" with "clearlake"
4. Import back into Task Scheduler

## File Structure

```
ClearLake/
├── repo/
│   ├── data/          # CSV files from Campbell logger
│   ├── metadata/      # Auto-generated stats
│   ├── logs/          # Sync logs
│   ├── config.yaml    # Auto-generated
│   └── README.md
```

## URLs

- GitHub: https://github.com/hfmanifold/Clear_Lake_ECI.git
- Shiny App: https://YOUR_ACCOUNT.shinyapps.io/clear-lake-monitoring/

