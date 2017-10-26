# Step 1 - Register on IFTTT
1. Go to https://ifttt.com/ and create an account (if you don't already have one).

# Step 2 - Make a Discord Webhook
1. Find the Discord channel in which you would like to send Tweets.
2. In the settings for that channel, find the Webhooks option and create a new webhook. Note: Do NOT give this URL out to the public. Anyone or service can post messages to this channel, without even needing to be in the server. Keep it safe!
3. Copy URL and do **not** set a Avatar or Name
-# Step 3 - Make an IF recipe
1. "My recipes"
2. "Create a recipe"
3. Press that underlined huge "this".
4. (Step 1/7) Search for "YouTube" in the "Search channels" box. Click on it. If it needs you to connect YouTube channel (only first time), just click it, log into Google, and authorize it.
5. (Step 2/7) "New public video uploaded by you", for others select `New video from subscriptions` and select the channel.
6. (Step 3/7) Just click "Create trigger".
8. (Step 4/7) Search for "Webhooks" in the "Search channels" box.
9. (Step 5/7) You only have 1 choice.
10. (Step 6/7) Here's the important part.

# Step 4 - Setup the webhook

1. Select **"Post"** in method, and **"application/json"** in content type.
2. Paste your webhook URL in the URL box.
3. Paste the following stuff in **Body**. Edit it if you want.
```json
{
  "username":"YouTube",
  "avatar_url":"https://i.imgur.com/UHWPdp0.png",
  "content":"__{AuthorName}}__ uploaded an new YouTube video: **{{Title}}**: {{Url}}"
}
```
# Step 5 - Finish it!

Now what you have to do is just click "Create Action". It will start to run immediately. You can shut it down using the power button. If there's any error, it'll appear in the log. "Check now" button updates the log in case it is not automatically updated (I think).