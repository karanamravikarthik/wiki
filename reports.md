# Gatling Perf Test Reports

* Global Information
* Response time against Global RPS
* Active Users along with the Simulation
* Response Time Distribution
* Response Time Percentiles over Time
* Number of requests per second
* Number of responses per second

The last line of the execution console output shows the HTML report path.

## **Global Information**

This chart shows how response times are distributed among standard ranges. The right panel shows the number of OK/KO requests.

The top panel shows some standard statistics such as min, max, average, standard deviation, and percentiles globally and per request.


Individual HTTP request information can be viewed by clicking on the “Details” tab.

## **Response time against Global RPS**

This chart is only available when looking at the details for an individual request/group.

## **Active Users along with the Simulation**
This chart displays the active users during the simulation: total and per scenario.

“Active users” are neither “concurrent users” nor “users arrival rate”. It is a kind of mixed metric that serves for both open and closed workload models that represent “users who were active on the system under load at a given second”.

It’s computed as:

$(numberofaliveusersatprevioussecond)+(numberofusersthatwerestartedduringthissecond)−(numberofusersthatwereterminatedduringtheprevioussecond)$

## **Response Time Distribution**

This chart displays the distribution of response times.

## **Response Time Percentiles over Time**

This chart displays a variety of response time percentiles over time but only for successful requests. As failed requests can end prematurely or be caused by timeouts, they would have a drastic effect on the percentiles computation.

## **Number of requests per second**

This chart displays the number of requests sent per second over time.

## **Number of responses per second**

This chart displays the number of responses received per second over time: total, successes, and failures.


## **The Report, in numbers**

***Assertions***

**Assertion:** Our assertions are listed in nice readable sentences

**Status:** Whether our assertion passed (OK) or failed (KO)

***Statistics***

*Requests*

All requests, or groups of requests, that were executed as part of our simulation are listed here. We can click on groups to see the requests contained therein.

*Executions*

**Total:** Total times the event* was executed

**OK:** Successful events

**KO:** Failed events

**% KO:** Percentage of failed events

**Cnt/s:** Count of events per second

**Event can refer to either a single request or a group of requests*

*Response Time*

**Min:** The fastest response time

**Percentiles:** How the response time compares with others

**Max:** The slowest response time

**Mean:** The average response time.

**StdDev:** How far the response times vary from the average

**Standard Deviation**

How are the response times spread out from the average?

A low value here indicates that all responses were close to the average, and a high value indicates that they were more spread out.

If we see a high standard deviation we will know that our application does not respond in a consistent manner, the average does not tell the whole story, and it’s time to investigate this erratic behaviour.

**Percentiles**

How does a response time compare to all the others?

All of these statements are saying the same thing:


Measured at the 90th percentile, the response time is 3 seconds.
A response time of 3 seconds is greater than 90% of all responses.
90% of responses were faster than 3 seconds.
10% of responses were slower than 3 seconds.
The larger our user base, the closer to the 100th percentile we want to measure. Whether or not a response time of 3 seconds measured at the 99th percentile is adequate or not will depend on how many end users make up that 1%!

