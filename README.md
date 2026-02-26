# Trakt Search & Watchlist for Kodi

Search for movies, TV shows, and actors, then add them to your custom Trakt lists.

# Orignially built for use on a Vero 5 running Kodi 21.3
---

## Features

- **Search Movies** - Find movies and add to your "movies" Trakt list
- **Search TV Shows** - Find TV series and add to your "newshows" Trakt list  
- **Search Actors** - Browse filmographies and add content to appropriate lists
- **View Lists** - Browse your Trakt lists directly in Kodi
- **Custom Lists** - Works with your own Trakt list names

---

## Setup

### Pre-Requisites
1. Create a Trakt Account and create lists, typically one for Movies and one for TV Shows.
2. Setup Sonarr to import Trakt TV Show list
3. Setup Radarr to import Trakt Movies list

### Installation
1. Download ZIP file and place in a location accessible to Kodi
2. Navigate to Add-Ons and Add from ZIP file
3. Application should appear in the Programs list
4. Launch the application to configure the integrations


### 1. Get Trakt API Credentials

1. Go to https://trakt.tv/oauth/applications
2. Log in (or create free account)
3. Click **"NEW APPLICATION"**
4. Fill in:
   - **Name:** Kodi Trakt Search
   - **Description:** Personal use
   - **Redirect URI:** `urn:ietf:wg:oauth:2.0:oob`
   - **Permissions:** Leave all unchecked
5. Click **"SAVE APP"**
6. Copy your **Client ID** and **Client Secret**

### 2. Configure Add-on

1. Right-click add-on → **Settings**
2. **Trakt Configuration** tab:
   - Enter your **Client ID**
   - Enter your **Client Secret**

### 3. Authorize with Trakt

1. Click **"► Authorize with Trakt"**
2. Note the code shown
3. Go to https://trakt.tv/activate in a browser
4. Enter the code
5. Complete authorization
6. Click **OK** in Kodi
7. You should see "Authorization successful!"

### 4. Configure Your Lists (Optional)

1. Click **"► Fetch My Trakt Lists"** to see your available lists
2. Set your list names:
   - **TV Show List Name:** (default: newshows)
   - **Movie List Name:** (default: movies)

These should match your actual Trakt list slugs.

---

## Usage

### Search for Movies

1. Launch add-on
2. Select **"Search Movies"**
3. Enter movie title
4. Click a result to add it to your "movies" list

### Search for TV Shows

1. Launch add-on
2. Select **"Search TV Shows"**
3. Enter show title
4. Click a result to add it to your "newshows" list

### Search for Actors

1. Launch add-on
2. Select **"Search Actors"**
3. Enter actor name
4. Click actor to see their filmography
5. Click any movie/show to add to appropriate list

### View Your Lists

1. Launch add-on
2. Select **"View 'newshows' List"** or **"View 'movies' List"**
3. Browse items in your Trakt lists

---

## Integration with Kodi Library

This add-on populates your Trakt lists. To sync them to your Kodi library:

1. Use Kodi's built-in Trakt integration
2. Configure it to import from your custom lists
3. Content added via this add-on will appear in your library

---

## Troubleshooting

### "Please authorize with Trakt first"

**Solution:** Click "► Authorize with Trakt" and complete authorization.

### Lists not showing

**Solution:** 
1. Click "► Fetch My Trakt Lists" to verify list names
2. Make sure list names in settings match your actual Trakt lists
3. List names are case-sensitive and should use the "slug" format (all lowercase, hyphens instead of spaces)

### Can't add to lists

**Check:**
- Are you authorized? (try Fetch Lists)
- Do the lists exist on Trakt.tv?
- Are list names spelled correctly?

---

## Requirements

- **Kodi:** Matrix (19.x) or newer recommended
- **Trakt Account:** Free account at https://trakt.tv
- **TMDB API:** Pre-configured (included)

---

## Support

Check Kodi log for detailed error messages:
- **Location:** Settings → System → Logging → View Log File
- **Search for:** `[Trakt Search]`, `[Trakt Authorize]`, or `[Trakt Fetch Lists]`

---

## License

MIT License - Free to use and modify
