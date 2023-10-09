# Latency_Optimization

## Current Status:
As our collaboration with Nike continues, they recently e-mailed us regarding customer complaints. They mentioned their dissatisfaction with load times. They have requested improvements in latency.

## Observations:
We began testing latency by simulating a surge of users requesting the application. During the blitz, we created 1,000 threads to access the application. Given the application's nature, 1,000 threads sufficed for latency measurement. The application was able to handle the traffic without crashing. Before any optimization, we recorded a latency of 40ms.

## Resolution:
Several optimization strategies could lower latency. After discussing the pros and cons with the team, installing a CDN on our application was the optimal solution. We decided to use AWS CloudFront. This approach would route users to the CDN before reaching the web server, reducing latency since the CDN would have the web page cached. 

## Optimization 
- The possibility of deploying multiple CDN servers in various locations was discussed as an additional optimization. This could be deployed later on upon Nike's request
- Horizontal scaling with the implementation of a load balancer could also lower latency. The load balancer would distribute the incoming traffic evenly to the new resources
- AWS Global Accelerator could be deployed to create a faster path for our users. This path would run through AWS Global Network and find the closest route.

## Results
- Before Optimization: 40-50ms 
- After CDN installation: 6ms
- This was an optimization of 85%
  
## Conclusion: 
The purpose of resolving the latency issue during the Blitz test was to address customer complaints. Nike customers expressed dissatisfaction with the application's wait times, leading to a negative user experience. The goal was to improve the responsiveness to the application, which was accomplished with a CDN. 
