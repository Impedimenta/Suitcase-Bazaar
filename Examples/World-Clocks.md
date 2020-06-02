## World Clocks

This example uses [Erica Sadun's](https://twitter.com/ericasadun) [`now`](https://github.com/erica/now) (a command line tool for calculating times around the world) to return the input time in the local time zone for members of my team.

```bash
#! /usr/local/bin/Suitcase interpreter

# Print out the times for each member of your team!
# Using `now` by Erica Sadun we can quickly print 
# the local time info for all of the team.
#
# Install `now` using `mint`,
#
#    % mint install erica/now
 
# Application 
--name="World Clocks" 
--window-floating # The window will be infront of all others
--window-width="620"
--application-identifier="5797E2A3-6836-4867-9BA6-3AA560B4BBEB"

--control-title="Time:" 
  --control-type="label"
  --control-group-identifier="g.time"
  
--spacer
--control-group-identifier="g.time"
  
# Text field for entering the time to look up
--control-title="5PM" 
  --control-type="text-field"
  --control-group-identifier="g-time"
  --control-identifier="id-time"

# Team

# Rad
--control-title="🤔 Rad in" 
  --control-type="label"
  --control-group-identifier="g.rad"

--control-title="Tokyo, Japan" 
  --control-type="label"
  --control-group-identifier="g.rad"
  --control-identifier="id-rad-loc"

--spacer
--control-group-identifier="g.rad"

--control-title="--:--:--" 
  --control-type="label"
  --control-group-identifier="g.rad"
  --control-identifier="id-rad-time"

--spacer
--control-group-identifier="g.rad"

--control-title="🕰" 
  --control-type="button"
  --control-group-identifier="g.rad"
  --control-action="/usr/local/bin/now"
  --control-action-parameter="--local,id-time,id-rad-loc"
  --control-action-destination="id-rad-time"
  
# Pablo
--control-title="🎨 Pablo in" 
  --control-type="label"
  --control-group-identifier="g.pab"

--control-title="Madrid, Spain" 
  --control-type="label"
  --control-group-identifier="g.pab"
  --control-identifier="id-pab-loc"

--spacer
--control-group-identifier="g.pab"

--control-title="--:--:--" 
  --control-type="label"
  --control-group-identifier="g.pab"
  --control-identifier="id-pab-time"

--spacer
--control-group-identifier="g.pab"

--control-title="🕰" 
  --control-type="button"
  --control-group-identifier="g.pab"
  --control-action="/usr/local/bin/now"
  --control-action-parameter="--local,id-time,id-pab-loc"
  --control-action-destination="id-pab-time"
  
# Miranda
--control-title="🌸 Miranda in" 
  --control-type="label"
  --control-group-identifier="g.mir"

--control-title="Bristol, UK" 
  --control-type="label"
  --control-group-identifier="g.mir"
  --control-identifier="id-mir-loc"

--spacer
--control-group-identifier="g.mir"

--control-title="--:--:--" 
  --control-type="label"
  --control-group-identifier="g.mir"
  --control-identifier="id-mir-time"

--spacer
--control-group-identifier="g.mir"

--control-title="🕰" 
  --control-type="button"
  --control-group-identifier="g.mir"
  --control-action="/usr/local/bin/now"
  --control-action-parameter="--local,id-time,id-mir-loc"
  --control-action-destination="id-mir-time"
  
# Richard
--control-title="🤖 Richard in" 
  --control-type="label"
  --control-group-identifier="g.rjs"

--control-title="Cupertino, US" 
  --control-type="label"
  --control-group-identifier="g.rjs"
  --control-identifier="id-rjs-loc"

--spacer
--control-group-identifier="g.rjs"

--control-title="--:--:--" 
  --control-type="label"
  --control-group-identifier="g.rjs"
  --control-identifier="id-rjs-time"

--spacer
--control-group-identifier="g.rjs"

--control-title="🕰" 
  --control-type="button"
  --control-group-identifier="g.rjs"
  --control-action="/usr/local/bin/now"
  --control-action-parameter="--local,id-time,id-rjs-loc"
  --control-action-destination="id-rjs-time"
```
