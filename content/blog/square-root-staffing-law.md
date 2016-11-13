---
title: The Square Root Staffing Law
date: '2016-10-29T09:57:01-04:00'
author: Baron Schwartz
categories:
- Math
- Performance
- Scalability
description: The square root staffing law is a capacity planning rule of thumb.
image: media/2016/10/square-root-staffing-law.png
draft: false

---
The square root staffing law is a rule of thumb derived from queueing theory, useful for getting an estimate of the capacity you might need to serve an increased amount of traffic.

![Square Root Staffing Law](/media/2016/10/square-root-staffing-law.png)

The square root staffing law is designed to help with capacity planning in what's called the QED regime, which tries to balance efficiency with quality of service. Capacity planning is a set of tradeoffs: for best quality of service, you must provision lots of spare capacity (headroom), but that's wasteful. For best efficiency, you minimize idle capacity, but then quality of service becomes terrible.

The QED regime poses the following scenario: assuming that your current quality of service is acceptable, and you want to maintain it, how much must you increase capacity to serve increased demand?

The picture above illustrates this. Suppose you currently have 10 servers (the green circle) and your peak utilization is 25% (the blue circle), so you have 75% idle capacity (the green area). You predict that you'll need to serve 3x the current peak load for, say, Black Friday. How many more servers do you need?

The answer is less than a linear increase to 30 servers (the red dashed line). It's 21, in fact (the orange circle). This answer comes from the rule of thumb that to hold quality of service constant, you must increase the headroom by the square root of the load increase.

If you'd like to experiment interactively with this capacity planning tool, I built a [Desmos calculator](https://www.desmos.com/calculator/iwsypdf7l8) for you. You can drag the circles around to see how parameters such as utilization affect the amount of idle capacity you'll need to provision. You can download an [Excel worksheet](https://www.vividcortex.com/resources/square-root-staffing-law-workbook?utm_campaign=xaprb&utm_source=www.xaprb.com) from VividCortex as well.

The square root rule is an approximation, but it's a decent one, and its bounds are well understood.

<span style="letter-spacing: 0.01em;">To learn more about this, please read my book</span> [The Essential Guide To Queueing Theory](https://www.vividcortex.com/resources/queueing-theory)<span style="letter-spacing: 0.01em;">, which contains further reference material you might also find helpful.</span>  

You might also be interested in learning about the [Universal Scalability Law](https://www.vividcortex.com/resources/universal-scalability-law/), which is a great tool for capacity planning as well.