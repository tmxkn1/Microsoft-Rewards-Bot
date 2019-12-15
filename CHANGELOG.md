**2019-07-09**

    - Fixed sporadic crashes caused by geolocation requests

**2019-07-02**

    - Fixed browser refresh loop caused by login errors
    - Fixed password-based login in headless mode

**2019-06-25**

    - Added support for 2FA, passwordless login via Microsoft Authenticator

**2019-04-03**

    - Added fix for wait_until_visible from .find_element to .find_elements

**2019-04-02**

    - Added adreo00's code for setting log level with argparse

**2019-04-01**

    - Added fix for detecting pcpoints element during point status check
    - Removed edge points as the status screen no longer displays them

**2019-03-01**

    - Incorporated ShoGinn's lightning quiz fix
    - Fixed .cico quiz close patch
    - Added const for logging level

**2019-02-02**

    - Fixed open offer link to target the link

**2019-02-01**

    - Added chromedriver auto-downloading

**2019-01-29**

    - Added error handling for 'credits2', function should exit and script should continue to execute.
    - Changed automation from firefox/geckodriver to chrome/chromedriver
        - Immediate improvement in speed and stability over firefox/geckodriver
        - Appears to use less RAM than firefox (suprisingly..)
        - May be possible to run on raspberrypi (rpi has chromedriver)
    - Mitigated credits2 error by performing an action before going to search URL

**2018-12-20**

    - Performance improvements
    - Fixed login, now waits until page is fully loaded
    - Replaced urllib api call with requests
    - Updated get points with chrome extension source, less prone to error (credit to Shoginn for the url!)
    - Updated quizzes to log open quiz offers, completed quiz offers, all points
    - Modified error catching for alerts, combined with timeoutexception
    - Misc fixes

**2018-11-28**

    - Fixed issue with daily poll IDs changing
    - Added check for sign-in prompt after click on a quiz
    - Misc fixes

**2018-10-20**

    - Added argparse
    - Added points from email links
    - Added randomized account login order
    - Reworked newsapi.org API to google trends
    - Fixed logging
    - Fixed issue with dropped searches

**2018-10-08**

    - Initial release
    - Basic functionality for completing searches and quizzes.
