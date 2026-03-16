# Digital_Nomad
Automata class assignment
# Object Types
## Population Groups
Population groups are meant to represent a group of sentient creatures looking to survive in harsh conditions
### States
The population group has 3 states consume, spread and starve.
A population starts in the starve state where the energy that they have is depleting. During this state they can move to find resources that way they don't just stay in one spot and die. They can't overlap on any other population groups. So they can get pinned into a location and starve. If their energy reaches zero they die.
Finally, there is the consume state where they increase their energy by decreasing the quanitity of a nearby resource
## Resources
The resources are shown as the color green if they have resources that can be acquired, or yellow if their resources are tapped. 
### States
The resource has three states as well, grow, idle and consume. In the consume state the resource determines how many neighboring population groups it has. Then the resource decreases its qty for each of those neighbors. Once the resource's qty reaches zero, it enters into the idle state. The idle state the resource is dormant for a certain time, then it enters the grow state. During the grow state a resource replenishes it's qty. There is a max qty that a resource can have.
## Seasons
There is a winter phase in this code which decreases the resource's qty by a certain amount. After the initial hit of winter it takes time for the resources to replenish its qty. At some point everything will become green again almost like a spring. I'm not sure what the summer and fall would be in this metaphor.
## Learnings
The more population groups the slower the code runs. There is likely some optimization that can be done for the neighboring checks. I could likely use another object to map the grid to improve the efficiency of the checking.
Even though the movement looks random, unless a parameter is changed the same behavior will present itself.
Because the order of checking neighbors starts at North, there is a clear preference to moving upwards.
When winter comes and the resources are scarce the population groups scatter to areas they wouldn't reach during a fairer season.
