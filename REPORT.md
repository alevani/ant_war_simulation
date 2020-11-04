```
NOK = Not Ok 

MOK = More or less ok

OK = Done.

NRV = Need revision (grammar - spelling - content)

[Nothing] = Actually not ok but I was just too lazy to write [NOK] or [MOK]
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



## 1.1 State of art [^NOK]

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

# 2. The ant kingdom [NRV]

This section is about ants. Their history, their birth, their life, but also how they function and behave in groups and individually. As we are restrained in time and space, we will talk about only a very few of the enormous amount of interesting species that exist out there. The end goal is to give ourselves an Idea of which ant species are good candidates for a simulation and why they are but also to highlights very interesting biological behaviors that emerge within each species. At the end of the section, some of these biological behaviors will be chosen, based on preferences and interests, to be used later for the simulation. 



## 2.1 Ants

Ants are ancient beings that emerge around 140 to 168 million years ago, even though they started to diversify only about some 60 million years after [^1] [^2]. From the dinosaur era to the Human realm, no kingdom has ever been as large and as powerful compared to the ants super-kingdom. They are estimated to be about 10'000'000'000'000'000 (10'000 trillion) individuals [^4], which account for 20% of the total animal biomass [^3] [^5]. This superkingdom, however, is far from being an unified and coherent heaven. From the 16'000 classified species and the 20'000 estimated species [^2], rare are the ant species that resemble one another. Indeed, from the very early age of their existence, ants have been evolving and adapting to a large amount of environment. They now come in a large variety of colors, from yellow to black. They live in every environment, from extreme heat desert to rainy forests and swamps. The only places that remain untouched (almost) are cold and high places on earth, as ants need a heat source to survive [^6]. Individually, ants cannot do much, they are too simple and their brain is only capable to perform a limited set of action. To become what ants are today, they needed something fundamentally important: Collaboration. It is like the human race. We, throughout the years, had to come up with some very complex collaboration tools and framework to construct the society we have nowadays. 

Throughout this collaboration ants are capable of achieving the greatest. They can assemble themselves into complex structure such as bridge or boat to overcome environmental challenges, they achieve agriculture through foraging and maintenance, and have complex symbiotic relationships[^7]. However, this collaborative behaviour only emerges within ants of the same colonies (and sometimes, but less likely, of the same species). Ant colonies are more likely to fight or avoid contact than discuss peacefully about what would be the best strategy to get the piece of bread from a picnic and how it would be beneficial for each of them. So what is the difference? What makes them less able to collaborate than humans? As said earlier, they have a very limited brain and understanding of the world. They have eyes and they can see, but they can distinguish between dark and light, but that's it. At their level everything but the colony and the queen survival is meaningless. They don't have complex communication tools and only recognise "friend" ant if they carry the same chemical badge. Ants do not live a happy life, and their main purpose is only to fulfil the colony's needs. 

## 2.2 Interesting species

Throughout this sub-section, we will talk about a few ant species that stands out within the 12000 others. Going trough the Army Ants first as they will be the once used for the simulation because they deliver the most interesting collective behaviour, to 4 other types of ants that are also interesting to mention and from which we are going to highlight a few biological behaviors: Carpenter ants, Leafcutter ants,  and Pharaoh ants are among the most known species of ants. This because they mostly exist in an environment close to humans and thus are more inclined to have interaction with our society.

### 2.2.1 The army ants (*Marabunta*)

From all the known ants species, there is a category of ant legitimately called "the army ants". This category that the evolutionary tree has brought to be combatants, are dreadful warriors among the ground. They have been given large mandibles, painful sting and armour, and it exists about 200 species of them [^8]. If two colonies or species encounter one another in the nature, it is unlikely that they will fight against each other. Indeed, this makes sense from an evolutionary stand points as throughout time army ants that were attacking other army ants eradicate themselves to extinction [^11]. They don't have a nest, they rather like to crawl on the ground in a very long and narrow group, consuming up to 500'000 prey animals each day [^9][^27]. The behaviour of crawling on the ground is something specific to the army ants called the "Army ant syndrome" [^10] (see Figure N). This syndrome is a two phase life style cycle that army ants have adopt to .. ?. 

In the first two to three weeks long phase called the stationary phase, the prey that were previously used to feed to the larvae are now reserved to the queen for her to prepare her birth cycle. The queen they lays her eggs and reaching the end of the stationary phase, the new born larvae emerge from their cocoons as the colony prepares itself to enter the second phase. [^9] 

The second phase called the "Nomadic phase" last approximately 15 days, which gives the time for the new born larvae to develop into fully functional workers. In this phase, the colony moves during the day, etching on the ground and capturing everything they can, from insects, spiders and even dead ant bodies. Usually an ant colony would send one or few scouts to look around the colony and seek for food or threats, but the army ants are leaderless group of foragers and like to overwhelm the prey at once sending by sending a lot of them. At the end of the 15 days, the larvae no longer require food and the colony can enter the stationary phase again. [^9] [^26]

<img src="https://ars.els-cdn.com/content/image/3-s2.0-B9780128015322000143-f14-29-9780128015322.jpg?_" alt="alt text" title="simulation rep 1" style="zoom:100%;" />



### 2.2.2 Carpenter ants (*Camponotus spp*)

<img src="https://images.squarespace-cdn.com/content/v1/502d2cede4b0ab396711e089/1452718051897-X50TNDX2FA0ZPGLV2R8R/ke17ZwdGBToddI8pDm48kPm4n540DuKLRMJEMZqwAkMUqsxRUqqbr1mOJYKfIPR7LoDQ9mXPOjoJoqy81S2I8N_N4V1vUb5AoIIIbLZhVYy7Mythp_T-mtop-vrsUOmeInPi9iDjx9w8K4ZfjXt2dotFL7oufSUosRNfcO_cim7GlB-pHugHaNE4nEeDGWx4W07ycm2Trb21kYhaLJjddA/image-asset.jpeg?format=1500w" alt="alt text" title="" style="zoom:30%;" />

Carpenter ants, represented in Figure N, are inhabitants of a lot of forest in the world. They like to build their nest in high humidity woods and they alone account for approximately 1000 ant species. If carpenter ants are among the most known species in the world, it is because they are sadly famous to be a nuisance to a lot of buildings and structures made of wood, causing structural damages. Nevertheless, carpenter ants are interesting little beings. A mechanism to highlight from their collective behavior is that, once their primary nest is big enough, carpenter ants like do build satellite nest containing workers while the eggs, the newly hatched larvae, and the queen remain in the primary nest. [^12] [^14]

### 2.2.3 Leafcutter ants ( *genera Atta - Acromyrmex*)

<img src="https://bloximages.chicago2.vip.townnews.com/tucson.com/content/tncms/assets/v3/editorial/6/f8/6f8ee49e-8721-53f0-acb4-1cecb5f4ed7a/57ed68f427660.image.jpg?resize=1200%2C856" alt="alt text" title="" style="zoom:37%;" />

Leafcutter ants are tiny ants of about 47 species which can carry about 20 times their body-weight. If an average-sized human could do that, he would be able to pull up to 1400kg [^13]. As their name may imply, Leafcutter ants cut fragments of a leaf which they bring back to the nest to feed the fungus garden. The fungus garden is the main source of supply of the colony and they take good care of it. The fungus garden can generate chemicals to tell the ants if the fragments they brought back from the foraging are toxic or not. This collaboration between ants and fungus is called an ant-fungus mutualism. But the care of the fungus garden does not end here. Indeed, a category of worker is specialized in taking care of it and bring the toxic leaf and dead leaves to a waste heap. These waste transporters are the older, more dispensable leafcutter ants that ensure that the younger and more functional workers can work safely in the fungus garden. Once the waste is deposed in the waste heap, workers constantly organize the waste to help decomposition [^15] [^18]

**Colony hierarchy** 

Like any other ant species, Leafcutter ants are a well-organized group. There are 4 main classes starting with the "minims". The minims are the smallest worker and they take care of growing the brood and make sure the fungus garden is in safe hands. The second category, the minors, are slightly larger workers which are the first line of defense against external threats. Their main occupation is to patrol around the nest and making its surrounding a safe place. The third category is the one depicted in all photography (yes, it is the one in Figure N). They are the "real" Leafcutter. They are generalised foragers and wander outside the nest to cut leave fragments and bring them back to the nest. The fourth and last category is the Majors which are the largest worker ants. They are the soldier of the nest, defending and attacking against outside threats. Moreover, this category of ants also helps in other tasks such as cleaning the foraging trails of large debris. [^13]



### 2.2.4 Pharaoh ants (*Monomorium pharaonis*)

<img src="https://pestclue.com/wp-content/uploads/2020/03/Pharaoh-ants-1200x675.png" alt="alt text" title="" style="zoom:45%;" />

Pharaoh ants are infamously known as the largest indoor nuisance pest as they have established themselves in the most part of the world due to high human migration movements with the exponentially growing access to transports such as boats, planes or cars. 

 This species of ants will happily established their nest anywhere given a reliable source of heat.

 Pharaoh ant colonies are polygynous, which means they can contain more than a singe queen, the highest number of queens found in a single colony is 200. Each of these queen will lay up to a hundred eggs in their lifetime.  [^17] [^16]

They have a decision making behaviour on which nest they will choose (might want to read more on that). It seeks to minimize the time the colony is without a nest while optimizing the nest the colony finally chooses. -> negative It is used in their decision making algorithm for nest migration.

#### 2.2.4.1 Pheromones [^19] [^17]

Pharaoh ants have three interesting type of pheromones. The first one is a long-lasting attractive chemical used to build trail network. This trail can remain detectable even if it is unused for several days. 

 -> Pharaoh ants cease activity at night and begin each day of work at around 8 am, yet parts of the trail network are identical each day

The second one is a mid-lasting pheromone which usually disappear in a matter of minutes. This type of pheromone is used to indicate path to a food supply. It has to be mid-lasting [^explain pathfinder behaviours]

, because it reduces the chances for an ant to follow an un-efficient path. (As in the pathfinder, the more ants go on a trail the more attractive it become).

The last type, which decay after two hours, is a repellent pheromone (or negative trail) which indicates that a path to a food supply is inefficient. 

#### 2.2.4.2 Foraging

Pharaoh ant have a very specific and well described way of scouting, explain in the foraging section of the wikipedia page. Let's write something about it.

-------

### 2.2.5 small section about interesting behaviours of some less notorious ants?

Some ants keep "domestic animals" who generate honey for them. They carry them along.

Many ants feed from flowering plants rich in carbohydrates

Some carpenter species construct defensive shelters around base of plants to guard them from other insects (food supply protection, could be cool to implement)

- Hymenoptera, females do all the work

https://www.quantamagazine.org/ants-build-complex-structures-with-a-few-simple-rules-20140409/

-> they talk about structure and bio robotic, not the same topic but it could be relevant to write a bit about it here.

https://www.sciencedaily.com/releases/2007/10/071009212548.htm

https://theconversation.com/leafcutter-ants-are-in-a-chemical-arms-race-against-a-behaviour-changing-fungus-97892



# 3. Ant behaviours and mechanisms

This section is about ants behaviours and mechanisms, we will go through the behaviours we mentioned in the early paragraphs of this paper as well as some new ones to see how collective behaviours can emerge when every element of the colony activate itself to a task. The aim is also to define a set of interesting behaviours that can be used either from a robotic stand point or a software stand point later in the master project.

Firstly, let's define what "collective behaviours" truly means. Collective behaviour is a process without central control that brings together multiple participants to achieve some outcome [^20]. Now that we have clearly defined what collective behaviours are let's think of something; Ants are capable of building complex structures, they can defend their nest as a group when a threat knocks to their door and are capable to organise to achieve such tasks. So how is it that such simple being are capable of the greatest thing? This is the question that we will elaborate on in the next sub-chapters.

## 3.1 Organization

How do ants organize? Even though ants are simples beings, their collaborative behaviour are extremely complex and close to be on a military level. Each colony more or less have the same structure but it may slightly variate from a species to another. A colony begins with its queen. The queen is not a hierarchal label as she has no power on what the ant colony is doing yet she is the only type of ant that will give birth to young workers. It has been found that some queen may lay up to 1000 eggs a day for up to seven years. The larvae are the growing workers laid by the queen, and are source of high tension between colonies when an attack occurs as some species like to steal them as food supply or even to use them as new worker in the opponent's colony [^28]. Growing to be adult ant, the larvae will splits themselves up in soldiers, workers and scout. Whereas being a soldier will depend on your

- Scout

- Soldier
- Worker
- Larvae
- Drones (Their only purpose is to mate with the queen)
- Winged male, once they mature live colony in swarms to create new colonies. We could imagine that the newly created colony could enter war with the original one (after a few gene epoch)

## 3.2 Communication

### Pheromones [^[^source](https://en.wikipedia.org/w/index.php?title=Carpenter_ant)]

As in most other social insect species, individual interaction is heavily influenced by the queen. The queen can influence individuals with odors called [^pheromones](https://en.wikipedia.org/wiki/Pheromones), which can have different effects. Some pheromones have been known to calm workers, while others have been known to excite them. Pheromonal cues from ovipositing queens have a stronger effect on worker ants than those of virgin queens.[^[^18\]](https://en.wikipedia.org/wiki/Carpenter_ant#cite_note-18)

We could imagine to have an excitement of pixel in a nest, close to a queen, expressing which pheormone is currently being diffused. (Juste une diffusion colorée de pixel aux alentours de la reine).

I think the idea is to first be able to generate one colony and see it construct/gather food and breed workers. Implement the war rules as well.-> each colony has its own chemical badge

-> the shortest the path is the more likely it is that an ant encounters it before it evaporates

## 3.3 Navigation

https://en.wikipedia.org/wiki/Ant_colony_optimization_algorithms

https://www.quantamagazine.org/decoding-the-remarkable-algorithms-of-ants-20150625/

Edward [^21]

## 3.4 Task

### 3.4.1 Types of task

The types of task that a colony has may variate slightly from a colony to another (as in leaf cutter ant's colony where some ants have to maintain the fungus garden) but overall we can sum them up in X tasks:

- Foraging
- Scouting
- Patrolling
- Nest maintenance

#### 3.4.1.1 Foraging

When foraging, ants will move randomly in many different directions to increase their chance to encounter food and a positive pheromone trail. If the ants ever finds food it will sub-sequently crawl home leaving behind it a pheromone trail indicating the other ants where the food is. As more ants encounter the trail left by our lucky ants, the pheromone trail get bigger and bigger leading to even more ant finding it. The more appealing the food is (in quantity) the most ant will switch their current task to get the food area. If the ant fails to return to the colony in time the pheromone trail eventually evaporate and no ant will be able to follow the trail back to the food supply.



#### 3.4.1.2 Scouting

#### 3.4.1.3 Patrolling

#### 3.4.1.4 Nest maintenance

### 3.4.2 Task allocation [NRV]

As we have mentioned earlier, there is no central control unit in a colony of ants. This means that there's no one to tell an ant what to do at any given time and yet ants seem to have a pretty busy day-to-day calendar. Few studies have **suggested** that ants can select a task based on their age, their body size, their genetic background, their position in the nest, the way they eat but also by receiving signals from other ants [^22]. Earliest studies have highlighted (**todo** re-find the study**) ants can determine what task it should do with a very clever decision model. This decision is based on the rate at which an ant encounters another one. Indeed, every time an ant makes contact, there is a small probability that the ant will switch to the encountered ant's task. This also means that the more ants with the same task our ant encounters, the more likely it is to switch (note that this decision-making is only based on interaction and not location). Ultimately, larger ant colonies are better at task allocation than smaller ones. Switching to a task is a thing, being aware of what the other ant's task was is another. How is it that an ant knows what task to switch to even though we have stated multiple times in this paper that ants don't have any complex communication tools? It is because ants have been given antennas which they rob against encountered ants' antennas. This contact is what tells the ant the task the other is performing and it does so by analysing the cuticular hydrocarbon the antennas carry. These cuticular hydrocarbons variate regarding where the ant previously was and what task it was performing. For example, when ants are foraging out in the sun, the proportion of n-alkanes in their hydrocarbon profile increases leading the forager to smell recognizably different from an ant that works inside the nest  [^payam study]. Age is also a variable to take into consideration. Even though it has been found that this does not impact task allocation on a large scale, studies have found that older ants would usually take care of the maintenance of the nest and really any task that happens inside the nest, whereas younger workers would more likely be outside to forage and defend the nest in case of attack. Deborah M. Gordon, a world wide known scientist famous for her lifetime studies on ants, has discovered that not every ant would switch to a certain task even though the probability is high. She discovered that ants have "preferences" to which task they would be willing to switch to and she has then dressed a map of this behaviour:

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/ant_task_switching.png?raw=tru" alt="alt text" title="" style="zoom:100%;" />

This map shows that only in-nest ants (the older or/and inactive ants) would switch to nest maintenance if the demand was high in more important tasks such as foraging and that the highest task priority is foraging as every ant can eventually ending in switching up their task to become a forager. 



### 3.4.3 Environmental challenges [NRV]

The way ants choose what to do is also environment-based as there's a notion of operating cost of tasks that an ant takes into consideration when performing a task. Indeed, In some places in the world such as deserts or highly dry terrains, the operating cost of task is very high as finding resources is hard. This means that an ant will think twice before allocating some of its time scouting for food outside as it only does it if the returned income is higher than the one spent to get to the supply. This high operating cost behaviour can be summed up as "Don't go unless something positive happens". In some other places of the world the operating cost is low (houses, groceries, but also tropical forest), meaning that the energy an ant has to spend to reach a resource is little in comparison to the income it will return. This is the "Go unless something bad happens" behaviour [^29]. Such studies have also been conducted in human threatening environment such as space, where a small colony was filmed to study these behaviours. The study has shown that ant wouldn't move unless the colony's existence was at stake [^30].

## 3.5 Lifecycle of an ant colony

Ant colonies are technically alive forever, unless a storm or any natural / human catastrophe wipes them down. 

Ants kid and grant kid colonies ressemble parents in many ways. For example in the day they go foraging but also by having a pretty similar chemical badge	

### 3.5.1 Males and Females in ant colonies

Male are just there to reproduce, dies after mating with a winged female. The workers are all female -> https://www.youtube.com/watch?list=PLD018AC9B25A23E16&v=vG-QZOTc5_Q&ab_channel=TED-Ed

Each year at the same date, a female virgin winged ant go outside with few males and go mate. The new queen then dig a hole a lay her first eggs, feeding them from her body fat reserve. The ant will use sperm from the very first time she mated with one or two male and will keep it to lay eggs for 15 to 20 years.

### 3.5.2 Day and night cycle for ants

-> maintenance worker in the morning



-----

Sort of a conclusion to the ant kingdom chapter. Here I tell what behaviour is to remember and why they are interesting. (Also talk about task allocation in swarm robotics.). Here I guess I can say that for little robotic swarm task allocation and pheromones communication is the most interesting thing to take. But for a visual visualisation there's  more.

# 4. Building a simulator

## Introduction

## Exploration of Language and drawing frameworks [^NOK] [^NRV] 

Many technics can be used to build a good simulator, and yet, it is difficult for one to select the best within the ocean of languages and framework that exists. Many of these usually fit specifics kinds of implementation. This chapter is a deep through of some of the most relevant ones. We will go deeper on the understanding of a good drawing tool in the specific case of the ant war simulation and this will also be the occasion to have a first sight at the overall implementation.

The first step before plunging into google and look at every language and framework that exists is to specify the needs. As we have not yet a good understanding of the complexity of the simulation (this problem will arise later deeper phases), one needs to think on a more abstract level. Figure [^N] is a first very simple high-level not to scaled representation of an ongoing epoch in the simulator. Firstly, we need to be able to draw. This might sounds a bit too abstract but it already narrows down the scope as many languages such as C or C++ are low-level language, which would only add more complexity to the project (don't get me wrong, one can use these languages to draw, but there are a lot of easier ways to do it with higher-level languages). Server side languages like PHP, which depends on client side action to be able to draw, are also out of the basket. Secondly we will need to draw very simple shapes (mainly pixel alike) in a large quantity, which means that we don't need complex 3D render technics or polygon like software such as WebGL, ThreeJS and such. Thirdly We don't need to perform a lot of complex mathematical operations (such as integration, derivative, or trigonometry), as the agents will be evolving in a 2D plan. Finally, it is very likely that threads will be useful in the simulation (controlling the time, nests and such), so we need a language where using these is more or less easy. This conclude a first good definition of preliminary needs.

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/sim1.png?raw=tru" alt="alt text" title="simulation rep 1" style="zoom:100%;" />

Given that I do not master every languages that exist and since this project is not about the  discovering and use of a new language, this narrows down the scope even more. In the above section we got rid of the low-level languages and the server-side ones since they would only add more complexity in an already quite complex task. This leaves me with Javascript, Python and Java, three interesting candidates. From there, it is more of a personal choice than an actual language to language comparison. Each of these three languages implement drawing technics and can perform all of the above described needs. I will nonetheless explain the advantages and inconveniences of each, based on my personal experiences and knowledges acquired throughout my developer’s life. 

 Let’s start with Python. Python is a very light and high-level language and is surprisingly simple and satisfying to work with. Being non-typed and almost “Human language” alike makes it a very appealing language to choose. It has good support of threads and includes some powerful (yet, unknown to me) drawing frameworks such as PyGame or Arcade. Python almost look like the perfect candidate. However, it is the slowest of the three at “Calculation steps per seconds” (as shown in Figure N), which is highly important when one needs to create a simulation as it will defined how much item can the program handle at a given time T. That being said, Python remain quite an interesting candidate, but ultimately not the one which will be used for the simulation. Secondly, Java. It is broadly known (which makes it one of the most documented language in the market) and can be used for more or less everything. It already implements a lot of structure, function, drawing technics and basic graphic tools because it has been designed to be a somewhat higher-level version of C with oriented object programming. It uses the JVM (Java Virtual Machine) to run the Java compiled bytecode which adds a lot of overhead at the start compared to interpreted languages (but saving you from dummy mistakes). It however has the highest “Calculation steps per second” score compared to the two others as Figure N demonstrates it. All of that being said, Java would almost be the perfect candidates. The only downside one could really think of is the lack of “good” drawing frameworks. It becomes quickly frustrating to work with drawing and threading in Java (but this is highly personal). Finally Javascript. Javascript is the kind of candidate who is a clever mixt between the advantages of Java and Python. It has a good “Calculation steps per second” score, it is easy to use and web based. Being web-based means that it is rather easy to deploy [^more on that]. It has a good community and support a lot of user-made libraries, plus its documentation is also very great (as Python and Java). It has a very good vanilla drawing libraries and very good drawing frameworks such as Preprocess that can be used on top of VanillaJS

 

Used a lot for water like simulation (good at physics 

 Good community, large support, great documentation. 

Javascript is very much not perfect. Indeed, it is known among developers to be a very illogical language and sometimes being pointed at for it. The following is a short video that represents how bad Javascript can sometimes be: https://archive.org/details/wat_destroyallsoftware

 

This concludes blah blah…

<img src="https://2.bp.blogspot.com/-BcemgfpuSvQ/UfCyESwcPKI/AAAAAAAAA9Q/a2qKDpvmZN8/s1600/LatticeBoltzmannPerformanceGraph.png" alt="alt text" title="simulation rep 1" style="zoom:70%;" />

 

This concludes blah blah…

**Javascript**

- Top 1 candidate
- Even vanilla javascript is super good a drawing in canvas.
- WebGL and TreeJS are good but they are optimised for 3D render and we don't need that
- Preprocessing is a very nice and easy library that one can use on top of vanilla JS
- Light and Web based language (easy to deploy, test and maintain)
- Powerful, even for math based simulation
- Mid for calculation

## I must explain why it makes sense to implement env changes. The way the ants interact with everything actually depends on it. 



## it could be interesting to explain how I envision the below object, why all this variables and such

**to simulate https://ccl.northwestern.edu/netlogo/ but not building**

## To include in it

### introduction

"From what we been discussing in the "ant" section "...

- Passing day
- Being able to pause it and to click on any entity to get its details??
- Nomadic and stationary phase of an army ant colony
- Include heat and night/day period? 
- Include small difference in terrain height?
- Include seasons?
- Operating cost of task
- Task allocation
- Lots and lots more :electric_plug:

should we have no nest in start and workers have to create it by gathering dirt (can look back at the simple rule to building structure from the article). 

In the Pharaoh wikipedia page, they say that around  8 am scout go search for food, this should somehow be included in the brain of the ant. So that the simulation would look even more accurate. (Like in the night time nothing much appears, and then suddenly when sun appears, scout go search for food).

**A lot of the "to include in" are not specifically cited above, look at the object for more**

## Sketch of model

```javascript
// This is an abstract implementation of objects / classes

World {
	var is_day, temperature, day, season, time, speed, is_paused
  var global_population_increase_rate, global_population, noise_operation_magnitude
  var operating_cost // -> might be infered by above variable.
  var zoom //?? might be useful to scale every pixel

  Nest nests[^]
	Terrain terrain
	...
}

Terrain {
	var width, height
	Pixel map[^width][^height]
	...
}

Pixel {
	var height
	var type // Nest, food, ...
  var label[^{
    colony : '',
    magnitude : int // Every time an ant of the colony walks on a pixel with its same chemical labeel, increase magnitude by a pre-defined offset.
  }] // Chemical left by ant, if exists.
	...
}
  
Task {
  var id, description
  ...
}

Nest {
  var origin // pos(x,y) of the very first pixel of the nest
	var surface, health, population_increase_rate
    
	Resource resources[^{
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
	Queen queens[^] // One or many queens
	Worker workers[^]
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
  
function get_operating_cost(Task t) {
  /*
  	is a task a high operating cost or a low operating cost?
  */
}
```

# 5. Robotic

## Swarm robotic

Swarm robotic is the art of collectively run a lot of robots to solve problems by forming complex structures and behaviors such as the one observed in nature. They are scalable systems made of simple.

Scalable systems, with many robots (often homogeneous)

Simple control inspired by nature

Example: Ants and the pathfinder (have a nice and elaborated example here, with schema)

## State of art

- 272 e-puck robots
- Kilobot
- Locomotion unit
- Jasmine III
- SwarmBot -> https://www.youtube.com/watch?v=77SEQ-kj8PI&ab_channel=ScienceSquared

## Robot ant

Need communication device and ?? To simulate the pheromones trail. Something unrealistic but still doable would be to have a very large led panel, when the panel senses pressure by a robot going on it it turns the led on, that way another robot could see it with a light detector. We could even make the led fade out to simulate pheromones trail evaporation.

## In my case

Replicated few learnt behaviours in a robot?

### Talk about the mini swarm robot ITU has 

### The limitation of the technology and cost

- [^Robot that can replicate swarm behaviours](https://newatlas.com/colias-swarm-robot/33897/)

# 6. Conclusion

The study of the living things mechanisms is called biomimetic. This art of replicating what nature does has enabled us to ....

# 7. References

[^0 ]: [Biomimetic design: 10 examples of nature inspiring technology, Gertie Goddard, N/A](https://www.sciencefocus.com/future-technology/biomimetic-design-10-examples-of-nature-inspiring-technology/)
[^1]: [Phylogeny of the Ants: Diversification in the Age of Angiosperms, 2005](https://www.google.com/url?q=https%3A%2F%2Fpdfs.semanticscholar.org%2Fd186%2Fbbe2881027f99bbf1001c240f71f93baf6af.pdf&sa=D&sntz=1&usg=AFQjCNEw7aEhyFLFdE30DEsnv__kmTpbgA)
[^2]: [Ancient Ants Arose 140-168 Million Years Ago; Insects Needed Flowering Plants To Flourish, 2006](https://www.google.com/url?q=https%3A%2F%2Fwww.sciencedaily.com%2Freleases%2F2006%2F04%2F060407144825.htm&sa=D&sntz=1&usg=AFQjCNFl6IpckBVsLxDdvSME-ZkG-UyVoA)
[^3]: [Why is eusociality an almost exclusively terrestrial phenomenon?, 2014](https://www.google.com/url?q=https%3A%2F%2Fbesjournals.onlinelibrary.wiley.com%2Fdoi%2Ffull%2F10.1111%2F1365-2656.12251&sa=D&sntz=1&usg=AFQjCNH4eGixi40S7Pc4igMwqapbbocvxA)
[^4]: [Ant Ecology, 2010](https://books.google.de/books?hl=de&lr=&id=vlwVDAAAQBAJ&oi=fnd&pg=PR5&dq=10,000+trillion+ants&ots=aUqWFkzcGi&sig=Jhxc-cjuCLNaBqW7mf3kRWFJcZA#v=onepage&q=10%2C000trillion&f=false)
[^5]: [In search of ant ancestors, 2000](http://www.google.com/url?q=http%3A%2F%2Fwww.pnas.org%2Fcontent%2F97%2F26%2F14028.full&sa=D&sntz=1&usg=AFQjCNF1qJJu_HfDjQmCj-yjulkC35QH-g)
[^6]: [Why Ants Rule the World, Corey Binns, 2006](https://www.livescience.com/747-ants-rule-world.html)
[^7]: [The Remarkable Self-Organization of Ants, 2014](https://www.quantamagazine.org/ants-build-complex-structures-with-a-few-simple-rules-20140409/)
[^8]: [Army ant, 2008](http://www.newworldencyclopedia.org/entry/Army_ant)
[^9]: [Deadly Army Ants Decimate Entire Ecosystems, 2018](https://roaring.earth/deadly-army-ants/)
[^10]: [Wikipedia, Army ants](https://en.wikipedia.org/wiki/Army_ant)
[^11]: [How Ants Wage War, 2011](https://www.pri.org/stories/2011-11-16/how-ants-wage-war)
[^12]: [Wikipedia, Carpenter ant](https://en.wikipedia.org/wiki/Carpenter_ant#Behavior_and_ecology)
[^13]: [Wikipedia, Leaf cutter ant](https://en.wikipedia.org/wiki/Leafcutter_ant)
[^14]: [Carpenter Ants, College of agriculture, food and environment, 1997](https://entomology.ca.uky.edu/ef603#:~:text=Carpenter%20ants%20actually%20construct%20two,queen%2C%20eggs%20or%20young%20larvae)
[^15]: [Waste management in leaf-cutting ants, A. N. M. Bot, C. R. Currie, Adam G. Hart, Jacobus J Boomsma, 2001](https://www.researchgate.net/publication/248373454_Waste_management_in_leaf-cutting_ants)
[^16]: [Pharaoh Ants: Interesting Facts About Pharaoh Ants, Will David, 2020](https://pestclue.com/pharaoh-ants-interesting-facts-about-pharaoh-ants/)
[^17]: [Wikipedia, Pharaoh ants](https://en.wikipedia.org/wiki/Pharaoh_ant)
[^18]: [Leafcutter ants are in a chemical arms race against a behaviour-changing fungus, Sarah Worsley, 2018](https://theconversation.com/leafcutter-ants-are-in-a-chemical-arms-race-against-a-behaviour-changing-fungus-97892)
[^19]: [Longevity and detection of persistent foraging trails in Pharaoh's ants, Monomorium pharaonis (L.), Ducan E Jackson, Stephen J. Martin, M. Holcombe, Francis L.W. Ratnieks, 2006](https://www.researchgate.net/publication/222404029_Longevity_and_detection_of_persistent_foraging_trails_in_Pharaoh's_ants_Monomorium_pharaonis_L)
[^20]: [The Evolution of the Algorithms for Collective Behavior, Deborah M. Gordon, 2016](https://www.cell.com/fulltext/S2405-4712(16)30332-5#:~:text=Collective%20behavior%20is%20the%20outcome%20of%20a%20network%20of%20local%20interactions.&text=I%20suggest%20that%20a%20focus,collective%20behavior%20of%20cellular%20systems.)
[^21]: [HOW DO ANTS KNOW HOW TO FIND THEIR WAY HOME?, Gryphon Adams, N/A](https://animals.mom.com/role-scout-bee-5861.html)
[^22]: [Ant task alloc](http://people.cs.georgetown.edu/~cnewport/teaching/cosc844-spring17/pubs/ants-task.pdf) -> **to improve**
[^23]: https://www.sciencedirect.com/topics/agricultural-and-biological-sciences/army-ant -> **to name**
[^24]: [Inside the Amazon Warehouse Where Humans and Machines Become One, Matt Simon, 2019](https://www.wired.com/story/amazon-warehouse-robots/)
[^25]: [HOW HONEY BEES HELPED THE INTERNET, Pacific standard staff, 2017](https://psmag.com/news/how-honey-bees-helped-the-internet)
[^26 ]: [Six weeks in the life of a reproducing army ant colony: Male parentage and colony behaviour, D. J. C. Kronaeur, E. R. Rodríguez Ponce, John Lattke, Jacobus J Boomsma, 2007](https://www.researchgate.net/publication/225763258_Six_weeks_in_the_life_of_a_reproducing_army_ant_colony_Male_parentage_and_colony_behaviour)
[^27 ]: [A Mesozoic Clown Beetle Myrmecophile (Coleoptera: Histeridae), Yu-Lingzi Zhou, Adam Slipinski, Ren Dong, Joseph Parker, 2019](https://www.researchgate.net/publication/332447535_A_Mesozoic_Clown_Beetle_Myrmecophile_Coleoptera_Histeridae)
[^28 ]: [Kidnapper Ants Steal Other Ants' Babies - And Brainwash Them, Josh Cassidy, 2019](https://www.kqed.org/science/1947369/kidnapper-ants-steal-other-ants-babies-and-brainwash-them)

[^29 ] :  [Task switching is associated with temporal delays in *Temnothorax rugatulus* ants, Behav Ecol, 2017](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5255904/)

[^30] : [**All Together Now—A Lesson from Space Station “Ant-stronauts”**, Jessica Nimon,2014](https://www.nasa.gov/mission_pages/station/research/news/ants_in_space/)

[swam robotic] https://www.frontiersin.org/articles/10.3389/frobt.2020.00036/full

---

**Youtube**

- https://www.youtube.com/watch?v=0FZLPbBDYAA&ab_channel=wocomoWILDLIFE
- https://www.youtube.com/watch?v=QO3yKYC305g&ab_channel=KineticSand

Pic:

- http://dvschroeder.blogspot.com/2013/07/java-vs-javascript-vs-python.html
- https://bugoftheweek.squarespace.com/blog/2016/1/13/carpenter-ants-here-and-there-icamponotusi-spp -> carpenter ant pic
- https://tucson.com/controlling-leaf-cutting-ants/article_5c0f3482-89a3-11e6-ae65-8fe8c1dbd57d.html -> leaf cutter pic
- https://pestclue.com/pharaoh-ants-interesting-facts-about-pharaoh-ants/ -> pharaoh ants pic
- https://asia.nikkei.com/Business/Companies/Japan-s-fastest-bullet-train-to-squeeze-out-trip-every-5-minutes2 -> Japanese bullet train picture

[^27]: 