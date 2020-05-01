# Say

This is a very simple example, creating a single button that triggers the [`say`](x-man-page://say) command.

## Command

```bash
$ Suitcase --name="Say Example" \
  --control-title="Speak" \
    --control-type="button" \
    --control-action="/usr/bin/say Hello World!"
```

## Explanation

    --name="Say Example"
    
Set's the name of the running Suitcase, this is also used for the main window title if `--window-title`  is not set.

    --control-title="Speak"
    
Begin a Suitcase Control. Controls can be started by any of these arguments, `--control-title`, `--control-type` and `--control-action`. By convention `--control-title` is used to denote a new control has begun.

    --control-type="button"
    
Set the type of control. In this example we are creating a button. Valid control types include, `button`, `label`, `text`, or `text-field`.

    --control-action="/usr/bin/say Hello World!"
    
Define the Control Action attached to the button. This action calls the [`say`](x-man-page://say) command and uses an inline parameter of `Hello World!`. Note command locations need to be referenced absolutely. Suitcase *does not* search the `PATH` environment variable.