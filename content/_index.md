+++
title = "Security in collective adaptive systems: a Roadmap by Danilo Pianini"
outputs = ["Reveal"]
+++

{{< slide background-image="assets/bg.png" >}}

<script src="prism.js"></script>
<link rel="stylesheet" href="prism.css">
<link rel="stylesheet" href="blur.css">

## [Security in collective adaptive systems:](https://danysk.github.io/Slides-2019-eCAS-security/)
## [a Roadmap](https://danysk.github.io/Slides-2019-eCAS-security/)

__Danilo Pianini__, Roberto Casadei, Mirko Viroli

---

{{< slide background-image="assets/bg.png" >}}

### Our initial problem

{{< frag c="Find appropriate" >}}{{< frag c=" CAS-specific" >}}{{< frag c=" security practices" >}}
{{< frag c="Research in literature revealed:" >}}

* <span/>
* <span/>
* <span/>
* <span style="color: #222222">.......................................</span>

---

{{< slide background-image="assets/blackhole.jpg" >}}

---

{{< slide background-image="assets/bg.png" >}}

# Actually

There are several works, but they solve specific issues, no comprehensive methodologies for CASs

(to the best of our knowledge, of course)

---

{{< slide background-image="assets/bg.png" >}}

### Safety

*the ability to prevent, intercept, identify, and react to*

{{% fragment %}}**unintentional** *damage*{{% /fragment %}}

### Security

*the ability to prevent, intercept, identify, and react to*

{{% fragment %}}**intentional**, **malicious** *damage*{{% /fragment %}}


* {{% fragment %}}and **privacy** / **confidentiality** is yet another topic{{% /fragment %}}

---

{{< slide background-image="assets/bg.png" >}}

#### They look similar...

they prevent and react to some kind of failure

#### ...but they are tackled very differently

* {{% fragment %}}Different set of tools{{% /fragment %}}
* {{% fragment %}}Different *mindset*{{% fragment %}} -- adversiarial thinking{{% /fragment %}}{{% /fragment %}}

---

{{< slide background-image="assets/bg.png" >}}

### Who cares about security, anyway?

CAS are applied to (or proposed for):

* {{% fragment %}}Swarm robotics{{% /fragment %}}
* {{% fragment %}}e-Health{{% /fragment %}}
* {{% fragment %}}Smart cities{{% /fragment %}}
* {{% fragment %}}Crowd safety{{% /fragment %}}

{{% fragment %}}Human-safety critical systems{{% /fragment %}}

---

{{< slide background-image="assets/bg.png" >}}

### Why are CASs a special case?

Traditional security for distributed, or even P2P systems, may fall short in CAS context

* {{< frag c="Elements from different administrative domains" >}}
* {{< frag c="Often relying on emergence" >}}
* {{< frag c="Side effects on diverse scales" >}}
* {{% fragment %}} Active research --> novel challenges {{% /fragment %}}

---

{{< slide background-image="assets/bg.png" >}}

## Where to start

* Literature on security in related systems
  * Internet of Things (mostly focused on networking)
  * Autonomic computing
* Literature on security methods at large

---

{{< slide background-image="assets/bg.png" >}}

## Security patterns

* {{% color %}}97 security patterns{{% /color %}} identified by six works
* [Systematically organized](https://ieeexplore.ieee.org/document/4267603/) by Hafiz et al. by:
  * Context
  * Threat model

---

{{< slide background-image="assets/bg.png" >}}

## Classification by context

* Core
* Perimeter
* Exterior

Some pattern may involve multiple contexts

---

{{< slide background-image="assets/bg.png" >}}

### Classification by threat model

* {{% color %}}S{{% /color %}}poofing
* {{% color %}}T{{% /color %}}ampering
* {{% color %}}R{{% /color %}}epudiation
* {{% color %}}I{{% /color %}}nformation Disclosure
* {{% color %}}D{{% /color %}}enial of Service
* {{% color %}}E{{% /color %}}scalation of privilege
* Multi-purpose

---

{{< slide background-image="assets/bg.png" >}}

### Higher level patterns

* 12 patterns transcend such classification
* Security {{% color %}}*principles*{{% /color %}} rather than security {{% color %}}*patterns*{{% /color %}}

A bit like the relationship between *architectural* pattern and *design* patterns in programming

--> We will focus on those

---

{{< slide background-image="assets/planning.png">}}

---

{{< slide background-image="assets/planning.png" state="blur-animation" transition="fade-in fade-out" >}}

## Plan for security

* Asset evaluation
* Risk determination
* Security needs identification for assets
* Vulnerability assessment

CASs' openness may imply partial knowledge of assets

---

{{< slide background-image="assets/minefield.jpg">}}

---

{{< slide background-image="assets/minefield.jpg" state="blur-animation" transition="fade-in fade-out" >}}

## Minefield

Custom variations of well-known security algorithms

* Reduces global system knowledge
* May backfire


---

{{< slide background-image="assets/hidden.jpeg" transition="fade-in fade-out" >}}

---

{{< slide background-image="assets/hidden.jpeg" state="blur-animation" transition="fade-in fade-out" >}}

## Hidden implementation

Minimize communication of system details with clients

* Reduces global system knowledge
* May backfire dramatically
* Security cannot be implemented **solely** by obscurity

---

{{< slide background-image="assets/accesscard.jpg" transition="fade-in fade-out" >}}

---

{{< slide background-image="assets/accesscard.jpg" state="blur-animation" transition="fade-in fade-out" >}}

## Policy

Express policies clearly, check conformance, applicate orderly, isolate enforcement

* Lots of useful literature in autonomic computing!
* [SACPL](https://doi.org/10.1007/978-3-642-35887-6_2) a possible base for a formal, CAS-oriented policy language?
* Application in order and isolation of enforcement potentially problematic

---

{{< slide background-image="assets/accesscard.jpg" state="blur" transition="fade-in fade-out" >}}

## Protected System

Prevent unauthorized access as first line of defense

* Mediate access via guards
* Typically enforced via *single access point*
* Potentially clashes with openness and scalability

How to enforce policies for many-to-many access to resources?

---

{{< slide background-image="assets/minas.jpg" transition="fade-in fade-out" >}}

---

{{< slide background-image="assets/minas.jpg" state="blur-animation" transition="fade-in fade-out" >}}

## Defense in depth

Account for threats at multiple layers

* Close to metal
* Platform
* Middleware / coordination
* Application

New implications for CAS!

* Multi-scale / multi-layer adaptation is pervasive
* Attack a layer to open a breach on a higher level
* Turn adaptation against itself

---

{{< slide background-image="assets/hanging.jpg" transition="fade-in fade-out" >}}

---

{{< slide background-image="assets/hanging.jpg" state="blur-animation" transition="fade-in fade-out" >}}

## Low hanging fruit

Keep system in operation, plug the holes

* Related to maintenance and continuous operativity
* Pluggin holes in a CAS? How to?
* Runtime injection of security patches?
* Potentially larger attack surface
* Meta-facilities proposed in CAS
  * None designed with security in mind

---

{{< slide background-image="assets/hacker.jpeg" >}}

---

{{< slide background-image="assets/hacker-self.jpeg" >}}

---

{{< slide background-image="assets/hacker.jpeg" state="blur-animation" transition="fade-in fade-out" >}}

## White hats, hack thyself

Plan and execute attacks under controlled, but non trivial, circumstances

* Especially expensive on a CAS
  * Deployments can be massive
* Behavior is context dependent and situated
* Similarities with corner-case testing
* Simulation as security sandbox?
* Emulating multi-scale attacks can be very hard

---

{{< slide background-image="assets/balance.jpg" >}}

---

{{< slide background-image="assets/balance.jpg" state="blur-animation">}}

## Balancing
### prevention, detection, response

* Don't focus only on prevention
* Perfectly secure CASs are unlikely to ever exist
* Related to monitoring
* Immune system mimicry
* Good news: recovery *might* be easier in CASs

---

{{< slide background-image="assets/bg.png" >}}

## The future

* Analyze the existing security patterns in detail
  * Understand implications
  * Tailor them to CAS
  * Identify unsolved issues
* Consider security when designing CAS
* Better understand multi-level attacks

---
