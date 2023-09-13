---
date created: Wednesday, August 30th 2023, 09:26:58
date modified: Friday, September 1st 2023, 08:20:01
---

# Lab 12 - Extra - Tasks

In the presentation I explained the need for a task system. There are many bright stars in this category. I've found, that with the help of the plugin "Tasks", Obisidian is also that, on steroids. But, you have to really adjust it to your liking.

## Install Tasks

- [ ] Install the community plugin: `Tasks`
    - [ ] Go to `Settings` -> `Community plugins`
    - [ ] Turn off `Restricted mode`
    - [ ] Click `Community plugins` - `Browse`
    - [ ] Search for `Tasks` and install it.
    - [ ] Enable the plugin `Tasks` in `Settings` -> `Community plugins`

## Pitfalls of using tasks in Obsidian

The greatest pitfall of using tasks in Obsidian is the markdown notation of checkboxes: `- [ ] `. This is universally used as signs of todo's. Meetingnotes often contain these, roadmaps of software and many other notes also contain these.

To start collecting and filtering on those checkboxes means you start looking for other peoples tasks and todo's, as well as talking points in meeting notes.

Search for `- [ ]` in your vault, if you are using obsidian for some longer amount of time. Are all the results actionable content which you want to actually do? I firmly expect "No!" to be your answer.

So it helps, as talked about in the presentation, to think of tasks as abstract or meta pointers to an actual content. Tasks shouldn't contain information, they should link to information. When you write such a task: "Work on proposal", "Chase topic X" you want to keep it short and sweet in order to keep your tasklist manageable.

We'll make sure that the Tasks are true tasks by putting a defining label on them:

- [ ] Go to `Settings` and select `Tasks`.
- [ ] Put a clear defining tag in `Global Filter`. I've put `#ST` there, (Stephs Tasks), to be able to filter them all.
- [ ] Go to `Settings` and select `Hotkeys`
- [ ] Search for `Tasks: Create or edit task` and assign it `control`+`option`+`t` (mac) or `control`+`alt`+`t` (other)
    - *This shortcut will be your way to create new and edit existing tasks.*
- Heavily suggested:
    - [ ] Disable the `Auto-suggest task content` toggle. The pop-ups are very distracting and off-putting.
- [ ] Restart Obsidian for the changes to have effect.

## Create the base of a task system

Please create two notes in your vault:

- `Recurring`
- `My Tasks Dashboard`

### Exercise: Recurring tasks

Go to the `Recurring` note and experiment with the workings of recurrence:

- [ ] Press `control`+`option`+`t` to start creating a tasks
    - [ ] try putting in different recurrences:
        - [ ] "Every month on the first"
        - [ ] "Every 3 months on the last friday"
        - [ ] "Every monday"
        - [ ] "Every monday when done"
        - [ ] [Read what "when done" means on this page](https://publish.obsidian.md/tasks/Getting+Started/Recurring+Tasks)
    - [ ] Add a scheduled date, as this is needed for a recurring tasks to work. Use natural language:
        - [ ] "friday"
        - [ ] "next friday"
        - [ ] "in two weeks"
        - [ ] "next weekday"
    - [ ] Confirm the task
- [ ] Check the task to see the magic. Check the new one too.
- [ ] Edit the task to add or remove "when done" from the recurrence.
- [ ] Now, check the task again. And the new one. See the difference?

### My Tasks Dasboard

After the previous exercise you'll have created some garbage to list here, so let's go about creating a cool and useful dashboard!

Past this in your dashboard note:

<pre><code>

# My Tasks Dashboard

## Late

```tasks
scheduled before today
group by scheduled
not done
```

## Today

``` tasks
(scheduled today) OR (no scheduled date)
group by scheduled
not done
```

## This week

``` tasks
(scheduled after today) AND (scheduled this week)
group by scheduled
not done
```

## Next week

``` tasks
(scheduled next week)
group by scheduled
```

## Later

``` tasks
(scheduled after next week)
group by scheduled
```
</code></pre>

The queries are quite readable right? Adjust to your liking!  
[Here's the documentation](https://publish.obsidian.md/tasks/Queries/About+Queries)

## Exercise: Birthdays

Create a file in your vault named `Birthdays`.

- [ ] Put in one or 2 birthdays using the `control`+`option`+`t` shortcut.
    - ie: `- [ ] James birthday 🔁 every September on the 25th ⏳ 2024-09-25 `
- [ ] Try to adjust the filters in your `My Tasks Dashboard` so that:
    - [ ] Birthdays are filtered out of the queries yet in place.  
          [Could be helpful](https://publish.obsidian.md/tasks/Queries/Filters#Filters%20for%20File%20Properties)
    - [ ] Put a new header for birthdays in your dashboard. Place a query showing you today's birtday  
          [Could be helpful](https://publish.obsidian.md/tasks/Queries/Filters#Searching%20for%20dates)
