## NRE Topics

WIP list of high-level NRE topics for diving into later. For now, the exercise is about making sure the list is reasonably complete and concise. This is an EXTREMELY WIP list. I'm open to merging, splitting, adding, deleting categories as needed to make it make more sense.

### 1. Workflows and Infrastructure-as-Code

Python, automation tools (Ansible/StackStorm/Salt, etc)

Autonomous workflows. Software gets its inputs from other software (see event driven)

Everything is API-Driven. Not just network device APIs but also cloud service APIs, 

Defining all of the above triggers, tests, workflows, configs, telemetry, policies as code. Treat the code as the source of truth

Workflows have to be:
- End-to-end (campus, DC, WAN, etc)
- Top-to-bottom (L2 - L7)

### 2. Network Observability

[SLI/SLO/SLA Breakdown](https://twitter.com/whereistanya/status/986954786661650432)
- Service-Level Indicators (SLI): X should be true...
- Service-Level Objectives (SLO): Y proportion of the time...
- Service-Level Agreements (SLA): Or else Z.

Metrics. Putting latency, bandwidth, reachability, etc as supporting metrics to SLI

Knowing the applications and users of the network is 100% crucial. You cannot calculate SLI, or MTBF/MTTR from any other perspective.

Everything is measured, and everything is actionable. Either by humans, or by machines.

### 3. Event-Driven Automation

Understanding triggers from #2 and tying them to workflows in #1

Building a culture of seeing a "new" issue, and creating autoremediation for it if possible.

Aim is to never log into the device to remediate issues

### 4. Test-Driven Network Automation

Tests that make assertions about how the network is working, and integrating this into the automation on top

- Network Testing (config linting, operational assertions like "rtr1 must have 3 bgp peers up")
- Application Testing (application performance over the network)

### 5. Application-Centricity

- Cloud-Native Applications
- Cloud Networking
- Distributed systems and applications, and their deployment models

Distributed applications and systems are becoming the new norm. NREs need to be extremely familiar with Layer 7. Understanding that resources are ephemeral and move often.

### 6. Continuous X

- Continuous Integration
- Continuous Delivery
- Continuous Improvement
- Canary Deployments (part of CD?) - making changes in a limited scope as a test, and rolling out slowly - all automated.

### 7. Chaos Engineering

[Principles of Chaos](https://principlesofchaos.org/)

I think there's a lot that can be done for networking here, but there's not a lot of tooling or trust that this is even a good idea today.
Lots of work needs done here to get networks ready for Chaos Testing

## Resources

- [The Future of Network Reliability Engineering](https://michael-kehoe.io/post/the-future-of-reliability-engineering-part1/)
- [networkreliability.engineering](http://networkreliability.engineering)
- [Google's SRE Book](https://landing.google.com/sre/book/index.html)
