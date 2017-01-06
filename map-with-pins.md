I like the Wikipedia maps with pins that are generated from a list of
coordinates and the choice of a map. E.g., pick Europe and enter coordinates
for Paris, Brussels, and London and you get a map image of Europe with markers
on those spots.

On Wikipedia this is done through the `Template:Location map`. The Lua code
this uses can be found in `Module:Location map`. Can I directly start using
this or will I need to actively convert things over?

Could this be fun to transfer to Rust?

On `Module:Location map`:

- `p` is the "page" it is what is returned and holds the functions that can be
  invoked from the module
- `p.getMapParams` finds the map data given a map name (e.g., Europe). This is
  found in `Template:Location map LOCATION` or `Module:Location
  map/data/LOCATION`. Holds the image and HELLA UGLY LOOKING calculations that
  I assume are used to convert degree to the appropriate spot on the map


# TO READ

- http://www.gnuplotting.org/plotting-the-world-revisited/
- http://xplanet.sourceforge.net/

Via

```
17:49 <Darxus> ward: I wonder if xplanet does what you want?  I used to do a bunch of stuff with that.
17:50 <dsockwell> http://www.gnuplotting.org/plotting-the-world-revisited/
17:50 <dsockwell> that doesnt have borders
17:50 <Darxus> ward: You can feed it a file that contains country / state boundaries,  lat / lon that you want to point to, then a bunch of coordinates for things you want to mark.
17:51 <Darxus> dsockwell: The stuff with the satellite view type maps on this page I did with xplanet: https://www.wired.com/2003/07/slammer/
17:51 <dsockwell> http://www.naturalearthdata.com/downloads/
17:52 <dsockwell> you can dl country vectors there
17:52 <ward> o that looks good dsockwell 
17:52 <dsockwell> and apply mostly the same script as in that blog
17:52 <dsockwell> i guess
17:52 <ward> and I'll have a look at that one too, Darxus 
17:52 <dsockwell> that's what i'd start with
17:52 <dsockwell> gl;hf
17:53 <Darxus> Heh, mapping with gnuplot seems pretty nuts.
17:53 <Darxus> (I did the "as the world churns" (didn't name them) graph in that wired article with gnuplot.)
```
