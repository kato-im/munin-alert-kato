Send Munin alerts to Kato.
-----------------------------

This script converts Munin alerts into messages in a Kato room.

Put this script somewhere on your Munin master and make it executable. Then
add it as a contact in your Munin configuration like so:

    contact.kato.command [THIS] --kato_url=[KATO_URL]
    contact.kato.always_send warning critical

Replace [THIS] with the full path to this script. Replace [KATO_URL] with url
provided in integrations tab in your room setttings.

Don't forget to add it to your contacts list.

If you want to change the name associated with the message, pass a value for
the --from argument. If you'd like the messages to link back to your Munin
web interface then use --munin-prefix.

If you need to put spaces or other "special" characters in a from value
then you can use URL encoding. e.g. %20 for a space.

Based on [munin-alert-hipchat](https://github.com/distilledmedia/munin-alert-hipchat).
