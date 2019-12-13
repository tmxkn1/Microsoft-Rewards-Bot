# Microsoft-Rewards-Bot

Microsoft Rewards (Bing Rewards) Bot - Completes searches and quizzes , written
in Python! :raised_hands:

## Overview

This program will automatically complete search requests and quizzes on
Microsoft Rewards! Search terms are the daily top searches retrieved using
Google Trends' API. This bot runs selenium in headless mode for deployment on
VPS and for increased performance on local machines. The bot also uses
selenium's user agent options to fulfill points for all three platforms (pc,
edge browser, mobile). 100% free to use and open source. Code critique/feedback
and contributions welcome!

## Features

- Completes PC search, Edge search, Mobile search via user agents
- Retrieves top daily searches via Google Trends' API
- Completes polls, all types of quizzes (multiple choice, click and drag and
  reorder), and explore dailies
- Headless mode (Confirmed working on DigitalOcean linux droplet)
- Supports unlimited accounts via JSON, in randomized order.
- Randomized search speeds
- Logs errors and info by default, can log executed commands and search terms by
  changing the log level to DEBUG
- Tested and confirmed working for U.S. and U.K. (more to come!)

## Requirements

- Python 3.6
- Requests 2.21.0
- Selenium 3.14.0
- Chrome Browser

## How to Use

1. Clone and navigate to repo
2. Modify ms_rewards_login_dict.json with your account names and passwords,
   remove .example from filename.
3. Enter into cmd/terminal/shell: `pip install -r requirements.txt`
   - This installs dependencies (selenium)
4. Enter into cmd/terminal/shell:
   `python ms_rewards.py --headless --mobile --pc --quiz`
   - enter `-h` or `--help` for more instructions - `--headless` is for headless
     mode - `--mobile` is for mobile search - `--pc` is for pc search - `--quiz`
     is for quiz search
     - `-a` or `--all` is short for mobile, pc, and quiz search -
       `--authenticator` use Microsoft Authenticator prompts instead of
       passwords - **When using Microsoft Authenticator:** - Headless mode is
       always disabled - Respond to the prompt within 90 seconds and Approve the
       sign in request - Learn how to use and download the app at
       [https://go.microsoft.com/fwlink/?linkid=871853](https://go.microsoft.com/fwlink/?linkid=871853)
   - Script by default will execute mobile, pc, edge, searches, and complete
     quizzes for all accounts (can change this setting in the .py file)
   - Script by default will run in interactive mode
   - Run time for one account is under 5 minutes, for 100% daily completion
   - If python environment variable is not set, enter
     `/path/to/python/executable ms_rewards.py`
5. For completing points from email links:

   - Modify email_links.txt file with email links. - Copy and paste links
     without surrounding quotes, each on individual line, like such:

     ```
     httplink2
     httplink3
     ```

   - Enter cmd/terminal/shell argument `python ms_rewards.py --email`
   - **Script will be manual, requires key press to continue, as the quizzes are
     not yet standardized.**

6. Crontab (Optional for automated script daily on linux)
   - Enter in terminal: `crontab -e`
   - Enter in terminal:
     `0 12 * * * /path/to/python /path/to/ms_rewards.py --headless --mobile --pc --quiz` -
     Can change the time from 12am server time to whenever the MS daily searches
     reset (~12am PST)
   - Change the paths to the json in the .py file to appropriate path

## To Do

- Argparse for options: - logging - custom user agents
- Rewrite script into class-based code or Organize monolithic code into
  different py files for maintainability
- os.environ variables for multiple logins (current account names and passwords
  are too long)
- Proxy support
- Multithreaded mode or seleniumGrid
- Support for other regions
- Telegram Intergration for reporting bot status/total points.

## License

100% free to use and open source. :see_no_evil: :hear_no_evil: :speak_no_evil:

## Versions

For a summary of changes in each version of the bot, please see the
**[CHANGELOG](CHANGELOG.md).** Alternatively, a list of
**[all commits to xMNG/master](https://github.com/xMNG/Microsoft-Rewards-Bot/commits/master)**
is also available.

#### Special Thanks

@ShoGinn - for extraordinary assistance in making this project better!
