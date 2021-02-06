---
title:  "Agile Architecture part I"
date:   2021-02-06 21:42:00 +0300
categories: [architecture, agile]
tags: [architecture, agile, archimate]
---

# Agile Architecture. Part I
Hi there! Here is some insights I have by reading some books, papers and docs about agile architecture. I believe that I will proceed to drill down in this topic, so this list will expands

### Dedicated system architects who are not participate in coding become useless
Software or system architecture, which is closest to a daily changing reality, needs to be created by the experts directly in touch with that reality; i.e., the members of Agile teams realizing that system. Classical software architect roles are increasingly being performed by experienced Agile team members rather than by separate experts (Agile Architecture Modeling Using the ArchiMate Language)
### Models better than pictures
It is important to stress the value of models over just pictures. Models can be analyzed, transformed, and visualized in different ways, so they can be the basis for much more than just communicating the essence of an architecture. Moreover, models are much easier to maintain and keep consistent than pictures (Agile Architecture Modeling Using the ArchiMate Language)
### Decisions making should be as deferred as possible
Key in avoiding this “instant legacy” problem is deferring decisions for as long as possible, since deciding too early without sufficient information increases the risk of that decision being wrong. Moreover, you should explore alternatives and not rush into a specific solution too soon. (Agile Architecture Modeling Using the ArchiMate Language)
### Intentional Architecture should be strategic not tactic
Architecture models, especially those with a longer-term outlook, should therefore express intent rather than detailed design. This intent is usually quite stable: the strategy of an organization does not change on a daily basis, and translating that into action is where intentional architecture comes into play. (Agile Architecture Modeling Using the ArchiMate Language)
### Microservices are at least not simpler than monolith
Dealing with large, complex systems requirement is difficult in any methodology, and is perhaps the biggest challenge in adopting Agile ways of working. By their very nature, these large systems are not very Agile because the large number of dependencies they exhibit slows down change.
Some Agile methodologists would say you simply have to break down those systems into chunks that are each manageable by a single team. Microservices are an example of such an approach but, as anyone who has seen them in action knows, the result is often that the complexity that used to be hidden within the single large system now shows up in the connections and communication patterns between these microservices. (Agile Architecture Modeling Using the ArchiMate Language)
### On green field design it's better to start from capabilities and on brown field it's better to start from technology
For a newly to-be-developed solution we recommend starting your models from a feature perspective, expressed in ArchiMate behavior concepts and using, for example, services, functions, and processes. Which application components (or business roles and actors in case of a non-IT-based part of the solution) perform that behavior, and via which interfaces you can get these services, are next steps. On the contrary, when creating models of an existing solution, it is often easier to start with the components and their interfaces, since those are often more “visible” and concrete than services and functions, which are somewhat more abstract and may require some deeper analysis of these components. (Agile Architecture Modeling Using the ArchiMate Language)