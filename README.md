# picroft example skill gpio Readme

This is a skill for picroft that will interact with the GPIO

## Requirements

This requires a Picroft install on the RPi you can find instructions on the home.mycroft.ai site.
Be sure that mycroft user has the following the group for gpio

## Documenting

The documentation is done by sphinx with some of it in the code.  The following will generate the html docs.

```
cd docs
make html
```

You can then find the generated html in ```docs/build/html/index.html```.  Open that file in your browser and you should be able to navigate the docs.

## Installing
Once you have a picroft image configure it for SSH access.  Change the Makefile ip address for the RPi you installed the image onto.

```make install.pi```

This will installl this source onto the RPi.

## Testing

```make test.pi```

This will run a test to be sure you have access to the gpio be sure to test on the system in a simular manner as mycroft.

## Using

Once installed on a paired Picroft you should be able to issue commands:

```
Turn Led On
Turn Led Off
Blink Led
Led Status
```

And Picroft should respond with the following.

```
Led is Off
Led is On
Button Pressed
Button Released
```

## Files

    vocab - This captures entities used by the skill to understand the vocal command.
    dialog - This is used for responces back to the users.
