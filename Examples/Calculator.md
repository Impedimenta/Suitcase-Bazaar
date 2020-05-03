## Calculator

> [🧳 Download Suitcase](https://github.com/Impedimenta/Suitcase/releases)

This is an attempt to build a functioning calculator using Suitcase. The result technically works, but is not useful in any meaningful way.

```bash
Suitcase --name="SCalc" --window-width="0" \
  --control-title="Spacer" --control-type="spacer" --control-group-identifier="rz" \
  --control-title=" " --control-type="label" --control-group-identifier="rz" --control-identifier="output" \
  --control-title="Spacer" --control-type="spacer" --control-group-identifier="rc" \
  --control-title="SCalc" --control-type="label" 	--control-group-identifier="rc" \
  --control-title="Spacer" --control-type="spacer" --control-group-identifier="rc" \
  --control-title="Hex" --control-type="button" --control-group-identifier="rc" \
    --control-action="/usr/bin/printf" --control-action-parameter="%X,output" --control-action-destination="output" \
  --control-title="Oct" --control-type="button" --control-group-identifier="rc" \
    --control-action="/usr/bin/printf" --control-action-parameter="%o,output" --control-action-destination="output" \
  --control-title="Spacer" --control-type="spacer" --control-group-identifier="r0" \
  --control-title=" C " --control-type="button" --control-group-identifier="r0" \
	--control-action="/bin/echo" --control-action-destination="output" \
  --control-title="Spacer" --control-type="spacer" --control-group-identifier="r0" \
  --control-title="Copy" --control-type="button" --control-group-identifier="r0" \
	--control-action="/usr/bin/printenv output | /usr/bin/pbcopy" \
  --control-title="Spacer" --control-type="spacer" --control-group-identifier="r0" \
  --control-title="÷" --control-type="button" --control-group-identifier="r0" \
	--control-action="/bin/echo" --control-action-parameter="output,/" --control-action-destination="output" \
  --control-title="Spacer" --control-type="spacer" --control-group-identifier="r1" \
  --control-title="7" --control-type="button" --control-group-identifier="r1" \
	--control-action="/bin/echo" --control-action-parameter="output,7" --control-action-destination="output" \
  --control-title="8" --control-type="button" --control-group-identifier="r1" \
	--control-action="/bin/echo" --control-action-parameter="output,8" --control-action-destination="output" \
  --control-title="9" --control-type="button" --control-group-identifier="r1" \
	--control-action="/bin/echo" --control-action-parameter="output,9" --control-action-destination="output" \
  --control-title="×" --control-type="button" --control-group-identifier="r1" \
	--control-action="/bin/echo -e" --control-action-parameter="output,*" --control-action-destination="output" \
  --control-title="Spacer" --control-type="spacer" --control-group-identifier="r2" \
  --control-title="4" --control-type="button" --control-group-identifier="r2" \
	--control-action="/bin/echo" --control-action-parameter="output,4" --control-action-destination="output" \
  --control-title="5" --control-type="button" --control-group-identifier="r2" \
	--control-action="/bin/echo" --control-action-parameter="output,5" --control-action-destination="output" \
  --control-title="6" --control-type="button" --control-group-identifier="r2" \
	--control-action="/bin/echo" --control-action-parameter="output,6" --control-action-destination="output" \
  --control-title="−" --control-type="button" --control-group-identifier="r2" \
	--control-action="/bin/echo" --control-action-parameter="output,-" --control-action-destination="output" \
  --control-title="Spacer" --control-type="spacer" --control-group-identifier="r4" \
  --control-title="1" --control-type="button" --control-group-identifier="r4" \
	--control-action="/bin/echo" --control-action-parameter="output,1" --control-action-destination="output" \
  --control-title="2" --control-type="button" --control-group-identifier="r4" \
	--control-action="/bin/echo" --control-action-parameter="output,2" --control-action-destination="output" \
  --control-title="3" --control-type="button" --control-group-identifier="r4" \
	--control-action="/bin/echo" --control-action-parameter="output,3" --control-action-destination="output" \
  --control-title="+" --control-type="button" --control-group-identifier="r4" \
	--control-action="/bin/echo" --control-action-parameter="output,+" --control-action-destination="output" \
  --control-title="Spacer" --control-type="spacer" --control-group-identifier="r5" \
  --control-title="0" --control-type="button" --control-group-identifier="r5" \
	--control-action="/bin/echo" --control-action-parameter="output,0" --control-action-destination="output" \
  --control-title="±" --control-type="button" --control-group-identifier="r5" \
	--control-action="/bin/bash" --control-action-parameter="-cx,echo \$((\$output * -1))" --control-action-destination="output" \
  --control-title="Spacer" --control-type="spacer" --control-group-identifier="r5" \
  --control-title=" Equals " --control-type="button" --control-group-identifier="r5" \
	--control-action="/bin/bash" --control-action-parameter="-cx,echo \$((\$output))" --control-action-destination="output"
```

> [🧳 Download Suitcase](https://github.com/Impedimenta/Suitcase/releases)