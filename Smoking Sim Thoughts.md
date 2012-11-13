**Representing the Human**

We need to have a number of attributes that the modelled human (referred to as a **node**) can work from. These may to take the form of values between 0 and 1 - which allows easy transition over to probabilities. Others will have other ranges that better suit them, these are stated below.

Example attributes are:
* **Peer-pressure factor** - how much immediately local networks change the rest of a node's attributes
* **Local network reach** - a multiplier against the number of nodes a person is away from the source, i.e. the further away, the lower the influence. This would serve well if it could go above	0 since some people may be extremely affected by distant relations
* **Smoking likelihood** - a key attribute that stores the current likelihood for the node to take up the smoking habit. Would work well if it was between 0 and 2, where 1 is the point that is a certain smoking start, and 2 is a doubling in consumption
* **Smoking consumption** - not sure how to represent but would be important when deciding about how it impacts on local connections. High volume smokers are probably more likely to have an effect on others than casual smokers.

Deciding **how far the node can see** is an important factor - perhaps it may be worth degrading the amount they can see as they have more intermediate friends (e.g. you're more likely to know a bit about your friend-of-a-friend than a friend-of-a-friend-of-a-friend). This affects the reconfiguration of the network as the giving up effort goes on. 

**Representing the Network**
**Edges** (connections between people) could be weighted to represent how strong the connection is - as it moves towards zero, that edge is a prime candidate for being removed, where as high-weight ones will play a part in the spreading of influence. This could be recalculated on the fly, and when combined with the ability to store how affected someone is by influence, this provides a mechanism to model person-to-person interactions.

At what point should an **edge be added**? After an initial contact, or after a certain threshold has been reached? Perhaps attributes in common should come into it, like *smoking volume*. The important thought here is whether the edges represent acquaintance, friendship or simply a connection. It could be the case that someone is connected with an enemy, and they want to be an opposite to them. This, however, adds quite a layer of complexity to the model.

**Human-Network Interactions**
Over time, it is crucial that the nodes have the ability to reconfigure as attempts at giving up change. This is important since the success in the attempt may be down to changing your social circle, for example. The changes must not be immediate and wide-ranging though, as if a group wants to give up, the group may well stick together.

Importantly, this is not an 'external' removal, this should be assessed from the point of view of a node. A key decision is whether the edges should be **directed or not**. To date, I have not decided - it is a difficult decision as making them directed allows for a more complex model of the network but introduces complications (much more processing needs to be completed), whilst the undirected approach may be a little simplistic in its view of friendship (it presumes mutual weighing). 

Currently, I feel that directed is a good option since it would, for example, allow a node to reach out to a new person (through extended networks or random meeting) and initiate a connection - this could be reciprocated through some sort of internal 'in and out' register, where a node tracks who talks to them and who they talk to.

**Getting Information From the Network**
Some thoughts are:
* The **ability to trigger** certain parts of the network as an 'Act of God' would be useful - these might represent sudden changes of heart that the model could not represent.
* Generating networks using **real-world statistics** would be good, for example, if the following sentences could be represented:
	* 23% of the population are smokers
	* 40% of the population are smokers but of those, 50% are likely to quit soon.
	* There are 300 people in this network.
The ideal approach is that these kinds of facts would spit out a network that represents a realistic model of a small world, in which there are smokers and non-smokers.
* **Random events** may be worth adding, where a group of nodes randomly meet another. This allows for a simulation of meeting new people, which further affects the smoking effort.
* When it comes to actual simulation, the **rate of events** should be considered. It's unrealistic and probably a hindrance if the model is moving too quickly as it would not represent the often carefully considered approach to giving up smoking that people can take.
* Some form of **analysis** needs to be put together so that the models can be assessed as time goes on. I need to look for research that could be similar to the stuff that will be going on in this model.


