---
title:  "This is a test"
date:   2015-09-06 9:32:00
description: ooh, jekyll!
---

So. I have this thing now. I can do stuff on it apparently. It's pretty cool.

All of this is hosted from Github Pages, and it's open source too.

Obligatory test of syntax highlighting (random snippets from old code):

{% highlight python %}
def get_inventory(db, network, user):
    inv = None
    try:
        query = select([table.c.inv]) \
            .where(table.c.network == network) \
            .where(table.c.user == user)
            
        inv = db.execute(query).fetchall()[0][0]
    except IndexError:
        return {}
    #load JSON
    return loads(inv)
  
@asyncio.coroutine
@hook.command("place", "plant", "fuse", autohelp=False)
def place(bot, conn, event):
    """place <item> [regex]"""
    global set, place, mines, kicks
  	if event.chan not in ENABLED or (conn.name, event.chan) not in status_cache:
{% endhighlight %}

That's about it.. after all, this is just a test.

We now return you to your regularly scheduled programming.
