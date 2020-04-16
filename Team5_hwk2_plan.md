# Team 5 Homework 2 Project Outline

## Summary
Does the type of AWS EC2 instance affect observed network performance in real life conditions? If so, how much?  To answer this question, Team 5 will run a series of experiments.  Specifically, we will choose to compare three instances in the `M4` family that AWS claims will have low, medium, and high network performance: `M4.Large`, `M4.2xLarge`, and `M4.16xLarge`.  We will use the `iperf3` test to examine network latency and bandwidth for all three types of instances under both on-demand (OD) and spot pricing at both peak (11AM) and off-peak (11:59PM) times.  To maintain comparability, we will run our experimental instances on the same day of the week in the AWS us-west-2 region.  This produces a  3 $\times$ 2 $\times$ 2 research design, as reflected in the table below.

|               | `M4.Large`  | `M4.2xLarge`| `M4.16xLarge`|
|:-------------:|:-----------:|:-------------:|:------------:|
| Spot, peak    | $Z$         |  $Z$          | $Z$          |
| Spot, off-peak| $Z$         |  $Z$          | $Z$          |
| OD, peak      | $Z$         |  $Z$          | $Z$          |
| OD, off-peak  | $Z$         |  $Z$          | $Z$          |

The value, $Z$, represents the number of `iperf3` tests that will be run in that instance type.  We will run a test on the most expensive instance (OD peak `M4.16xLarge`) to get an upper bound on cost and then set $Z$ such that $12Z$ `iperf3` tests will cost less than \$50-\$75.

We will document the mean, median, standard deviation, and maximum values for both network performance (Kb/s or PPS) and cost (\$ / Kb or packet).  We will also document the percent of spot intances terminated by AWS.

### Next Steps:
1. Discuss the instances types to experiment
1. Method experts learn how to use iperf to calculate the speed and discuss what will be the measurement 
    1. [Amazon network speed calculation](https://aws.amazon.com/premiumsupport/knowledge-center/network-throughput-benchmark-linux-ec2/)
1. Decide how many attempts to run based on the cost
1. Method expert write iperf script and lanch the experiment
1. Summarize the data and analyze
1. Write up 
