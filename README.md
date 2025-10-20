# X.com Profile Cleaner

A Tampermonkey userscript to bulk delete tweets and undo reposts from your X.com (Twitter) profile.

## 🌐 Website

Visit [https://bogdantimes.github.io/x-profile-cleaner/](https://bogdantimes.github.io/x-profile-cleaner/) for easy installation and full documentation.

## Features

- **Delete all tweets** from your profile automatically
- **Undo all reposts** with a single click
- **Real-time counter** showing deleted tweets and undone reposts
- **Auto-scroll** to load older content
- **Smart detection** to only process your own content
- **Pause/Resume** functionality
- **Persistent username** storage across sessions
- **Advanced filtering** using X's search operators (date ranges, keywords, engagement metrics)

## Installation

### Quick Install

**[Click here to install](https://update.greasyfork.org/scripts/553223/Xcom%20Profile%20Cleaner.user.js)**

### Manual Installation

1. Install Tampermonkey for your browser:
   - [Chrome](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)
   - [Firefox](https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/)
   - [Edge](https://microsoftedge.microsoft.com/addons/detail/tampermonkey/iikmkjmpaadaobahmlepeloendndfphd)
   - [Safari](https://apps.apple.com/us/app/tampermonkey/id6738342400)
   - [Opera](https://addons.opera.com/en/extensions/details/tampermonkey-beta/)

2. Click the install link above or:
   - Open Tampermonkey Dashboard
   - Click the "+" tab to create a new script
   - Copy and paste the script from `userscript.js`
   - Save (Ctrl+S or Cmd+S)

## Usage

### Setup

1. Navigate to your X.com profile page (e.g., `https://x.com/yourusername`)
2. You'll see a blue control panel in the top-right corner
3. Enter your username (without the @ symbol) in the input field
4. Click "Save Username"

### Cleaning Your Profile

1. Make sure you're on your profile page or the "Posts & replies" tab
2. Click "Start Cleaning" button
3. The script will automatically:
   - Delete your tweets
   - Undo your reposts
   - Scroll down to load more content
   - Continue until all content is processed

### Advanced: Delete Tweets from Specific Time Period

You can use X's search functionality to target specific tweets:

**Delete tweets from a date range:**
```
from:yourusername since:2023-01-01 until:2024-01-01
```

**Delete only replies:**
```
from:yourusername filter:replies
```

**Delete tweets with specific keywords:**
```
from:yourusername "keyword or phrase"
```

**Delete tweets with low engagement:**
```
from:yourusername max_faves:10
```

**How to use:**
1. Go to X.com search
2. Enter your search query (e.g., `from:yourusername since:2023-01-01 until:2024-01-01`)
3. Press Enter to see filtered results
4. Run the script on the search results page
5. It will only delete tweets shown in those search results!

**Other useful operators:**
- `min_replies:N` / `max_replies:N` - Filter by reply count
- `min_faves:N` / `max_faves:N` - Filter by like count
- `min_retweets:N` / `max_retweets:N` - Filter by repost count
- `filter:links` - Only tweets with links
- `filter:media` - Only tweets with images/videos
- `filter:mentions` - Only tweets mentioning others
- `-filter:replies` - Exclude replies

### Controls

- **Start Cleaning**: Begin the deletion process
- **Stop**: Pause the process at any time
- **Counter**: Shows real-time stats for deleted tweets and undone reposts

## Important Notes

⚠️ **WARNING**: This action is **irreversible**. Deleted tweets cannot be recovered.

### Before Using:

- Consider downloading your Twitter archive first (Settings > Your Account > Download an archive of your data)
- Test on a few tweets first by stopping the script early
- The script respects Twitter's rate limits, but use responsibly

### Limitations:

- Must be on your own profile page or search results to work
- Cannot delete tweets you're mentioned in (only your own)
- May take time for profiles with thousands of tweets
- Twitter may temporarily rate-limit if you process too much too fast

## Troubleshooting

**Script not working:**
- Refresh the page
- Make sure you entered your username correctly
- Check browser console (F12) for errors

**Stuck on certain tweets:**
- Some tweets (like pinned tweets) may need manual deletion
- Click "Stop" and manually delete problematic tweets

**Rate limiting:**
- Take breaks if Twitter shows errors
- The script includes delays to minimize this

**Search results not working:**
- Make sure you're using the correct search syntax
- Verify the search returns results before running the script

## Privacy

- Your username is stored locally in your browser
- No data is sent to external servers
- The script only interacts with X.com

## Contributing

Found a bug? Have a feature request? Open an issue or submit a pull request!

## License

MIT License - Feel free to modify and distribute

## Credits

Created by [@d_g_t_l](https://x.com/d_g_t_l)

## Disclaimer

This script is provided as-is with no warranties. Use at your own risk. The author is not responsible for any data loss or account issues resulting from use of this script.