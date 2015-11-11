# PHPBerks Website

The website for the PHPBerks use group. Built using OpenUG.


## Screenshots

Templates can be found in the `templates` directory and are easily modified. The default layout is a simple bootstrap theme. [Twig](http://twig.sensiolabs.org/) is used as a templating engine.

## How To

### Add Pages

`content/page/{id}.md`

Example `content/page/index.md`:

```md
---
title: Welcome to Local User Group
description: This is an example website for a user group
---

# Welcome to Local User Group

This is an example website for a user group made using [OpenUG][OpenUG].

This website can be modified by editing the files in the `content` directory.

To edit this page, look for the `content/page/index.md` file. It should look like this:


[OpenUG]: http://github.com/AndrewCarterUK/OpenUG
```

### Add Events

`content/event/{id}.md`

`{id}` must contain the `Y-m-d` prefix.

Example `content/event/2015-12-25-christmas-meetup.md`:

```md
---
title: Christmas Meetup
description: We are all meeting at Christmas!
joind.in: http://joind.in/
meetup: http://meetup.com/
talks:
    - @talk:fire-drone
---

# Christmas Meetup

This is an example event for Christmas Day, 2015. Links for joind.in and meetup.com will appear below if they're present in the metadata section of this event.

If present, event talks will also appear on the right hand side of this page.
```

### Add Talks

`content/talk/{id}.md`

Example `content/talk/fire-drone.md`:

```md
---
title: How to create a drone that spits fire
speaker: @speaker:alice
event: @event:2015-12-25-christmas-meetup
joind.in: http://joind.in/blah
---

Learn how to create a fire spitting drone using a Raspberry PI, 10 hair dryers and some tweezers.
```

### Add Speakers

`content/speaker/{id}.md`

Example `content/speaker/alice.md`:

```md
---
name: Alice
talks:
    - @talk:fire-drone
---

# Speaker Profile: Alice

Alice is an example speaker at your user group. You can use this space to write a bio for Alice.

Any talks listed in the metadata section will appear on the right hand side.
```
