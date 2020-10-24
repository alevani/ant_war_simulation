```
NOK = Not Ok 

MOK = More or less ok

OK = Done.

NRV = Need revision (grammar and spelling)

[Nothing] = Actually not ok but I was just too lazy to write [NOK] or [MOK]
```

----

[toc]

-----

# 0. Abstract

What is the document about.

# 1. Introduction [NOK]

This project is part of the "[Research project (K-CS and K-SD) Autumn 2020 (KIREPRO1PE)](https://learnit.itu.dk/course/view.php?id=3020186)" ITU course which intend as a bridge between the specialisation course and the master thesis (that is, a preliminary work for the Master thesis). Its aim is the study of the abstract mechanisms employed by ants during attack between colonies of given species. Ants are one of the various social species that can be studied to create bioinspired algorithms and models of collective behaviors. They are very interesting because as a single unit, an ant is a very simple being, but as a swarm they show a lot of exciting collective behaviours and their underlying mechanisms can be studied and used for everyday problems.

The art of studying the nature to replicate its behaviors into robotic to solve complex human problems is called Bio-inspired robotic (or more commonly “Biomimetic”). There are numerous examples such as the very famous “Japanese Bullet train” (Shinkansen) which gets its nose design from the Kingfisher bird’s beak (who’s aerodynamic ), reducing the train’s energy consumption by 15%, making it 10% faster and quieter. 

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/bullet_train.jpg?raw=true" alt="alt text" title="The Shinkansen bullet train" style="zoom:25%;" />

The hook and loop fastener (also known as the Velcro), created by the Swiss engineer George de Mestral in the 1950s is also a very famous example of biomimetic. This two part binding system was inspired by burrs, which de Mestral studied under microscope after he figured how surprisingly easy these would stick to its dog's hair. He discovered that burrs had micro hook that were able to catch anything with a loop. Nowadays, the hook and loop fastener is used throughout the world.

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/burrs.jpg?raw=true" alt="alt text" title="Burrs and their loops" style="zoom:60%;" />



Other examples are the use of insect-inspired algorithms for coordination within groups of robots, on land, air, or even underwater.





https://asia.nikkei.com/Business/Companies/Japan-s-fastest-bullet-train-to-squeeze-out-trip-every-5-minutes2 -> Japanese bullet train picture

## 1.1 Goals [NOK]

what should be the learning outcome and product outcome

Explain that it won't be a SUPER very accurate simulation, I'm an engineer not a biologist. But the tool will be opensource and it should be easy to define and change sets of rules <----- Maybe the rules will be a decision tree that any dev could change and see the output through the simulation.

## 1.2 State of art [NOK]

Even though biomimetic on ants is a very studied topic with numerous papers, videos and books about the subject, there is no proper implementation of an ant war simulator. The closest implementations are simulations of pathfinders (here is an example found on Github: http://bwiklund.github.io/ant-simulator/) or very low level territory defence demonstration (such as https://github.com/computationalcore/ants-simulation). 



https://github.com/computationalcore/ants-simulation -> nice! ant colony simulator, the brain of each ant is fairly simple but that's a start

https://github.com/karask/AntSim -> could be useful but poorly documented

http://ants.aichallenge.org/

https://github.com/ultimape/PixelAntColony

write way more here, find examples video and relevant study on the subject

# 

Talk about examples from the file form Payam.

It is very likely that this project will be a reflection of all the studies, such as “Combat between large derived societies: A subterranean army ant established as a predator of mature leaf-cutting ant colonies” written by Scott Powell or “The Remarkable Self- Organisation of Ants”, written by Emily Singer.

# 2. The ant kingdom

This section is about ants. Their history, their birth, their life, but also how they function and behave in groups and individually. As we are restrained in time and space, we will talk about only a very few of the enormous amount of interesting species that exist out there. The end goal is to give ourselves an Idea of which ant species are good candidates for a simulation and why they are but also to highlights very interesting biological behaviors that emerge within each species. At the end of the section, some of these biological behaviors will be chosen, based on preferences and interests, to be used later for the simulation. 



## 2.1 Ants

Ants are ancient beings that emerge around 140 to 168 million years ago, even though they started to diversify only about some 60 million years after [1] [2]. From the dinosaur era to the Human realm, no kingdom has ever been as large and as powerful compared to the ants super-kingdom. They are estimated to be about 10'000'000'000'000'000 (10'000 trillion) individuals [4], which account for 20% of the total animal biomass[3] [5]. This superkingdom, however, is far from being an unified and coherent heaven. From the 16'000 classified species and the 20'000 estimated species  [2], rare are the ant species that resemble one another. Indeed, from the very early age of their existence, ants have been evolving and adapting to a large amount of environment. They now come in a large variety of colors, from yellow to black. They live in every environment, from extreme heat desert to rainy forests and swamps. The only places that remain untouched (almost) are cold and high places on earth, as ants need a heat source to survive [6]. Individually, ants cannot do much, they are too simple and their brain is only capable to perform a limited set of action. To become what ants are today, they needed something fundamentally important: Collaboration. It is like the human race. We, throughout the years, had to come up with some very complex collaboration tools and framework to construct the society we have nowadays. 

[explain what ants can build, what they do, -> **– They construct complex colonies, care for livestock, do agriculture or have complex symbiotic relationships.**] [7]

However, this collaborative behaviour only emerges within ants of the same colonies (and sometimes, but less likely, of the same species). Ant colonies are more likely to fight or avoid contact than discuss peacefully about what would be the best strategy to get the piece of bread from a picnic and how it would be beneficial for each of them. So what is the difference? What makes them less able to collaborate than humans? As said earlier, they have a very limited brain and understanding of the world. At their level everything but the colony and the queen survival is meaningless. Ants do not live a happy life, and their main purpose is only to fulfil the colony's needs. 

## 2.2 Organization

Even though ants are simples beings, their collaborative behaviour are extremely complex and are on a military level. Each colony more or less have the same structure (it may variate from a species to another)

### 2.2.1 Hierarchical Structure

Even though it exists thousands of species, ant colonies have a somewhat structured and space-and-time proof hierarchy. (It may variate but mostly the same)

- Scout
- Queen

Queen [Some species of ant have queen that lay up to 1000 eggs a day for up to seven years](https://www.terminix.com/blog/education/what-is-an-ant-colony/) -> That could give me information on of much eggs to breed in one epoch

- Soldier
- Worker
- Larvae
- Drones (Their only purpose is to mate with the queen)
- Winged male, once they mature live colony in swarms to create new colonies. We could imagine that the newly created colony could enter war with the original one (after a few gene epoch)

### 2.2.2 Communication

**Pheromones**

​	-> each colony has its own chemical badge

### 2.2.3 Task allocation

## 2.3 Interesting species

! Say that it's gonna be the main species of the simulator due to its very various interesting behaviours.

### 2.3.1 The army ants

From all the known ants species, there is a category of ant legitimately called "the army ants". This category that the evolutionary tree has brought to be combatants, are dreadful warriors among the ground. They have been given large mandibles, painful sting and armour, and it exists about 200 species of them [8]. If two colonies or species encounter one another in the nature, it is unlikely that they will fight against each other. Indeed, this makes sense from an evolutionary stand points as throughout time army ants that were attacking other army ants eradicate themselves to extinction [11]. They don't have a nest, they rather like to crawl on the ground in a very long and narrow group, consuming up to 500'000 prey animals each day [9]. The behaviour of crawling on the ground is something specific to the army ants called the "Army ant syndrome" [10] (see Figure N). This syndrome is a two phase life style cycle that army ants have adopt to .. [?]. 

In the first two to three weeks long phase called the stationary phase, the prey that were previously used to feed to the larvae are now reserved to the queen for her to prepare her birth cycle. The queen they lays her eggs and reaching the end of the stationary phase, the new born larvae emerge from their cocoons as the colony prepares itself to enter the second phase. [9] 

The second phase called the "Nomadic phase" last approximately 15 days, which gives the time for the new born larvae to develop into fully functional workers. In this phase, the colony moves during the day, etching on the ground and capturing everything they can, from insects, spiders and even dead ant bodies. Usually an ant colony would send one or few scouts to look around the colony and seek for food or threats, but the army ants are leaderless group of foragers and like to overwhelm the prey at once sending by sending a lot of them. At the end of the 15 days, the larvae no longer require food and the colony can enter the stationary phase again. [9]

<img src="https://ars.els-cdn.com/content/image/3-s2.0-B9780128015322000143-f14-29-9780128015322.jpg?_" alt="alt text" title="simulation rep 1" style="zoom:100%;" />

#### Structure within the colony

**structure in the colony** -> check if it's the correct structure for the army ant

- Workers
- Soldiers
- Males
- Queen



#### Some famous species

- Neotropical Army Ants => specialised in hunting other insects (wasp, termite, other ants)
- Army Ant solider
- Bullet Ant
- Giant Amazonian Ant



**Very interesting, could be added to the simulation that's quite fun**

## Other types of ant species

### Carpenter ants -> we don't need much more, a small introduction is far more than enough.

https://en.wikipedia.org/wiki/Carpenter_ant#Behavior_and_ecology

Over 1000 species

Build nest in woods

They have a primary nest and create satelite nest

Only eggs, the newly hatched [larvae](https://en.wikipedia.org/wiki/Larvae), workers, and the queen reside in the primary nests

Build nest in high humidity

### 

### Leaf cutter ants

https://en.wikipedia.org/wiki/Leafcutter_ant

47 species

Carry 20 times their body weight (it's as if I could carry up to 1500kg)

**Colony hierarchy** 

- Minims -> smallest workers, take care of the growing brood and the fungus garden
- Minors -> Slightly larger, First line of defence, they patrol. 
- Mediae -> Generalised foragers, cut leaves and bring fragments it back to the nest
- Majors -> Largest worker ant, act as soldier (defends and attacks), they also help in other task such as cleaning the foraging trails of large debris.

They cut leaf to bring it back to the fungus garden, feeding the fungus plants with it (ant-fungus mutualism). The fungus diffuses chemical telling the ants if the type of leaf they brought back from foraging is toxic or not for it.

They have a waste management for the toxic leaf -> "The waste transporters and waste-heap workers are the older, more dispensable leafcutter ants, ensuring the healthier and younger ants can work on the fungal garden. The *[Atta colombica](https://en.wikipedia.org/wiki/Atta_colombica)* species, unusually for the Attine tribe, have an external waste heap. Waste transporters take the waste, which consists of used substrate and discarded fungus, to the waste heap. Once dropped off at the refuse dump, the heap workers organise the waste and constantly shuffle it around to aid decomposition"



### Black crazy ants (Paratrechina)

https://en.wikipedia.org/wiki/Longhorn_crazy_ant

They are called like that because they dash erratically around instead of following straight lines

One of the most widespread ant specie in the world,

Nest in either dry or damp sites (hollow trees, under loose bark / rocks / wood logs...)



### Pharaoh ants

Known to be the largest major indoor nuisance pest, it has established itself in the most part of the world, and will happily do so provided a source of heat.

Each colony contains many queens (polygynous), up to 200, which can lay hundreds of eggs in her lifetime. 

They have a decision making behaviour on which nest they will choose (might want to read more on that). It seeks to minimize the time the colony is without a nest while optimizing the nest the colony finally chooses.

#### pheromones

They have tree types of pheromones, one is a long-lasting attractive chemical, used to build trail network (remains detectable even if unsunsed for several days)

Pharaoh ants cease activity at night and begin each day of work at around 8 am, yet parts of the trail network are identical each day

Another one which this time disappear in a matter of minutes  is used to draw path to a food supply. The very fact that it Is medium lasting is nice, because it reduces the chances for an ant to follow an un-efficient path. (As in the pathfinder, the more ants go on a trail the more attractive it become).

The last one is a repellent, it is use as a "negative path trail", indicating that a path to a food supply is not a good one. Decay after two hours. It is used in their decision making algorithm for nest migration.

#### Foraging

Pharaoh ant have a very specific and well described way of scouting, explain in the foraging section of the wikipedia page. Let's write something about it.

-----

### Queen

If there is multiple queens, workers might kill all of them but one at some point. Queens will produce fewer workers so that they have more fighting power if needed

https://www.livescience.com/10635-queen-ant-sacrifice-colony-retain-throne.html

-------

Some ants keep "domestic animals" who generate honey for them. They carry them along.

Many ants feed from flowering plants rich in carbohydrates

Some carpenter species construct defensive shelters around base of plants to guard them from other insects (food supply protection, could be cool to implement)

- Hymenoptera, females do all the work

https://www.quantamagazine.org/ants-build-complex-structures-with-a-few-simple-rules-20140409/

-> they talk about structure and bio robotic, not the same topic but it could be relevant to write a bit about it here.

https://www.sciencedaily.com/releases/2007/10/071009212548.htm

https://theconversation.com/leafcutter-ants-are-in-a-chemical-arms-race-against-a-behaviour-changing-fungus-97892

-short introduction on ants, the species, the population, why they are interesting



## Ant mechanisms



### Individual

Winged male, once they mature live colony in swarms to create new colonies. We could imagine that the newly created colony could enter war with the original one (after a few gene epoch)

short paragraph explaining what an ants alone can do (not a whole lot)

**source ytb**

Scout find food and mark the way (also here https://www.youtube.com/watch?v=NJ3pLY819hA&ab_channel=TerraMater) 

for surface extension, they send scout, once scout from each colonies encounter they rush to their nest and ring the alarm.

### Collective

Collective behavior is a process without central control that brings together multiple participants to achieve some outcome. We see the outcomes of collective behavior everywhere in nature (The Evolution of the Algorithms for Collective Behavior) -> this book also mentioned the idea of an "food availability measure" by ants. => how much ant are dispatched to a food supply depends on the rate at which food if is found and not the location. The more food is available the more quickly a ant will return to the nest, the more worker it will find and convert.

-> ants task management: 

Each ants do what is based on the rate of interaction between ants. (Cuticular hydrocarbon). It tells what ants does what because the way ant ant work tells change the hydrocarbon chemical reactione. For example, when harvester ant foragers are out in the sun, the proportion of n-alkanes in their hydrocarbon profiles increases, leading a forager to smell recognizably different from an ant that works inside the nest (Wagner et al., 2001)

-----

I think an important ascpect is that all the behaviour won't be findable as "algorithms" just because they are not. For instance, they way ants breed or such is not a algorithm. So I will have to learn how they do it and create my own algorithm. That's gonna be a nice output.

https://en.wikipedia.org/wiki/Ant_colony_optimization_algorithms

https://www.quantamagazine.org/decoding-the-remarkable-algorithms-of-ants-20150625/

- Communication
  - -> they can comm. through pheromone trails (https://www.quantamagazine.org/ants-build-complex-structures-with-a-few-simple-rules-20140409/)
- Pathfinder

# Building a simulator

## Introduction

## Exploration of Language and drawing frameworks [NOK] [NRV] 

Many technics can be used to build a good simulator, and yet, it is difficult for one to select the best within the ocean of languages and framework that exists. Many of these usually fit specifics kinds of implementation. This chapter is a deep through of some of the most relevant ones. We will go deeper on the understanding of a good drawing tool in the specific case of the ant war simulation and this will also be the occasion to have a first sight at the overall implementation.

The first step before plunging into google and look at every language and framework that exists is to specify the needs. As we have not yet a good understanding of the complexity of the simulation (this problem will arise later deeper phases), one needs to think on a more abstract level. Figure [N] is a first very simple high-level not to scaled representation of an ongoing epoch in the simulator. Firstly, we need to be able to draw. This might sounds a bit too abstract but it already narrows down the scope as many languages such as C or C++ are low-level language, which would only add more complexity to the project (don't get me wrong, one can use these languages to draw, but there are a lot of easier ways to do it with higher-level languages). Server side languages like PHP, which depends on client side action to be able to draw, are also out of the basket. Secondly we will need to draw very simple shapes (mainly pixel alike) in a large quantity, which means that we don't need complex 3D render technics or polygon like software such as WebGL, ThreeJS and such. Thirdly We don't need to perform a lot of complex mathematical operations (such as integration, derivative, or trigonometry), as the agents will be evolving in a 2D plan. Finally, it is very likely that threads will be useful in the simulation (controlling the time, nests and such), so we need a language where using these is more or less easy. This conclude a first good definition of preliminary needs.

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/sim1.png?raw=tru" alt="alt text" title="simulation rep 1" style="zoom:100%;" />

Given that I do not master every languages that exist and since this project is not about the  discovering and use of a new language, this narrows down the scope even more. In the above section we got rid of the low-level languages and the server-side ones since they would only add more complexity in an already quite complex task. This leaves me with Javascript, Python and Java, three interesting candidates. From there, it is more of a personal choice than an actual language to language comparison. Each of these three languages implement drawing technics and can perform all of the above described needs. I will nonetheless explain the advantages and inconveniences of each, based on my personal experiences and knowledges acquired throughout my developer’s life. 

 Let’s start with Python. Python is a very light and high-level language and is surprisingly simple and satisfying to work with. Being non-typed and almost “Human language” alike makes it a very appealing language to choose. It has good support of threads and includes some powerful (yet, unknown to me) drawing frameworks such as PyGame or Arcade. Python almost look like the perfect candidate. However, it is the slowest of the three at “Calculation steps per seconds” (as shown in Figure N), which is highly important when one needs to create a simulation as it will defined how much item can the program handle at a given time T. That being said, Python remain quite an interesting candidate, but ultimately not the one which will be used for the simulation. Secondly, Java. It is broadly known (which makes it one of the most documented language in the market) and can be used for more or less everything. It already implements a lot of structure, function, drawing technics and basic graphic tools because it has been designed to be a somewhat higher-level version of C with oriented object programming. It uses the JVM (Java Virtual Machine) to run the Java compiled bytecode which adds a lot of overhead at the start compared to interpreted languages (but saving you from dummy mistakes). It however has the highest “Calculation steps per second” score compared to the two others as Figure N demonstrates it. All of that being said, Java would almost be the perfect candidates. The only downside one could really think of is the lack of “good” drawing frameworks. It becomes quickly frustrating to work with drawing and threading in Java (but this is highly personal). Finally Javascript. Javascript is the kind of candidate who is a clever mixt between the advantages of Java and Python. It has a good “Calculation steps per second” score, it is easy to use and web based. Being web-based means that it is rather easy to deploy [more on that]. It has a good community and support a lot of user-made libraries, plus its documentation is also very great (as Python and Java). It has a very good vanilla drawing libraries and very good drawing frameworks such as Preprocess that can be used on top of VanillaJS

 

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



## To include in it

### introduction

"From what we been discussing in the "ant" section "...

- Passing day
- Being able to pause it and to click on any entity to get its details??
- Nomadic and stationary phase of an army ant colony
- Include heat and night/day period? 

- Include small difference in terrain height?

- Include seasons?

should we have no nest in start and workers have to create it by gathering dirt (can look back at the simple rule to building structure from the article). 

In the Pharaoh wikipedia page, they say that around  8 am scout go search for food, this should somehow be included in the brain of the ant. So that the simulation would look even more accurate. (Like in the night time nothing much appears, and then suddenly when sun appears, scout go search for food).



From https://en.wikipedia.org/wiki/Carpenter_ant

### Pheromones [[source](https://en.wikipedia.org/w/index.php?title=Carpenter_ant)]

As in most other social insect species, individual interaction is heavily influenced by the queen. The queen can influence individuals with odors called [pheromones](https://en.wikipedia.org/wiki/Pheromones), which can have different effects. Some pheromones have been known to calm workers, while others have been known to excite them. Pheromonal cues from ovipositing queens have a stronger effect on worker ants than those of virgin queens.[[18\]](https://en.wikipedia.org/wiki/Carpenter_ant#cite_note-18)

We could imagine to have an excitement of pixel in a nest, close to a queen, expressing which pheormone is currently being diffused. (Juste une diffusion colorée de pixel aux alentours de la reine).

I think the idea is to first be able to generate one colony and see it construct/gather food and breed workers. Implement the war rules as well.

**A lot of the "to include in" are not specifically cited above, look at the object for more**

## Sketch of model

```javascript
// This is an abstract implementation of objects / classes

World {
	var is_day
  var zoom? // might be useful to scale every pixel
	var temperature
	var day
	var season
	var time
	var speed
  var is_paused
  var global_population_increase_rate
  var global_population
	Nest nests[]
	Terrain terrain
	...
}

Terrain {
	var width
	var height
	Pixel map[width][height]
	...
}

Pixel {
	var height
	var type // Nest, food, ...
  var label[{
    colony : '',
    magnitude : int
  }] // Chemical left by ant, if exists.
	...
}
  
Task {
  var id
  var description
  ...
}

Nest {
  var origin // pos(x,y) of the very first pixel of the nest
	var surface
	var health
	var population_increase_rate
    
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
    var type
    var health
    var size
    var strenght // hit
    var speed
		var walk_randomness // To what extend the ant walks straight
    var has_task
    var current_task
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

# Robotic

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

## In my case

Replicated few learnt behaviours in a robot?

### Talk about the mini swarm robot ITU has 

### The limitation of the technology and cost

- [Robot that can replicate swarm behaviours](https://newatlas.com/colias-swarm-robot/33897/)

# Conclusion

The study of the living things mechanisms is called biomimetic. This art of replicating what nature does has enabled us to ....

# References

[1] [Phylogeny of the Ants: Diversification in the Age of Angiosperms, 2005](https://www.google.com/url?q=https%3A%2F%2Fpdfs.semanticscholar.org%2Fd186%2Fbbe2881027f99bbf1001c240f71f93baf6af.pdf&sa=D&sntz=1&usg=AFQjCNEw7aEhyFLFdE30DEsnv__kmTpbgA)

[2] [Ancient Ants Arose 140-168 Million Years Ago; Insects Needed Flowering Plants To Flourish, 2006](https://www.google.com/url?q=https%3A%2F%2Fwww.sciencedaily.com%2Freleases%2F2006%2F04%2F060407144825.htm&sa=D&sntz=1&usg=AFQjCNFl6IpckBVsLxDdvSME-ZkG-UyVoA)

[3] [Why is eusociality an almost exclusively terrestrial phenomenon?, 2014](https://www.google.com/url?q=https%3A%2F%2Fbesjournals.onlinelibrary.wiley.com%2Fdoi%2Ffull%2F10.1111%2F1365-2656.12251&sa=D&sntz=1&usg=AFQjCNH4eGixi40S7Pc4igMwqapbbocvxA)

[4] [Ant Ecology, 2010](https://books.google.de/books?hl=de&lr=&id=vlwVDAAAQBAJ&oi=fnd&pg=PR5&dq=10,000+trillion+ants&ots=aUqWFkzcGi&sig=Jhxc-cjuCLNaBqW7mf3kRWFJcZA#v=onepage&q=10%2C000trillion&f=false)

[5] [In search of ant ancestors, 2000](http://www.google.com/url?q=http%3A%2F%2Fwww.pnas.org%2Fcontent%2F97%2F26%2F14028.full&sa=D&sntz=1&usg=AFQjCNF1qJJu_HfDjQmCj-yjulkC35QH-g)

[6] [Why Ants Rule the World, Corey Binns, 2006](https://www.livescience.com/747-ants-rule-world.html)

[7] [The Remarkable Self-Organization of Ants, 2014](https://www.quantamagazine.org/ants-build-complex-structures-with-a-few-simple-rules-20140409/)

[8] [Army ant, 2008](http://www.newworldencyclopedia.org/entry/Army_ant)

[9] [Deadly Army Ants Decimate Entire Ecosystems, 2018](https://roaring.earth/deadly-army-ants/)

[10] [Wikipedia, army ants](https://en.wikipedia.org/wiki/Army_ant)

[11] [How Ants Wage War, 2011](https://www.pri.org/stories/2011-11-16/how-ants-wage-war)

---

**Youtube**

- https://www.youtube.com/watch?v=0FZLPbBDYAA&ab_channel=wocomoWILDLIFE
- https://www.youtube.com/watch?v=QO3yKYC305g&ab_channel=KineticSand

**Kurzgesagt - In a Nutshell**

- The World War of the Ants - The Army Ant

- The Warrior Kingdoms of the Weaver Ant

- The Billion Ant Mega Colony and the Biggest War on Earth

**Mega source**

- https://sites.google.com/view/sources-argentine-ants
- https://sites.google.com/view/sourcesweaverants
- https://sites.google.com/view/sources-world-war-ants/

**Ants**

- https://pdfs.semanticscholar.org/d186/bbe2881027f99bbf1001c240f71f93baf6af.pdf

**Army ants**

- https://www.sciencedirect.com/topics/agricultural-and-biological-sciences/army-ant


**Swarm robotic**

- https://www.frontiersin.org/articles/10.3389/frobt.2020.00036/full

Pic: java step calc

- http://dvschroeder.blogspot.com/2013/07/java-vs-javascript-vs-python.html
