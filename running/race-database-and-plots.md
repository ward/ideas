It would be interesting to see some plots of where runners are distributed in
terms of time (pace?) for certain races. This can and probably should be
generalised to a method that works on any race, assuming the data is in a
proper format. Also useful (necessary) in this is the presence of age and
gender data so you can distinguish this from the rest.  Clearly, once that data
is present, you could also look how the age-grade is distributed in a race.
This in turn is likely useful for an evaluation of age grade like suggested in
[this other idea](agegradeevaluation.md).

Required:

* Scripts to parse results into a sort of standardized format
* Write out what information needs to be saved about a certain race beyond its
  associated results
    * Name
    * Date
    * Distance
* (Possibly, likely) group races per event
* Scripts to turn the standardized race results into nice plots given some
  parameters. Decide on what to do this in. Python's libraries? R?
