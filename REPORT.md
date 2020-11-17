```
NOK = Not Ok 

MOK = More or less ok

NRV = Done but need revision (grammar - spelling - content)

OK = Done.
```

----

[toc]

-----

# 0. Abstract [NRV]

Ants are among the most simple beings out there and yet they are capable of great things such as building structures, communicate in a very non-conventional fashion, concentrate their manpower to gather supplies, and defend their nest. This document references the life of ants from what they are and where they come from to how they behave in order to see if it is possible to collect emerging collective behaviors to implement in simulations. While gathering the information, how to simulate the collected behaviors will be discussed in two distinct ways: The first one will be a software-based simulation where programming languages such as Javascript or C will be studied to evaluate if they fit the needs of such a task,  and used to represent the ants moving to replicate as much as possible the studied behaviors. The second simulation will be robotic-based and will aim at fetching one or two behavior to replicate the complexity of these when applied to swarm robotic in a reduced setup.

# 1. Introduction [NOK]

[NRV]

This project is part of the "[Research project (K-CS and K-SD) Autumn 2020 (KIREPRO1PE)](https://learnit.itu.dk/course/view.php?id=3020186)" ITU course which intends to be a bridge between the specialization course and the master thesis (that is, a preliminary work for the Master thesis). Its aim is the study of the abstract mechanisms employed by ants. Ants are one of the various social species that can be studied to create bioinspired algorithms and models of collective behaviors. They are very interesting because as a single unit, an ant is a very simple being, but as a swarm, they show a lot of exciting collective behaviors, and their underlying mechanisms can be studied and used for everyday problems.

The art of studying nature to replicate its behaviors into a robotic/algorithm to solve complex human problems is called "bio-inspired robotic" (also more commonly know as “Biomimetic”). There are numerous examples such as the very famous “Japanese Bullet train” (Shinkansen) which gets its nose design from the Kingfisher bird’s beak (who’s aerodynamic ), reducing the train’s energy consumption by 15%, making it 10% faster and quieter [^0]. The hook and loop fastener (also known as the Velcro), created by the Swiss engineer George de Mestral in the 1950s is also a very famous example of biomimetic. This two-part binding system was inspired by burrs, which de Mestral studied under a microscope after he figured how surprisingly easy these would stick to its dog's hair. He discovered that burrs had micro hooks that were able to catch anything with a loop. Nowadays, the hook and loop fastener is used throughout the world [^0]. Bio-mimetic is also very useful in robotic as today's human problems get more and more complex, risky, and costly. Amazon uses a large network of swarm robots in their warehouse to control the package so that the human workers on site don't even have to move. The ordered package comes to them, they fill the box and staple it, and put it back on the robot to be ready for delivery [^24] . Another good and relevant example is the network's Honey bee algorithm. Back in 1988 in the Georgia Institute of Technology, Professor John Hagood Vande Vate discovered after some discussion how effectively nectar foragers honey bee could distribute themselves effectively among the local clusters of flowers without any central authority. The professor and his team of computer scientists built up an algorithm to reflect the seen behavior. This algorithm sat for a decade, unused, until an Oxford student named Sunil Nakrani needed inspiration for a web hosting problem. Sunil and the professor refined the honey bee algorithm to make it fit the situation and made Internet Web hosting services dramatically more efficient [^25].

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/bullet_train.jpg?raw=true" alt="alt text" title="The Shinkansen bullet train" style="zoom:25%;" />



<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/burrs.jpg?raw=true" alt="alt text" title="Burrs and their loops" style="zoom:60%;" />



## 1.1 State of art [NOK] [TODO]

### 1.1.1 Software

Biomimetic being a growing study topic, one could easily think the internet is place to thousands of alike project. 

Needless to say that even though some project ressemble the goal of this paper, theres

Even though biomimetic on ants is a very studied topic with numerous papers, videos and books about the subject, there is no proper implementation of an ant war simulator. The closest implementations are simulations of pathfinders (here is an example found on Github: http://bwiklund.github.io/ant-simulator/) or very low level territory defence demonstration (such as https://github.com/computationalcore/ants-simulation). 

https://github.com/computationalcore/ants-simulation -> nice! ant colony simulator, the brain of each ant is fairly simple but that's a start

https://github.com/karask/AntSim -> could be useful but poorly documented

http://ants.aichallenge.org/

https://github.com/ultimape/PixelAntColony

write way more here, find examples video and relevant study on the subject

Talk about examples from the file from Payam.

It is very likely that this project will be a reflection of all the studies, such as “Combat between large derived societies: A subterranean army ant established as a predator of mature leaf-cutting ant colonies” written by Scott Powell or “The Remarkable Self- Organisation of Ants”, written by Emily Singer.

https://ccl.northwestern.edu/netlogo/

Pocket ant (game)

### 1.1.2 Robotic

- 272 e-puck robots

- Kilobot

- Locomotion unit

- Jasmine III

- SwarmBot -> https://www.youtube.com/watch?v=77SEQ-kj8PI&ab_channel=ScienceSquared

  [^Robot that can replicate swarm behaviours](https://newatlas.com/colias-swarm-robot/33897/)

# 2. The ant kingdom [NRV]

This section is about ants. Their history, their birth, their life, but also how they function and behave in groups and individually. As we are restrained in time and space, we will talk about only a very few of the enormous amount of interesting species that exist out there. The end goal is to give ourselves an Idea of which ant species are good candidates for a simulation and why they are but also to highlights very interesting biological behaviors that emerge within each species. At the end of the section, some of these biological behaviors will be chosen, based on preferences and interests, to be used later for the simulation. 



## 2.1 Ants [NRV]

Ants are ancient beings that emerge around 140 to 168 million years ago, even though they started to diversify only about some 60 million years after [^1] [^2]. From the dinosaur era to the Human realm, no kingdom has ever been as large and as powerful compared to the ants super-kingdom. They are estimated to be about 10'000'000'000'000'000 (10'000 trillion) individuals [^4], which account for 20% of the total animal biomass [^3] [^5]. This superkingdom, however, is far from being an unified and coherent heaven. From the 16'000 classified species and the 20'000 estimated species [^2], rare are the ant species that resemble one another. Indeed, from the very early age of their existence, ants have been evolving and adapting to a large amount of environment. They now come in a large variety of colors, from yellow to black. They live in every environment, from extreme heat desert to rainy forests and swamps. The only places that remain untouched (almost) are cold and high places on earth, as ants need a heat source to survive [^6]. Individually, ants cannot do much, they are too simple and their brain is only capable to perform a limited set of action. To become what ants are today, they needed something fundamentally important: Collaboration. It is like the human race. We, throughout the years, had to come up with some very complex collaboration tools and framework to construct the society we have nowadays. 

Throughout this collaboration ants are capable of achieving the greatest. They can assemble themselves into complex structure such as bridge or boat to overcome environmental challenges, they achieve agriculture through foraging and maintenance, and have complex symbiotic relationships[^7]. However, this collaborative behaviour only emerges within ants of the same colonies (and sometimes, but less likely, of the same species). Ant colonies are more likely to fight or avoid contact than discuss peacefully about what would be the best strategy to get the piece of bread from a picnic and how it would be beneficial for each of them. So what is the difference? What makes them less able to collaborate than humans? As described earlier, they have a very limited brain, they have eyes and they can somewhat distinguish between dark and light, they have a limited set of communication tools and understanding of the world, which have make them less able to develop collectiveness within other species during the evolution. At their level everything but the colony and the queen survival is meaningless.

## 2.2 Interesting species [NRV]

Throughout this sub-section, we will talk about a few ant species that stands out within the 12000 others. Going trough the Army Ants first as they will be the once used for the simulation because they deliver the most interesting collective behaviour, to 4 other types of ants that are also interesting to mention and from which we are going to highlight a few biological behaviors: Carpenter ants, Leafcutter ants,  and Pharaoh ants are among the most known species of ants. This because they mostly exist in an environment close to humans and thus are more inclined to have interaction with our society.

### 2.2.1 The army ants (*Marabunta*) [NRV]

From all the known ants species, there is a category of ant legitimately called "the army ants". This category that the evolutionary tree has brought to be combatants, are dreadful warriors among the ground. They have been given large mandibles, painful sting and armour, and it exists about 200 species of them [^8]. If two colonies or species encounter one another in the nature, it is unlikely that they will fight against each other. Indeed, this makes sense from an evolutionary stand points as throughout time army ants that were attacking other army ants eradicate themselves to extinction [^11]. They don't have a nest, they rather like to crawl on the ground in a very long and narrow group, consuming up to 500'000 prey animals each day [^9][^27]. The behaviour of crawling on the ground is something specific to the army ants called the "Army ant syndrome" [^10] (see Figure N). This syndrome is a two phase life style cycle that army ants have adopt to .. ?. 

In the first two to three weeks long phase called the stationary phase, the prey that were previously used to feed to the larvae are now reserved to the queen for her to prepare her birth cycle. The queen they lays her eggs and reaching the end of the stationary phase, the new born larvae emerge from their cocoons as the colony prepares itself to enter the second phase. [^9] 

The second phase called the "Nomadic phase" last approximately 15 days, which gives the time for the new born larvae to develop into fully functional workers. In this phase, the colony moves during the day, etching on the ground and capturing everything they can, from insects, spiders and even dead ant bodies. Usually an ant colony would send one or few scouts to look around the colony and seek for food or threats, but the army ants are leaderless group of foragers and like to overwhelm the prey at once sending by sending a lot of them. At the end of the 15 days, the larvae no longer require food and the colony can enter the stationary phase again. [^9] [^26]

<img src="https://ars.els-cdn.com/content/image/3-s2.0-B9780128015322000143-f14-29-9780128015322.jpg?_" alt="alt text" title="simulation rep 1" style="zoom:100%;" />



### 2.2.2 Carpenter ants (*Camponotus spp*) [NRV]

<img src="https://images.squarespace-cdn.com/content/v1/502d2cede4b0ab396711e089/1452718051897-X50TNDX2FA0ZPGLV2R8R/ke17ZwdGBToddI8pDm48kPm4n540DuKLRMJEMZqwAkMUqsxRUqqbr1mOJYKfIPR7LoDQ9mXPOjoJoqy81S2I8N_N4V1vUb5AoIIIbLZhVYy7Mythp_T-mtop-vrsUOmeInPi9iDjx9w8K4ZfjXt2dotFL7oufSUosRNfcO_cim7GlB-pHugHaNE4nEeDGWx4W07ycm2Trb21kYhaLJjddA/image-asset.jpeg?format=1500w" alt="alt text" title="" style="zoom:30%;" />

Carpenter ants, represented in Figure N, are inhabitants of a lot of forest in the world. They like to build their nest in high humidity woods and they alone account for approximately 1000 ant species. If carpenter ants are among the most known species in the world, it is because they are sadly famous to be a nuisance to a lot of buildings and structures made of wood, causing structural damages. Nevertheless, carpenter ants are interesting little beings. A mechanism to highlight from their collective behavior is that, once their primary nest is big enough, carpenter ants like do build satellite nest containing workers while the eggs, the newly hatched larvae, and the queen remain in the primary nest. [^12] [^14]



### 2.2.3 Leafcutter ants ( *genera Atta - Acromyrmex*) [NRV]

<img src="https://bloximages.chicago2.vip.townnews.com/tucson.com/content/tncms/assets/v3/editorial/6/f8/6f8ee49e-8721-53f0-acb4-1cecb5f4ed7a/57ed68f427660.image.jpg?resize=1200%2C856" alt="alt text" title="" style="zoom:37%;" />

Leafcutter ants are tiny ants of about 47 species which can carry about 20 times their body-weight. If an average-sized human could do that, he would be able to pull up to 1400kg [^13]. As their name may imply, Leafcutter ants cut fragments of a leaf which they bring back to the nest to feed the fungus garden. The fungus garden is the main source of supply of the colony and they take good care of it. The fungus garden can generate chemicals to tell the ants if the fragments they brought back from the foraging are toxic or not. This collaboration between ants and fungus is called an ant-fungus mutualism. But the care of the fungus garden does not end here. Indeed, a category of worker is specialized in taking care of it and bring the toxic leaf and dead leaves to a waste heap. These waste transporters are the older, more dispensable leafcutter ants that ensure that the younger and more functional workers can work safely in the fungus garden. Once the waste is deposed in the waste heap, workers constantly organize the waste to help decomposition [^15] [^18]

#### Colony hierarchy

Like any other ant species, Leafcutter ants are a well-organized group. There are 4 main classes starting with the "minims". The minims are the smallest worker and they take care of growing the brood and make sure the fungus garden is in safe hands. The second category, the minors, are slightly larger workers which are the first line of defense against external threats. Their main occupation is to patrol around the nest and making its surrounding a safe place. The third category is the one depicted in all photography (yes, it is the one in Figure N). They are the "real" Leafcutter. They are generalised foragers and wander outside the nest to cut leave fragments and bring them back to the nest. The fourth and last category is the Majors which are the largest worker ants. They are the soldier of the nest, defending and attacking against outside threats. Moreover, this category of ants also helps in other tasks such as cleaning the foraging trails of large debris. [^13]



### 2.2.4 Pharaoh ants (*Monomorium pharaonis*) [NRV]

<img src="https://pestclue.com/wp-content/uploads/2020/03/Pharaoh-ants-1200x675.png" alt="alt text" title="" style="zoom:45%;" />

Pharaoh ants are infamously known as the largest indoor nuisance pest as they have established themselves in the most part of the world (given a reliable source of heat) due to high human migration movements with the exponentially growing access to transports such as boats, planes or cars. Pharaoh ant colonies are polygynous, which means they can contain more than a singe queen, the highest number of queens found in a single colony is 200. Each of these queen will lay up to a hundred eggs in their lifetime. In order to move and choose a convenient nest they use a decision making behaviour . It seeks to minimize the time the colony is without a nest while optimizing the nest the colony finally chooses. [^17] [^16]



#### Pheromones [^19] [^17]

Pharaoh ants have three interesting type of pheromones. The first one is a long-lasting attractive chemical used to build trail networks which can remain detectable even if it is unused for several days. This long-lasting chemical has been studied on this particular type of ants we it has been seen that pharaoh ants cease activity at night and begin each day of work at around 8 am, yet parts of the trail network are identical each day. The second one is a mid-lasting pheromone which usually disappear in a matter of minutes. This type of pheromone is used to indicate path to a food supply. Finally the last type, which decay after two hours, is a repellent pheromone (or negative trail) which indicates that a path to a food supply is inefficient. 

# 3. Ant behaviours and mechanisms [NOK]

This section is about ants behaviours and mechanisms, we will go through the behaviours we mentioned in the early paragraphs of this paper as well as some new ones to see how collective behaviours can emerge when every element of the colony activate itself to a task. The aim is also to define a set of interesting behaviours that can be used either from a robotic stand point or a software stand point later in the master project.

Firstly, let's define what "collective behaviours" truly means. Collective behaviour is a process without central control that brings together multiple participants to achieve some outcome [^20]. Now that we have clearly defined what collective behaviours are let's think of something; Ants are capable of building complex structures, they can defend their nest as a group when a threat knocks to their door and are capable to organise to achieve such tasks. So how is it that such simple being are capable of the greatest thing? This is the question that we will elaborate on in the next sub-chapters.



## 3.1 Organization [NRV]

How do ants organize? Even though ants are simples beings, their collaborative behaviour are extremely complex and close to be on a military level. Each colony more or less have the same structure but it may slightly variate from a species to another. A colony begins with its queen. The queen is not a hierarchal label as she does not have absolute power on what the ant colony is doing but she is the only type of ant that will give birth to young workers. It has been found that some queen may lay up to 1000 eggs a day for up to seven years (a grand total of 2'492'000 eggs). The larvae are the growing workers laid by the queen, and are source of high tension between colonies when an attack occurs as some species like to steal them as food supply or even to use them as new worker in the opponent's colony [^28]. Growing to be adult ant, the larvae will then perform tasks rather than being attributed a role, see Task allocation section.



## 3.2 Communication [NRV] [^33] [^34]

As mentioned already in this paper, ants don't have as complex communication tools as humans do and yet, they are capable to generate collective behaviours in colonies that sometimes contain up to a few ten million individuals. It occurs that ants can communicate through 3 distinct channels; The first one is low resonance sounds, which ants can produce by scraping their legs in some specific part of their body to create different sounds. This communication method is mostly used when deposing pheromone trails would not suit the situation, such as helping a lost ant to find its way back through a tunnel or a narrow set of rocks. The second one is body language which they can use to generate primitive reflex in other ants by touching them in specific areas. Finally, the scent which ants use to detect the pheromone trail left by other ants. As mentioned earlier in this paper, pheromones are unique chemical badge among colonies of ant which serves many purposes. These pheromones can be used for navigation, telling an ant where to find a food supply or a source of water, but also used by the queen to influence the workers. It has been found that some pheromones used by the queen had the effect to calm or to excite the workers in specific situations [^35].



## 3.3 Navigation using pheromone trails [^36] [^37] [^38] [NRV]

The pheromones mentioned in the previous section are mainly used for ants to orientate. Whenever a forager comes back from a food supply leaving behind it a pheromone trail indicating the location of the source, another ant is likely to fall upon it and to follow it, ultimately leading it to the source. If the ant follows the trail is decided given a probabilistic model where the more pheromone there is on a trail (that is, left by multiple other workers), the more likely the ant is to follow it. Some other types of pheromones are also used as repellent as depicted in the Pharaoh ants section of this document. This navigation tool has already been studied a lot and has given birth to many papers and a very interesting algorithm used today to find optimal (shortest/fastest) path for maps and graphs; The ant pathfinder algorithm. 

The ant pathfinder algorithm works as follows: The ants are dispatch randomly from a given starting point to the neighboring edges of the graph, wandering to other edges, replicating foraging behaviors. Once an ant finds the destination node it backtrack to the starting point of the graph leaving behind it the so-called "pheromone trail" indicating where the destination point is. It is very likely that other ants will also find a path, and will be returning to the nest also leaving behind them the trail. Now that we have multiple likely paths, how does one figure which one has the shortest distance? Exactly like ants do. Indeed, as mentioned above, the shorter the path is, the more likely another ant will encounter it and mark it with its pheromone, the higher the level on the trail will be, leading to even more ants following this track and so on (see Figure N). After a few generation, the shortest pheromone trail will be visible as longer trail who suffered from a lack of pheromone have been evaporated.

https://www.researchgate.net/profile/Mohammed_Alhanjouri/publication/264704807/figure/fig5/AS:668858968989698@1536479813110/Ants-use-pheromone-as-indirect-communication-to-build-best-tour_W640.jpg

Figure N depicts the ant pathfinder algorithm in three phases. The first phase is the exploration phase of the algorithm where ants are dispatched randomly on edge of the neighboring nodes of the graphs, eventually finding the destination and coming back to the source. The second phase is the reinforcement phase, the shorter path will be reinforced as more ants will fall upon them. The third phase is the eventual evaporation of the longer path. Note that as seen in phase three and said above, choosing if the ant will be going on a given trail or not follows a probabilistic model, meaning that ants may result in exploring other paths. The longer path being evaporate, the shortest remain and is finally visible.

## 3.4 Task

### 3.4.1 Types of task [NOK]

Tasks may variate slightly from a colony to another, as in leaf cutter ant's colony where some ants have to maintain the fungus garden, but overall we can sum them up in 4 tasks:

- Foraging

- Scouting

- Patrolling

- Nest maintenance

  

#### Scouting [NRV]

Scouting is the action for an ant of going outside alone or with a very limited crew to search for food, one the scout have found a food source it will rush back to the nest (leaving behind it a pheromone trail) to "warn" the colony that supply is available. Scouting can also serve as attack planning, if an ant found a potential threat (that is, an enemy colony) it will go back to its nest to prepare defence if needed.



#### Foraging [NRV]

When foraging, ants will move randomly in many different directions to increase their chance to encounter food or a positive pheromone trail. If the ants ever finds food it will sub-sequently crawl home leaving behind it a pheromone trail indicating the other ants where the food is. As more ants encounter the trail left by our lucky ants, the pheromone trail gets bigger and bigger leading to even more ant finding it. The more appealing the food is (in quantity) the more ant will switch their current task to get to the food area. If the ant fails to return to the colony in time the pheromone trail eventually evaporate and no ant will be able to follow the trail back to the food supply. [^33] Ants also have a system of "memory of high reward foraging sites", the more food there is at a specific site the higher the reward is going to be, leading to the ant returning to this foraging site in the future, given that it is a static site (not a spontaneous drop of supply). [^50] [^53]

#### Patrolling [NRV]

Patrollers are the ants keeping guard of the nest, making sure no threat is near around. Like the scouters, if they even encounter a threat they will rush back to the nest and warn everyone, keeping the nest a safe and sound place.



#### Nest maintenance

Nest maintenance is the widest task an ant can perform, it goes from moving the newly laid eggs from the queen to the eggs chamber, taking care of a fungus garden as for the Pharaoh ants or other ant-fungus like types of ant, making the nest bigger, to cleaning it from dead bodies, food waste and such. Ants who perform such tasks have been found to be older that the one performing off-site task such as foraging and patrolling. This could be explained by their low performance in these tasks due to their older body [^52]. 



### 3.4.2 Task allocation [NRV]

As we have mentioned earlier, there is no central control unit in a colony of ants. This means that there's no one to tell an ant what to do at any given time and yet ants seem to have a pretty busy day-to-day calendar. Few studies have **suggested** that ants can select a task based on their age, their body size, their genetic background, their position in the nest, the way they eat but also by receiving signals from other ants [^22]. Earliest studies have highlighted (**todo** re-find the study**) ants can determine what task it should do with a very clever decision model. This decision is based on the rate at which an ant encounters another one. Indeed, every time an ant makes contact, there is a small probability that the ant will switch to the encountered ant's task. This also means that the more ants with the same task our ant encounters, the more likely it is to switch (note that this decision-making is only based on interaction and not location). Ultimately, larger ant colonies are better at task allocation than smaller ones. Switching to a task is a thing, being aware of what the other ant's task was is another. How is it that an ant knows what task to switch to even though we have stated multiple times in this paper that ants don't have any complex communication tools? It is because ants have been given antennas which they rob against encountered ants' antennas. This contact is what tells the ant the task the other is performing and it does so by analysing the cuticular hydrocarbon the antennas carry. These cuticular hydrocarbons variate regarding where the ant previously was and what task it was performing. For example, when ants are foraging out in the sun, the proportion of n-alkanes in their hydrocarbon profile increases leading the forager to smell recognizably different from an ant that works inside the nest  [^payam study]. Age is also a variable to take into consideration. Even though it has been found that this does not impact task allocation on a large scale, studies have found that older ants would usually take care of the maintenance of the nest and really any task that happens inside the nest, whereas younger workers would more likely be outside to forage and defend the nest in case of attack. Deborah M. Gordon, a world wide known scientist famous for her lifetime studies on ants, has discovered that not every ant would switch to a certain task even though the probability is high. She discovered that ants have "preferences" to which task they would be willing to switch to and she has then dressed a map of this behaviour:

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/ant_task_switching.png?raw=tru" alt="alt text" title="" style="zoom:100%;" />

This map shows that only in-nest ants (the older or/and inactive ants) would switch to nest maintenance if the demand was high in more important tasks such as foraging and that the highest task priority is foraging as every ant can eventually ending in switching up their task to become a forager. 



### 3.4.3 Environmental challenges [NRV]

The way ants choose what to do is also environment-based as there's a notion of operating cost of tasks that an ant takes into consideration when performing a task. Indeed, In some places in the world such as deserts or highly dry terrains, the operating cost of task is very high as finding resources is hard. This means that an ant will think twice before allocating some of its time scouting for food outside as it only does it if the returned income is higher than the one spent to get to the supply. This high operating cost behaviour can be summed up as "Don't go unless something positive happens". In some other places of the world the operating cost is low (houses, groceries, but also tropical forest), meaning that the energy an ant has to spend to reach a resource is little in comparison to the income it will return. This is the "Go unless something bad happens" behaviour [^29]. Such studies have also been conducted in human threatening environment such as space, where a small colony was filmed to study these behaviours. The study has shown that ant wouldn't move unless the colony's existence was at stake [^30].



## 3.5 Lifecycle of an ant colony [^51] [^32]

Ant colonies are part of an endless cycle in which one colony will give birth to some others which will then also give birth to some others. The only way a colony could come to its extinction is if a natural or human catastrophe wipes them down. The same way humans give birth to a descendent tree, the ants will give birth to "child" colonies and even "grand child colonies" where chemical badge between generation only variate from a few degree. [find ted talk with Deborah where she talks about that]

To give birth to a new colony, the original colony must first come to a certain level of maturity where the winged male will eventually fly out to mate with winged female (and die from this process).  The newly proclaimed queen then dig a hole and lay her first eggs, feeding them from her body fat reserve. The queen will use the sperm from the very first time she mated with males and will keep it to lay eggs for the rest of her life (up to 15-20 years). 



# 4. Simulation [NRV]

This section is a go through many behaviors we have seen throughout this paper and how they could be use to create a simulator. We will travers ways of creating such simulations both on the software side, with the study of languages, technics and framework, and on the robotic side with a more pragmatic approach and definition of needs and environmental restrictions to replicate a limited pre-defined set of collective behaviour.



## 4.1 Software [NRV]

### 4.1.1 Relevant collective behaviours

The collective behaviors that one can include in a simulator are countless and the only limits are today's computer power. Having this much freedom means the simulation can include almost everything as long as it remains coherent. There are two main categories of behaviors, internal, and external. We will define external behavior as behavior triggered by external sources such as the temperature or the time of the day, and internal behavior are the one directly induced by ant collectiveness. It is good to keep in mind that the development of an agent has to remain as simple as possible and self-centered (an ant hardly knows its outside world) as it is in real life. Individuals are simple, collectivity is where complex behaviors emerge.



#### External

Throughout the section "The ant kingdom" we have seen that many behaviour was directly linked to the outside environment of ant life. We have been talking about the operating cost of task which introduces a notion of time and environmental condition to the simulation. That being said, the following are possible behavior to implement in the simulation. There exists more but this is a good start.

- Time (Seasons, days)
- Environmental conditions (temperature, humidity?)
- Operating cost of a task



#### Internal

The section "Ants behaviors and mechanisms" has shown us how complex simple mechanisms can become when applied to the colony. We have been through the way ants communicate and navigate but also through the different tasks the colony has to perform and how they are allocated to individuals. The following tasks are possible behaviors and mechanisms to implement in the simulation.

- Task (Foraging, nest maintenance, ..) & Task allocation
- Queen's control over the colony 
- Pheromones
- Food and resources management
- Breeding and population growth

We also discussed more species-dependent behavior such as the Nomadic and Stationary phase of the army ant colonies or the satellite nest of the carpenter ant colonies, which would be interesting to pick, out of many others. 



#### Minor [NOK], while re-reading the document it would be nice to put more in this and the two above

Other mechanisms will be considered as minor as they will not affect the simulation as deep as the external or internal would. These are the one with the least priority and include 

- Ant body degradation

  Which affects how well an ant can perform a task

- Types of ant

  As it will be more important do define a set of task than a hierarchy and organisation



To conclude this brief definition of possibilities it is important to keep in mind that an infinite amount of behavior could be implemented but it would only make the development even more complex. The simulation has to be agent-based and the internal mechanisms are the most important to develop as they are the core of what defines an ant. However, externals mechanisms are also important to implement as they will show their influence on internal mechanisms and are not to be disregarded. Appendix 8.1 is an abstract implementation model of all the above behavior and mechanisms which can be used to develop the simulation and gives a wider perspective of the overall possible implementation.



### 4.1.2 Exploration of simulator, languages and drawing frameworks [NRV] 

Many technics can be used to build a good simulator, and yet, it is difficult for one to select the best within the ocean of languages and framework that exists as they each usually fit specifics kinds of implementation. This chapter is a deep through of some of the most relevant ones, we will go deeper on the understanding of a good drawing tool in the specific case of the ant simulation and this will also be the occasion to have a first sight at the overall software implementation.

The first step before plunging into google and look at every language and framework that exists is to specify the needs. As we have not yet a good understanding of the complexity of the simulation (this problem will arise at a later, deeper phase), one needs to think on a more abstract level. Figure [^N] is a first very simple high-level not to scaled representation of an ongoing epoch in the simulator. Firstly, we need to be able to draw. This might sounds a bit too abstract but it already narrows down the scope as many languages such as C or C++ are low-level language, which would only add more complexity to the project (don't get me wrong, one can use these languages to draw, but there are a lot of easier ways to do it with higher-level languages). Server side languages like PHP, which depends on client side action to be able to draw, are also out of the basket. Secondly we will need to draw very simple shapes (mainly pixel alike) in a large quantity Thirdly We don't need to perform a lot of complex mathematical operations (such as integration, derivative, or trigonometry), as the agents will be evolving in a 2D plan. Finally, it is very likely that threads will be useful in the simulation (controlling the time, nests and such), so we need a language where using these is more or less easy. This conclude a first good definition of preliminary needs.

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/sim1.png?raw=tru" alt="alt text" title="simulation rep 1" style="zoom:100%;" />

Given that I do not master every languages that exist and since this project is not about the discovering and use of a new language, this narrows down the scope even more. In the above section we got rid of the low-level languages and the server-side ones since they would only add more complexity in an already quite complex task. This leaves me with Javascript, Python and Java, three interesting candidates. From there, it is more of a personal choice than an actual language to language comparison. Each of these three languages implement drawing technics and can perform all of the above described needs. I will nonetheless explain the advantages and inconveniences of each, based on my personal experiences and knowledges acquired throughout my developer’s life. 

 Let’s start with Python. Python is a very light and high-level language and is surprisingly simple and satisfying to work with. Being non-typed and almost “Human language” alike makes it a very appealing language to choose. It has good support of threads and includes some powerful (yet, unknown to me) drawing frameworks such as PyGame or Arcade. Python almost look like the perfect candidate. However, it is the slowest of the three at “Calculation steps per seconds” (as shown in Figure N), which is highly important when one needs to create a simulation as it will defined how much item can the program handle at a given time T. That being said, Python remain quite an interesting candidate, but ultimately not the one which will be used for the simulation. Secondly, Java. It is broadly known and can be used for more or less everything, which makes it one of the most documented language in the market. It already implements a lot of structure, function, drawing technics and basic graphic tools because it has been designed to be a somewhat higher-level version of C with oriented object programming. It uses the JVM (Java Virtual Machine) to run the Java compiled bytecode which adds a lot of overhead at the start compared to interpreted languages (but it saves you from dummy mistakes). It however has the highest “Calculation steps per second” score compared to the two others as Figure N demonstrates it. All of that being said, Java would almost be the perfect candidates. The only downside one could really think of is the lack of “good” drawing frameworks. It becomes quickly frustrating to work with drawing and threading in Java (but this is highly personal). Finally Javascript. Javascript is the kind of candidate who is a clever mixt between the advantages of Java and Python. It has a good “Calculation steps per second” score, it is easy to use and it is web based which makes it easy to distribute on multiple platform. It has a good community and support a lot of user-made libraries, plus, its documentation is also very great (as Python and Java). It has a very good vanilla drawing libraries and very good drawing frameworks such as Preprocess, ThreeJS or WebGL which can be used on top of VanillaJS and offer a wide variety of tools and a large range of possibilities. This language and its framework are used for a lot of physics simulation such as liquid simulation [^48] or even planetary orbit simulation [^49]. The only thing one could reproach to Javascript is its lack of coherence in the way it has been built (a short video about how incoherent Javascript is: https://archive.org/details/wat_destroyallsoftware), but this is not going to be a problem for the development of the simulation.

In conclusion there is not a top of the list language as they all have their advantages and weaknesses but it is very likely that Javascript is going to be used over Python and Java as it is the most straight forward and flexible of the three, with its large variety of open-source libraries and its great documentation.



<img src="https://2.bp.blogspot.com/-BcemgfpuSvQ/UfCyESwcPKI/AAAAAAAAA9Q/a2qKDpvmZN8/s1600/LatticeBoltzmannPerformanceGraph.png" alt="alt text" title="simulation rep 1" style="zoom:70%;" />

 

## 4.2 Robot simulation

This section is about describing and defining a limited set of collective behaviours which can be taken from ants and transposed to real life robot condition and environment. This set of collective behaviour is purely arbitrary and can always be disregarded. We will also go through the definition of swarm in robotic and describe what are the requirements and limitations to implement such behaviours in real life. [^46]

Swarm robotic is the art of collectively run a lot of robots to solve problems by forming complex structures and behaviors such as the one observed in nature. They are scalable systems made of simple, often homogeneous agents. As in ant or bee colonies, swarm robotic does not have any main control unit, meaning that each agent knows what to do and where to go by communicating with nearby individual. 

<img src="https://roboticsandautomationnews.com/wp-content/uploads/2020/04/swarm-robotics-1.jpg" alt="alt text" title="simulation rep 1" style="zoom:70%;" />

Figure N shows small agent named "KiloBots" created by the Harvard University. By vibrating legs with a motor, these tiny robots are capable of horizontal, vertical and diagonal. They are equipped with transmitters and receivers and light detector, allowing them to perform complex task such as arranging themselves in complex shape structures or follow light sources to replicate low level swarm behaviours.

### 4.2.1 Relevant collective behaviours [NOK]

Where in the software simulation almost everything is possible since it is computer-generated, the real-life setup restrains our field of possibilities. The cost of the setup is also to take into consideration as the budget is not and never unlimited.  There are also some out-of-the-box problems such as recharging the robot's battery every time it runs off of power, which leads to losing time for the actual real life simulation. Fear of battery loose also means that the robot cannot venture as far he wants, and is limited in what kind of modules (sensors, motors, actuators,..) it adopts. Space and time are also concerns as the setup in which the agents will be moving will not be as large as in a software simulation. Indeed, such setup usually takes place at home or at school where only a few squared meters are given. Time is also a variable because one cannot imagine speeding up the real world to see the results more quickly (or at least this is not yet possible at the time this paper is written). The last bit of thing to keep in mind is the hardware problem. Indeed, when you write software the only problem there is usually stands between the seat and the screen (you), which means you cannot blame your computer if something does not work as expected. But in real life when dealing with hardware, many problems can occur such as loss of power leading to less energy in the wheel and strange behavior, unexpected sensor feedback because of the current environment, in-accuracy in robot's movement, and way more. Few more of these problems are discussed in a paper written in 2013 by Madhav Patil, Tamer Abukhalil, and Tarek Sobh, see ref. [^47]

Having so many limitations also means that the collective behaviors one can simulate are somewhat limited. Nevertheless, there is three collective behavior that stands out as they are quite complex, interesting to implement, and answer modern and real-life questions and concerns:

- Task allocation
- Operating cost of a task
- Pathfinders with Pheromone trails.

Task allocation is interesting because it is a modern problem. Indeed, if swarm robotic is tomorrow's future we will need to precisely be able to tell an agent what its task is, or more precisely, it will have to decide itself what task to do. Imagine building a bridge with the help of a robotic swarm to counter a flood in a small village, each agent composing the safety bridge needs to be able to know what location to go to. This task allocation will work as described in the section (SECIONT N) where an agent decides to switch to another task based on a probabilistic model after encountering one of its kind. The operating cost of a task could be defined as a subsection of task allocation or as a variable. What will be the cost for an agent to move at a given area? Will it have enough battery to perform the task anyway or is he even capable of enduring the journey? Operating cost of tasks coupled with task allocations will answer these questions. Finally, even though pathfinder already is a widely studied topic, it is still interesting to include a pathfinder algorithm as it's how an ant ultimately decides to move. If the simulation gets too complex it could be imagined to invent a less complex way of movement, such as random or based on a specific probabilistic distribution.



### 4.2.2 Robot implementation

As for the software implementation, we will define a set of features the physical robot needs to complete the tasks. A set of features can go from wheels, motors, or even wings to the many types of sensors a robot can be equipped of. This way, we will be able to define what type of robot should be used and how the task could be implemented. The first need is a brain, even though ants are simple beings we still need to be able to send information to the different parts of the robot and control them. This brain can be simulated with a Raspberry Pi (which in short, is a small computer) or a robot that already contains a motherboard and a control unit. Secondly, a communication system will be useful to share the robot's chemical badge to another one as to imitate the transfer of information when ants touch antennas, which will make possible to do "task allocations" by sharing pieces of information on the currently performed task. Thirdly, we need a way to simulate movement, and since ants are not flying insects (unless they are winged males or females) wheels is the easiest way to replicate their movement. Fourthly, it would be nice if our ant robots wouldn't collide every time they run onto each other, and to do that the robot will have to be equipped with proximity sensors, probably at the front to avoid a collision. Finally, we need to simulate the pheromone trails in some way and it is likely going to be the biggest challenge because the robots are not yet capable of "sensing" odor as ants or humans do or they do it in a very limited fashion.

A study from 2014 made by Ryusuke Fujisawa, Shigeto Dobota, Ken Sugawara, and Fumitoshi Matsuno [^39] demonstrates the complexity of such an implementation, where the robots were capable of diffusing ethanol on the ground for the other robots to sense, using an alcohol sensor which detects the proportions of alcohol gas in the air. The main problem of such a solution is that it considerably raises the complexity of the build as to depose alcohol on the ground the robot requires to have a tank (which serves as a container for the ethanol), a pump, and a diffuser.  This three component will have to be implemented on as many robot as needed to simulate the defined behaviour, which also raise the cost and the maintenance complexity of the task. Even though this solution is quite complex it still fits the swarm robotic definition of having no central unit. Some other ways of doing it would be to know the position of the robot in the given space. Imagine if we keep a map of where the robot went and go, we are then able to tell whether it goes on a trail left by another robot and vice versa. This solution is good because it only requires a pre-defined space with no obstacle (to avoid complexity in the execution) but totally defeats the idea of swarm robotic as we constantly need to tell the robots where they are and if they are currently on a pheromone trail,  which involve a central unit. Nevertheless, this position system could also resolve the "high and low" operating cost of task simulation as if we define areas in our map as being high or low cost then it is easier to tell the robot whether or not the task is worth the shot. There are many ways to localize a robot in a given space and we will go through 2 of these methods that can potentially be used for our implementation. 

The first way would be to use SLAM (Simultaneous Localisation And Mapping) which according to Wikipedia is "the computational problem of constructing or updating a map of an unknown environment while simultaneously keeping track of an agent's location within it"  [^43]. This localization method has been used in many modern problems such as the localization of autonomous vehicles [^42] or the localization of indoor vacuum robots [^44]. To localize the position of the robot in a given space one could use a range or an optical sensor, such as a Lidar, on top of the robot. Coupled with a localization algorithm such as the Markov localization algorithm [^41] we can precisely tell the robot's position on the map. This solution is great because it is somewhat easy to implement, requires less material than the ethanol diffuser solution, and one can change the computing cost of the localization to fit the computing power of the brain by using fewer samples in the algorithm. *However, this solution is only that good when one robot is present on the map as other robots could add undesirable noise in the optical/range sensors.* A second way would be to equip each robot with Bluetooth transmitters and receiver to perform triangulation as it is done nowadays to approximate our position in space with systems such as the Global Positioning System (GPS) or the Galileo Positioning System (Galileo). Triangulation works by collecting the distance of the subject from at least three receiver/transmitter towers and using a function to approximate its position. In 2013, a team of 5 researchers (Yapeng Wang, Xu Yang, Yutian Zhao, Yue Liu, L. Cuthbert) [^40] had conduct experiments for such technics and had concluded that the accuracy was good. This solution works better than the two others as it requires less computing power at a given time T and does not lose accuracy if other robots are present nearby

Another way of simulating these pheromone trails would be to use other robots acting as beacon and forming a path to a food supply. If a few of these robots are placed in a grid like manner one can imagine that our robotic ant could navigate in this grid constantly communicating with these beacons. These beacons would keep a state of how many times it has been contacted by an ant, incrementing the "pheromone trail" and also give to the ant a sense of how much pheromone there are in that area (allowing pathfinders and operating cost of task implementation).

This definition of needs yields that the robot has to be equipped with a "brain" (a control unit), wheels, proximity sensors, and either an optical/range sensors - Bluetooth transmitter and receiver, or a pump and diffuser system to sense and spread, to simulate the fake pheromone trails. The wheels and the proximity sensors can easily be achieved by using a Thymio-II robot [^45] which is a pre-built ready-to-use robot equipped with many features. Thymio-II also comes with a built-in central unit but its capacities are rather limited, thus the use of an external central unit such as a RaspberryPi is required. Using a RaspberryPi will also make easier the addition of new module and sensors. Whether it is choose to simulate the pheromone trail with the localization or with the alcohol sensors does not put at risk the choice of using Thymio-II. Indeed, one can easily build a structure on top of the Thymio-II (see Figure N), which can support both options. In the case of using beacons arranged in a grid-like manner, the implementation will require enough of them to accurately simulate a path from at least a source (the nest) and a few destination (it could be either food supply, task areas, high or low cost areas).

[PIC of our robot with the liar]

# 6. Conclusion [TODO]

Ant is a very special species... with more than nnn individuals and xxx species ...

The study of the living things mechanisms is called biomimetic. This art of replicating what nature does has enabled us to ....

# 7. References

[^0 ]: [Biomimetic design: 10 examples of nature inspiring technology, Gertie Goddard, N/A](https://www.sciencefocus.com/future-technology/biomimetic-design-10-examples-of-nature-inspiring-technology/)
[^1]: [Phylogeny of the Ants: Diversification in the Age of Angiosperms, C. Moreau, C.D. Bell, R. Vila, S.B. Archibald, N. Pierce,2005](https://www.semanticscholar.org/paper/Phylogeny-of-the-Ants%3A-Diversification-in-the-Age-Moreau-Bell/1569e0be3c39d14086d5f61e94bb7fed55e2f6e4?p2df)
[^2]: [Ancient Ants Arose 140-168 Million Years Ago; Insects Needed Flowering Plants To Flourish, National Science Foundation, 2006](https://www.sciencedaily.com/releases/2006/04/060407144825.htm)
[^3]: [Why is eusociality an almost exclusively terrestrial phenomenon?, Graeme D. Ruxton, Stuart Humphries, Lesley J. Morrell, David M. Wilkilson, 2014](https://besjournals.onlinelibrary.wiley.com/doi/full/10.1111/1365-2656.12251)
[^4]: [Ant Ecology, Lori Lach, Catherine Parr, Kirsti Abbott, 2010](https://books.google.de/books?hl=de&lr=&id=vlwVDAAAQBAJ&oi=fnd&pg=PR5&dq=10,000+trillion+ants&ots=aUqWFkzcGi&sig=Jhxc-cjuCLNaBqW7mf3kRWFJcZA#v=onepage&q=10%2C000trillion&f=false)
[^5]: [In search of ant ancestors, Ted R. Schultz, 2000](https://www.pnas.org/content/97/26/14028.full)
[^6]: [Why Ants Rule the World, Corey Binns, 2006](https://www.livescience.com/747-ants-rule-world.html)
[^7]: [The Remarkable Self-Organization of Ants, Emily Singer,2014](https://www.quantamagazine.org/ants-build-complex-structures-with-a-few-simple-rules-20140409/)
[^8]: [Army ant, N/A ,2008](http://www.newworldencyclopedia.org/entry/Army_ant)
[^9]: [Deadly Army Ants Decimate Entire Ecosystems, Amanda Ellis, 2018](https://roaring.earth/deadly-army-ants/)
[^10]: [Wikipedia, Army ants](https://en.wikipedia.org/wiki/Army_ant)
[^11]: [How Ants Wage War, Marco Werman, 2011](https://www.pri.org/stories/2011-11-16/how-ants-wage-war)
[^12]: [Wikipedia, Carpenter ant](https://en.wikipedia.org/wiki/Carpenter_ant#Behavior_and_ecology)
[^13]: [Wikipedia, Leaf cutter ant](https://en.wikipedia.org/wiki/Leafcutter_ant)
[^14]: [Carpenter Ants, College of agriculture, food and environment, 1997](https://entomology.ca.uky.edu/ef603#:~:text=Carpenter%20ants%20actually%20construct%20two,queen%2C%20eggs%20or%20young%20larvae)
[^15]: [Waste management in leaf-cutting ants, A. N. M. Bot, C. R. Currie, Adam G. Hart, Jacobus J Boomsma, 2001](https://www.researchgate.net/publication/248373454_Waste_management_in_leaf-cutting_ants)
[^16]: [Pharaoh Ants: Interesting Facts About Pharaoh Ants, Will David, 2020](https://pestclue.com/pharaoh-ants-interesting-facts-about-pharaoh-ants/)
[^17]: [Wikipedia, Pharaoh ants](https://en.wikipedia.org/wiki/Pharaoh_ant)
[^18]: [Leafcutter ants are in a chemical arms race against a behaviour-changing fungus, Sarah Worsley, 2018](https://theconversation.com/leafcutter-ants-are-in-a-chemical-arms-race-against-a-behaviour-changing-fungus-97892)
[^19]: [Longevity and detection of persistent foraging trails in Pharaoh's ants, Monomorium pharaonis (L.), Ducan E Jackson, Stephen J. Martin, M. Holcombe, Francis L.W. Ratnieks, 2006](https://www.researchgate.net/publication/222404029_Longevity_and_detection_of_persistent_foraging_trails_in_Pharaoh's_ants_Monomorium_pharaonis_L)
[^20]: [The Evolution of the Algorithms for Collective Behavior, Deborah M. Gordon, 2016](https://www.cell.com/fulltext/S2405-4712(16)30332-5#:~:text=Collective%20behavior%20is%20the%20outcome%20of%20a%20network%20of%20local%20interactions.&text=I%20suggest%20that%20a%20focus,collective%20behavior%20of%20cellular%20systems.)
[^21]: [HOW DO ANTS KNOW HOW TO FIND THEIR WAY HOME?, Gryphon Adams, N/A](https://animals.mom.com/rol861.html)
[^22]: [Task allocation in Ant Colonies, Alejandro Cornejo, Anna Dornhaus, Nancy Lynch, Radhika Negpal, N/A](http://people.cs.georgetown.edu/~cnewport/teaching/cosc844-spring17/pubs/ants-task.pdf)
[^23]: [Army Ant, Michael D. Breed, Janice Moore, 2016](https://www.sciencedirect.com/topics/agricultural-and-biological-sciences/army-ant) -> **to name**
[^24]: [Inside the Amazon Warehouse Where Humans and Machines Become One, Matt Simon, 2019](https://www.wired.com/story/amazon-warehouse-robots/)
[^25]: [HOW HONEY BEES HELPED THE INTERNET, Pacific standard staff, 2017](https://psmag.com/news/how-honey-bees-helped-the-internet)
[^26 ]: [Six weeks in the life of a reproducing army ant colony: Male parentage and colony behaviour, D. J. C. Kronaeur, E. R. Rodríguez Ponce, John Lattke, Jacobus J Boomsma, 2007](https://www.researchgate.net/publication/225763258_Six_weeks_in_the_life_of_a_reproducing_army_ant_colony_Male_parentage_and_colony_behaviour)
[^27]: [A Mesozoic Clown Beetle Myrmecophile (Coleoptera: Histeridae), Yu-Lingzi Zhou, Adam Slipinski, Ren Dong, Joseph Parker, 2019](https://www.researchgate.net/publication/332447535_A_Mesozoic_Clown_Beetle_Myrmecophile_Coleoptera_Histeridae)
[^28 ]: [Kidnapper Ants Steal Other Ants' Babies - And Brainwash Them, Josh Cassidy, 2019](https://www.kqed.org/science/1947369/kidnapper-ants-steal-other-ants-babies-and-brainwash-them)

[^29]:  [Task switching is associated with temporal delays in *Temnothorax rugatulus* ants, Behav Ecol, 2017](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5255904/)
[^30]: [All Together Now—A Lesson from Space Station “Ant-stronauts”, Jessica Nimon,2014](https://www.nasa.gov/mission_pages/station/research/news/ants_in_space/)
[^32]: [Plasticity of Daily Behavioral Rhythms in Foragers and Nurses of the Ant *Camponotus rufipes*: Influence of Social Context and Feeding Times, PLoS One, 2017](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5242425/)
[^33]: [Communication in ants, Duncan E. Jackson, Francis L.W. Ratnieks, 2006](https://www.cell.com/current-biology/comments/S0960-9822(06)01834-3)
[^34]: [How ants communicate, Antkeepers, 2020](https://www.antkeepers.com/facts/ants/communication/)
[^35]: Journal of the Kansas Entomological Society, H.G. Fowler, R. B. Roberts , 1982
[^36]: [Finding Optimal Paths on Terrain Maps using Ant Colony Algorithm, Vinary Wishiwal, Mano Yadav, K. V. Arya, 2010](https://www.researchgate.net/publication/272912654_Finding_Optimal_Paths_on_Terrain_Maps_using_Ant_Colony_Algorithm)
[^37]: [Wikipedia, Ant colony optimization algorithms](https://en.wikipedia.org/wiki/Ant_colony_optimization_algorithms)

[^38]:  [Decoding the Remarkable Algorithms of Ants, Emily Singer, 2015](https://www.quantamagazine.org/decoding-the-remarkable-algorithms-of-ants-20150625/) 
[^39]: [Designing pheromone communication in swarm robotics: Group foraging behavior mediated by chemical substance, Ryusuke Fujisawa, Shigeto Dobota, Ken Sugawara, Fumitoshi Matsuno, 2014](https://www.researchgate.net/publication/265053113_Designing_pheromone_communication_in_swarm_robotics_Group_foraging_behavior_mediated_by_chemical_substance)
[^40]: [Bluetooth positioning using RSSI and triangulation methods, Yapeng Wang, Xu Yang, Yutian Zhao, Yue Liu, L. Cuthbert, 2013](https://www.researchgate.net/publication/261056426_Bluetooth_positioning_using_RSSI_and_triangulation_methods)
[^41]: [Understanding Markov Localization, Sakshi Kakde, 2019](https://medium.com/@kakdesakshi/understanding-markovs-localisation-86aabe1549d4)
[^42]: [Simultaneous Localization And Mapping: A Survey of Current Trends in Autonomous Driving, Guillaume Bresson, Zayed Alsayed, Li Yu, Sébastien Glaser, 2017](https://hal.archives-ouvertes.fr/hal-01615897/file/2017-simultaneous_localization_and_mapping_a_survey_of_current_trends_in_autonomous_driving.pdf)
[^43]: [Wikipedia, Simultaneous localization and mapping](https://en.wikipedia.org/wiki/Simultaneous_localization_and_mapping)
[^44]: [A Light-and-Fast SLAM Algorithm for Robots in Indoor Environments Using Line Segment Map, Bor-Woei Kuo, Hsun-Hao Chang, Yung-Chang Chen, Shi-Yu Huang, 2011](https://www.hindawi.com/journals/jr/2011/257852/)
[^45]: [Thymio official website](https://www.thymio.org/)

[^46]:  [Swarm Robotic Behaviors and Current Applications, Front. Robot. Al, 2020](https://www.frontiersin.org/articles/10.3389/frobt.2020.00036/full)
[^47]: [Hardware Architecture Review of Swarm Robotics System: Self-Reconfigurability, Self-Reassembly, and Self-Replication, Madhav Patil, Tamer Abukhalil, Tarek Sobh, 2013 ](https://www.researchgate.net/publication/256459816_Hardware_Architecture_Review_of_Swarm_Robotics_System_Self-Reconfigurability_Self-Reassembly_and_Self-Replication)

[^48]: [Paveldogreat on Github, WebGL Fluid Simulation](https://paveldogreat.github.io/WebGL-Fluid-Simulation/)
[^49]: [Implementing 2D Physics in JavaScript, Towards Science, Martin Heinz, 2020](https://towardsdatascience.com/implementing-2d-physics-in-javascript-860a7b152785)
[^50]: [Acquisition and expression of memories of distance and direction in navigating wood ants, A. Sofia D. Fernandes, Andrew Philippides, Tom S. Collett, Jeremy E. Niven, 2015](https://jeb.biologists.org/content/218/22/3580)

[^51]: [Inside an ant colony, Deborah M. Gordon, 2014](https://www.youtube.com/watch?v=vG-QZOTc5_Q&list=PLDuI-3qLEl1NP5IOwTyESncjHCY6BvdZU&index=16&t=0s&app=desktop)
[^52]: [Deborah Gordon: The emergent genius of ant colonies, Deborah M. Gordon, 2008](https://www.youtube.com/watch?v=ukS4UjCauUs&ab_channel=TED)
[^53]: [Ant Colonies Have Memories That Their Individual Members Don’t Have, Deborah M. Gordon, 2019](http://humana.social/ant-colonies-have-memories-that-their-individual-members-dont-have/)

Pics:

- http://dvschroeder.blogspot.com/2013/07/java-vs-javascript-vs-python.html
- https://bugoftheweek.squarespace.com/blog/2016/1/13/carpenter-ants-here-and-there-icamponotusi-spp -> carpenter ant pic
- https://tucson.com/controlling-leaf-cutting-ants/article_5c0f3482-89a3-11e6-ae65-8fe8c1dbd57d.html -> leaf cutter pic
- https://pestclue.com/pharaoh-ants-interesting-facts-about-pharaoh-ants/ -> pharaoh ants pic
- https://asia.nikkei.com/Business/Companies/Japan-s-fastest-bullet-train-to-squeeze-out-trip-every-5-minutes2 -> Japanese bullet train picture
- https://roboticsandautomationnews.com/2020/04/22/swarm-theory-lessons-from-nature-in-the-advancement-of-robotics/31878/ -> swarm robotic Harvard

# 8. Appendix

## 8.1 Abstract model of the software simulation

The following piece of code is an abstract implementation of the possible software simulation.

```javascript
World {
	var is_day // for visual only
  var temperature, day, season, time, speed, is_paused
  var global_population_increase_rate, global_population, noise_operation_magnitude
  var operating_cost // -> might be infered by above variable.
  var zoom //?? might be useful to scale every pixel

  Nest nests[]
	Terrain terrain
	...
}

Terrain {
	var width, height
	Pixel map[width][height]
	...
}

Pixel {
	var height
	var type // Nest, food, ...
  var label[^{
    colony : '',
    magnitude : int // Every time an ant of the colony walks on a pixel with its same chemical label, increase magnitude by a pre-defined offset.
  }] // Chemical left by ant, if exists.
	...
}
  
Task {
  var id, description
  ...
  operating_cost(this): cost // Is a task a high operating cost or a low operating cost?
}

Nest {
  var origin // pos(x,y) of the very first pixel of the nest
	var surface, health, population_increase_rate
    
	Resource resources[{
		var	food_supply,
    var water,
    var ?
  }]

	var nb_eggs
	
	Colony colony
	...
}

Resource {
	var type
  var ?
  var quality // influence in task allocation
  ...
}

// Colony of ants
Colony {
	var label // refers to the chemical attributes
	var population_size // nb of ants
	Queen queens[] // One or many queens
	Worker workers[]
	...
}

Ant {
    var type, health, size, speed, has_task, current_task, age, max_age
    var strenght // hit
		var walk_randomness // To what extend the ant walks straight
  	var x, y // its position in the terrain
    ...
}

Queen extends Ant {
  ...
}

Worker extends Ant {
	...
}

... extends Ant {
	...
}

// Some way of implementing a brain control
Brain {
    Behaviour behaviours
    /* An ant does not have rules, it only follows strict behaviours */
}

Behaviour {
  ...
}

Rule {
	var starving_cost? // one could imagine to have a dedicated class filled with such
  var food_distribution? // how is food distributes on the map
    ...
}
  
function war_cost() {
  /* Based on energy, nest.population_size and such, fitness function that tells an ant if the war is 		worth fighting for */
}
```

