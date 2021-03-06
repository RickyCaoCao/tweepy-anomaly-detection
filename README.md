# Twitter Trend Alert System
Track any Twitter keyword, mention, or retweet in real-time and instantly alert you via email, SMS, or phone if the keywords are trending.

This should take you **40 minutes or less and with minimal coding knowledge.**
For a full guide of the system, please checkout the blog post: <https://www.pagerduty.com/blog/how-to-twitter-trend-alert>

This is the staging/testing repo. For the official repository, please visit <https://github.com/PagerDuty/twitter-trend-alert-system>.

## Setup

### Install Libraries
This project uses `tweepy` and `datadogpy`.


For quick installment, simply run the following command in cmd/terminal:

```bash
  pip install -r requirements.txt
```

### Configuring API Keys
1. Rename the file `config-sample.py` to `config.py`
1. Enter the necessary API keys within the file.

### Keyword Setup
**Note:** During initial setup, I recommend keeping the default keyword in order to verify that the whole system works.

You can add the Twitter keywords that you want to track in the file `main.py`.

If you want to track multiple keywords, do as following:

`keywords = ['lebron', 'toronto raptors', 'nba']`

## Usage
Run `python main.py` in terminal and you should start seeing filtered tweets.

## Testing
**(Optional)**

If you would like to manually test specific keywords that typically don't receive traffic, there are some scripts available. However, since Twitter does not offer more than one active stream per API token on their free tier, you will need to make another account and get another set of API keys.

### Setup
There is a configuration file within `/scripts` for the new account API keys. Follow the same setup instructions as above.

### generate\_statuses.py
Offers you 3 different options to generate statuses that contain a specific keyword. You can modify the keyword within the script.

### delete\_all\_tweets.py
Since Twitter stops you from posting the same status in a certain period of time, run this script on your test account to quickly remove all your statuses.