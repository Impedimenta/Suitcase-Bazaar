## War Games

> [🧳 Download Suitcase](https://github.com/Impedimenta/Suitcase/releases)

This command builds upon the [Say example](./Say.md), by adding multiple buttons, action parameters and a `text-field` control.

The user can enter text into a `text-field` control and choose what voice is used to speak the string.

### Command

```bash
$ Suitcase --name="War Games" \
 --control-title="Shall we play a game?" \
	--control-type="text-field" \
	--control-identifier="say.textfield" \
  --control-title="Daniel" \
	--control-type="button" \
	--control-group-identifier="g.btns" \
	--control-action="/usr/bin/say" \
	--control-action-parameter="-v,Daniel,say.textfield" \
  --control-title="Samantha" \
	--control-type="button" \
	--control-group-identifier="g.btns" \
	--control-action="/usr/bin/say" \
	--control-action-parameter="-v,Samantha,say.textfield" \
  --control-title="Veena" \
	--control-type="button" \
	--control-group-identifier="g.btns" \
	--control-action="/usr/bin/say" \
	--control-action-parameter="-v,Veena,say.textfield"
```

### Explanation

    --name="War Games"
    
Sets the name of the running Suitcase, this is also used for the main window title if `--window-title` is not set.

    --control-title="Shall we play a game?" 
      --control-type="text-field" 
      --control-identifier="say.textfield" 

These 3 lines define the `text-field`. The first two we encountered in the [Say example](./Say.md), `--control-title` and `--control-type` set the placeholder text and control type respectively. The third option, `--control-identifier`, sets the contol's identifier. An identifier can be used by other controls and actions to reference a control during execution. 

In this example the identifier value, "say.textfield", is used to read the value of the `text-field` and pass it to the [`say`](x-man-page://say) command.

    --control-title="Daniel"
	  --control-type="button"
	  --control-group-identifier="g.btns"
	  --control-action="/usr/bin/say"
	  --control-action-parameter="-v,Daniel,say.textfield"
	  
The next three blocks of options define the buttons, they have the titles, Daniel, Samantha and Veena. The `--control-title`, `--control-type` and `--control-action` are simular to those detailed in the basic [Say example](./Say.md).

    --control-group-identifier="g.btns"
    
A group identifier option, `--control-group-identifier` allows controls to be physically grouped on screen. Any controls tagged with the same group identifier will appear next to each other in the Suitcase window.

	--control-action="/usr/bin/say"
    --control-action-parameter="-v,Daniel,say.textfield"
	
In this control's action declaration, the parameters are specified in the `--control-action-parameter` option and not inline as with [other examples](./Say.md). The `--control-action-parameter` takes a comma separated list of parameters.

One of the parameters listed is the control identifier (`--control-identifier`) from the `text-field` declaration. This will be substituted for the value of the `text-field` before being passed to the [`say`](x-man-page://say) command.

The `-v Daniel` parameters select the voice used to speak the text.

> [🧳 Download Suitcase](https://github.com/Impedimenta/Suitcase/releases)
