Look into age grade a bit more. Try to come up with how valid it is? Is
a ratio of the WR really the way to go? Is that really what is impressive?

Think about:

* plots
* how quickly it goes down for some distance comparing ages and genders

Compare this to distribution of runners in a race?

Also see [race-database-and-plots.md](race-database-and-plots.md)

--

Some quick R (times for the 20k)

```R
wr <- 3315
times <- seq(wr, wr+3600, 60)
ratios <- wr/times * 100
fwr <- 3700
fratios <- fwr / times
fratios[fratios > 100] <- NA
plot(times, ratios, xlab="Time (s)", ylab="Age grade", type="l", col="red")
lines(times, fratios, type="l")
```
