# How to add Valorant Rank Bot command to your chatbot

> Note: Don't forget that !getrank is just the name of the command, you can change it to whatever you want.

### Nightbot
If you are using Nightbot, send the following command in the chat of your Twitch channel (or add it via the Nightbot site manually):
```
!addcom !getrank $(urlfetch https://valorant-rank.vercel.app/rank/$(querystring)?channel=$(channel)&user=$(user))
```

### StreamElements
If you are using StreamElements, add the command as follows:
- Go to https://streamelements.com/dashboard/bot/commands/custom
- In the Response type field, enter the following text:
```
${urlfetch https://valorant-rank.vercel.app/rank/${1}?channel=${channel}&user=${user}}
```


### Streamlabs
If you are using Streamlabs, send the following command in the chat of your Twitch channel (or add it via the Streamlabs site manually):
```
!addcommand !getrank {readapi.https://valorant-rank.vercel.app/rank/{target.name}?channel={channel.name}&user={user.name}}
```
<br />

> Please note that fetching data is currently working for the EMEA region only.
> However, if you would like to extend the functionality to other regions, please feel free to contact me personally via Twitter or Telegram at @gwynnnplaine.

#### Made by @gwynplaine666, with many thanks to @HenrikDev for the data he provided.
