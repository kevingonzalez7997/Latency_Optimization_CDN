# Latency_optimization

## Current Status:
As our collaboration with Nike continues, they recently e-mailed us regarding customer complaints. They mentioned their dissatisfaction with load times. They have requested improvements in latency.

## Observations:
We began testing latency by simulating a surge of users requesting the application. During the blitz, we simulated 1,000 threads to access the application. Given the application's nature, 1,000 threads sufficed for latency measurement. The application was able to handle the traffic without crashing. Before any optimization, we recorded a latency of 40ms.

## Resolution:
Several optimization strategies could lower latency. After discussing the pros and cons with the team, installing a CDN on our application was the optimal solution. We decided to use AWS CloudFront. This approach would route users to the CDN before reaching the web server, resulting in reduced latency since the CDN would have the web page cached. The possibility of deploying multiple CDN servers in various locations was discussed as an additional optimization. This could be deployed later on upon Nike’s request. 

## Purpose: 
The purpose of resolving the latency issue during the Blitz test was to address customer complaints. Nike's customers were unsatisfied with the wait time they experienced while using the application, resulting in a negative user experience. The goal was to improve the application's responsiveness, which was accomplished with a CDN. After installing the CDN latency was re-tested. After Optimization, we recorded a latency of 6ms. This was an optimization of 85%.
