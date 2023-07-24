research thoughts

backtest_trades()
df_trade - symbol, time, tradedir, tradesize, tradeprice
df_mark - symbol, time, smid/mid
mark_times - list of ints
use_smid - mid vs smid

should floor time to nearest time
OR
should convert time into 2 nearest times…
do linear interpolation between them

delete rounded time


ideas:
Is there short-term mean reversion?
 - reversion to ema
is there short-term momentum?
use changes in smid to predict changes in future smid
run arima models on products, ratio of products, diff of products, sum of products
find betas between products, see if residuals are predictive

data processing:
append multiple days together, see if they line up correctly
measure variance at difference points in day, see if they are different, plot for each stock
see if diff days have diff variance

volume graphs:
see total volume requested at diff times of day / minute of the hour
Plot volume in past 5s vs absolute returns over next 5s



hypothesis
- [ ] are there single-product short-term trends? (mean reversion / momentum)
    - [ ] 1 to 60 sec trends
- [ ] are there cross-symbol pairs trades?
    - [ ] check if sum/diff/ratio of symbols is stationary
- [ ] how to differentiate between customers?
    - [ ] volume
    - [ ] timing (time of day, hour of day, date)
- [ ] are there customer patterns that exist across symbols?
- [ ] does customer volume indicate anything about symbols
    - [ ] Plot past 5sec volumes against future 5sec moves (in absolute) 
- [ ] are there nbbo patterns?



infra:
- [ ] Logging into files
    - [ ] At least take a look into it
- [ ] Storing data during round
- [ ] 
