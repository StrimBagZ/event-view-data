# StrimBagZ Event View Data

Upcoming StrimBagZ feature, planned use case are events like marathons:

 * Integrate marathon schedule (best way would be https://horaro.org)
 * Adding follow buttons for marathon participants
 * Push notification about runs that your interested in

## Requirement(s)

Horaro allows to customize the schedule, this creates the problem of getting 
consistence data, which is important.
As an example we take the schedule of [ESA 2015](https://horaro.org/esa/2015-purple), fair enough this schedule was 
mirrored from speedrun.com, and the [Pre-ESA Online Marathon](https://horaro.org/preesa/schedule)

The schedule of ESA 2015 is almost a perfect template, the only issues here would
be that getting the runners name and maybe getting their Twitch name.
The Runner/Runners column contains special characters like & or vs to indicate a
race, which is fine for reading as a human but not so for automating the process
which this project aims.

The Pre-ESA Online Marathon improved on this, contains a column for both runners
and Twitch username, and separates bot with a comma.
If every marathon schedule would be based on this layout, it would be no hassle
to implement this feature, but thats only the best case scenario of course.

The minimum of data this feature needs would be:

 * Scheduled Time (UTC)
 * Estimate
 * Game
 * Category
 * Runner
 * Twitch username

Best case would be that Runner and Twitch username is the same data and separated
by commas (Runner1,Runner2,Runner3...)

Of course another alternative would be getting this data beforehand, at least the
game, category and Runner/Twitch username, and the rest is getting pulled from
Horaro.

For Push notifications, about when a certain run starts, it requires that the
schedule is updated regularly, the notification will probably be sent 5-10 minutes
prior to the scheduled time.

## Feedback

If you're interested into this feature, feel free to drop your opinion as a GitHub
issue or contact me directly via [Twitter](https://twitter.com/Luigitus)
Especially if you're involved with organizing such a event, it would really interest
me what your thoughts are and if you want to try this feature out in a future event.
