# Histogram
This is code for random variable.
# The RANDU random number generator
rrandu <- function(n) {
x0 <- 5
M <- 2^21
a <- 65539
x <- x0
for(i in c(1:n)) {
x[i+1] <- (a*x[i]) %% M
}
return(x/(M+1))
}
# When looking at the histogram of a random sample generated with RANDU, everything seems fine.
x <- rrandu(10000)
idx <- c(1:9998)
hist(x, main="", freq=FALSE)
