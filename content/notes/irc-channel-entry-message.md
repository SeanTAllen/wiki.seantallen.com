---
title: "IRC Setting a Channel Entry Message"
slug: "irc-setting-channel-entry-message"
date: 2018-12-27T00:24:50-04:00
draft: false
tags: [IRC]
description: "Set a message that appears when a user enters the channel."
---
Notes from [GeekShed](http://www.geekshed.net/2011/04/setting-a-channel-entry-message/).

- Who can change a Channel Entry Message?

The channel entry message can only be set, edited, or removed by the channel founder. 

- How do you set a Channel Entry Message?

```
/msg ChanServ SET #channel ENTRYMSG [message]
```

For example:

```
/msg ChanServ set #topgear entrymsg All you have to do is follow some simple rules. Be nice, yield the right of way, and don’t run into anyone else. How hard can it be?
```

- How do you turn off Channel Entry Message?

```
/msg ChanServ SET #channel ENTRYMSG
```

For example:

```
/msg ChanServ set #topgear entrymsg
```