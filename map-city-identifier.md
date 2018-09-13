Around Brussels a lot of villages are directly connected to the edge of Brussels.
There is no space inbetween, it often feels like just a continuation of the city.
(I feel like in other countries, these villages might have been absorbed already.)
Is there a way for an algorithm to identify these continuous stretches of "city"?
So in essence, let it start in the centre and automatically grow outwards as long as there is city-like environment to grow on.

I guess you might see it as:
1. chop map into pieces
2. for each piece, decide whether it looks like city (many buildings to open plot ratio)
3. from start point, just add every neighbouring city-piece to your big slice of city
