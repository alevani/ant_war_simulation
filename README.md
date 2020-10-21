```
NOK = Not Ok 

MOK = More or less ok

OK = Done.

NRV = Need revision (grammar and spelling)

[Nothing] = Actually not ok but I was just too lazy to write [NOK] or [MOK]
```

# TODO

Do research on

## Biology

- [x] Wood ants
- [x] Some species like black crazy ants and pheroe ants have multiple queen within a singe colony
- [x] Leaf cutter ants
- [ ] The Queen in an ant colony
- [x] Carpenter ant
- [x] Army ants
  - [ ] What type of pheromones do they have
    - [ ] To they use repellent pheromones?
  - [ ] How do they scout and go back to the nest (foraging)
- [ ] How ants organise
- [ ] How ants communicate
  - [ ] How and what type of ant pheromones exist?
- [ ] Ant Pathfinder 
- [ ] Does army ant have a night/day cycle? If yes, use it for simulation.
- [ ] Ant task allocation
- [ ] Operating cost of task -> https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5255904/

## PEOPLE

- [ ] [Alex wild, photographer and researcher](https://www.alexanderwild.com)

## Tech

- [] https://www.argos-sim.info/

### To read

https://www.cell.com/current-biology/pdf/S0960-9822(06)01834-3.pdf (communication in ants)

# Introduction [NOK]

This project is part of the "[Research project (K-CS and K-SD) Autumn 2020 (KIREPRO1PE)](https://learnit.itu.dk/course/view.php?id=3020186)" ITU course which intend as a bridge between the specialisation course and the master thesis (that is, a preliminary work for the Master thesis). Its aim is the study of the abstract mechanisms employed by ants during attack between colonies of given species. Ants are one of the various social species that can be studied to create bioinspired algorithms and models of collective behaviors. They are very interesting because as a single unit, an ant is a very simple being, but as a swarm they show a lot of exciting collective behaviours and their underlying mechanisms can be studied and used for everyday problems.

The art of studying the nature to replicate its behaviors into robotic to solve complex human problems is called Bio-inspired robotic (or more commonly “Biomimetic”). There are numerous examples such as the very famous “Japanese Bullet train” (Shinkansen) which gets its nose design from the Kingfisher bird’s beak (who’s aerodynamic ), reducing the train’s energy consumption by 15%, making it 10% faster and quieter. 

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/bullet_train.jpg?raw=true" alt="alt text" title="The Shinkansen bullet train" style="zoom:25%;" />

The hook and loop fastener (also known as the Velcro), created by the Swiss engineer George de Mestral in the 1950s is also a very famous example of biomimetic. This two part binding system was inspired by burrs, which de Mestral studied under microscope after he figured how surprisingly easy these would stick to its dog's hair. He discovered that burrs had micro hook that were able to catch anything with a loop. Nowadays, the hook and loop fastener is used throughout the world.

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/burrs.jpg?raw=true" alt="alt text" title="Burrs and their loops" style="zoom:60%;" />



Other examples are the use of insect-inspired algorithms for coordination within groups of robots, on land, air, or even underwater.





https://asia.nikkei.com/Business/Companies/Japan-s-fastest-bullet-train-to-squeeze-out-trip-every-5-minutes2 -> Japanese bullet train picture

## Goals [NOK]

what should be the learning outcome and product outcome

Explain that it won't be a SUPER very accurate simulation, I'm an engineer not a biologist. But the tool will be opensource and it should be easy to define and change sets of rules <----- Maybe the rules will be a decision tree that any dev could change and see the output through the simulation.

## State of art [NOK]

Even though biomimetic on ants is a very studied topic with numerous papers, videos and books about the subject, there is no proper implementation of an ant war simulator. The closest implementations are simulations of pathfinders (here is an example found on Github: http://bwiklund.github.io/ant-simulator/) or very low level territory defence demonstration (such as https://github.com/computationalcore/ants-simulation). 



https://github.com/computationalcore/ants-simulation -> nice! ant colony simulator, the brain of each ant is fairly simple but that's a start

https://github.com/karask/AntSim -> could be useful but poorly documented

http://ants.aichallenge.org/

https://github.com/ultimape/PixelAntColony

write way more here, find examples video and relevant study on the subject

# 



It is very likely that this project will be a reflection of all the studies, such as “Combat between large derived societies: A subterranean army ant established as a predator of mature leaf-cutting ant colonies” written by Scott Powell or “The Remarkable Self- Organisation of Ants”, written by Emily Singer.

# The ant kingdom

Throughout this chapter, we will go through the history of ants, what they are and wha they account for. ... various species that could be interesting to study and use for the simulation

Introduction to the chapter? Like this chapter will go thought that, and that, and blah blah blah..Jan's style ;) (sorry if you see this <3) (something like above)

Ants are ancient being that emerge around 140 to 168 millions years ago, even though they really started to diversify only about some 60 millions years after. From the many known species -> this is not so English, ants form the very first insect super kingdom. They are estimated to be about 10'000'000'000'000'000 (10'000 trillion) individuals, which account for 20% of the total animal biomass. This super kingdom, however, is far from being a unified heaven. From the 11'000 classified species and the 20'000 estimated species, rare are the ants that get along together.

[a few examples of ants getting along and ants not getting along?]



Individually, and ant can't do much.

- One ant alone is nothing, they are like humain, they need collaboration to survive and evolve

>  They adapt to each env, that's why they exist everywhere.

https://www.livescience.com/747-ants-rule-world.html

>  They come in a range of colors from yellow and red to black. They exist in deserts, rain forests, and swamps—anywhere but the coldest and highest places on Earth.

> Fact: Each ant will belong to a nest and that's how they now if another ant is enemy or not. Surely nature use more sophisticated way for it, but I am not a biologist.

[Some species of ant have queen that lay up to 1000 eggs a day for up to seven years](https://www.terminix.com/blog/education/what-is-an-ant-colony/) -> That could give me information on of much eggs to breed in one epoch

#### Subtype

Even though it exists thousands of species, ant colonies have a somewhat structured and space-and-time proof hierarchy. (It may variate but mostly the same)

- Scout
- Queen
- Soldier
- Worker
- Larvae
- Drones (Their only purpose is to mate with the queen)
- Winged male, once they mature live colony in swarms to create new colonies. We could imagine that the newly created colony could enter war with the original one (after a few gene epoch)

## How do ants organize

## how do ants communicate

## How do  ants distribute task

## The army ants

! Say that it's gonna be the main species of the simulator due to its very various interesting behaviours.

From all the known ants species, there is a category of ant legitimately called "the army ants". This category, that the "evolutionary tree" has brought to be combatants, are dreadful warriors among the ground. They have been given large mandibles, painful sting and armour, and it exists about 200 hundred of species. They don't have a nest, they rather crawl on the ground in a very long and narrow group, consuming up to 500'000 prey animals each day.

**behaviour**

Interestingly enough, army ants do not fight between them. When encountered in the nature, they pretend like the other colony do not exist. This makes sense from an evolutionary stand points, as throughout time, army ants that were attacking other army ants eradicate themselves to extinction. 

Army ants adopt what scientist call a "Nomadic live style", which consist of..

**structure in the colony** -> check if it's the correct structure for the army ant

- Workers
- Soldiers
- Males
- Queen

Why they are interesting over other species



### Army ants

> Now it seems pretty obvious that I will use them, in regards of Q2.  has a lot of SUPER interesting stuff about them. I of course need to further study them (more that what wikipedia, that is). Super super nice.

- "200 diff species"
- They don't really build nest.
- 5000 -> 5000 what?
- Large mandibles and painful sting

#### Type -> some pic

- Neotropical Army Ants => specialised in hunting other insects (wasp, termite, other ants)
- Army Ant solider
- Bullet Ant
- Giant Amazonian Ant

> ! Army ants do not fight army ant :(



https://en.wikipedia.org/wiki/Army_ant

**Army ant syndrome**

<img src="https://ars.els-cdn.com/content/image/3-s2.0-B9780128015322000143-f14-29-9780128015322.jpg?_" alt="alt text" title="simulation rep 1" style="zoom:100%;" />

Usually ant colony would send one scout to look for food or threat, army ants send a leaderless group of foragers to detect and overwhelm the prey at once

#### from wikipedia -> Nomadic and stationary phase

Army ants have two phases of activity—a nomadic (wandering) phase and a stationary (statary) phase—that constantly cycle, and can be found throughout all army ants species.[[8\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Franks&Nigel&Holldobler_1987-9)

The nomadic phase begins around 10 days after the queen lays her eggs. This phase will last approximately 15 days to let the larvae develop. The ants move during the day, capturing [insects](https://en.wikipedia.org/wiki/Insects), [spiders](https://en.wikipedia.org/wiki/Spiders), and small [vertebrates](https://en.wikipedia.org/wiki/Vertebrates) to feed their brood. At dusk, they will form their nests or bivouac, which they change almost daily.[[8\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Franks&Nigel&Holldobler_1987-9) At the end of the nomadic phase, the larvae will spin pupal cases and no longer require food. The colony can then live in the same bivouac site for around 20 days, foraging only on approximately two-thirds of these days.[[2\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Schneirla,_T._C._1971-2)[[8\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Franks&Nigel&Holldobler_1987-9) Among the army ants are some species that venture out only at night, but no adequate studies of their activities have been made.

The stationary phase, which lasts about two to three weeks, begins when the [larvae](https://en.wikipedia.org/wiki/Larvae) pupate. From this point on, the prey that were previously fed to the larvae are now fed exclusively to the queen.[[8\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Franks&Nigel&Holldobler_1987-9) The abdomen ([gaster](https://en.wikipedia.org/wiki/Gaster_(insect_anatomy))) of the queen swells significantly, and she lays her eggs. At the end of the stationary phase, both the pupae emerge from their cocoons ([eclosion](https://en.wikipedia.org/wiki/Eclosion)) and the next generation of eggs hatch so the colony has a new group of workers and larvae. After this, the ants resume the nomadic phase.[[5\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Gotwald,_William_H._1982-6)[[8\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Franks&Nigel&Holldobler_1987-9)

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

I think an important focus will be to define what ants can do, e.g:

- Breed
- Food supply
- Attack and raid (to steal egg and kill workers/queen(s))
- Generally it seems that first only soldier go to war, workers remain in nest or create barricades in case of invasion

and then spend some time on EACH of these point and document them. building algorithms maybe? I shall see.

**war**

multiple ants can team up on one enemy ant to kill it (https://www.youtube.com/watch?v=NJ3pLY819hA&ab_channel=TerraMater)



each colony has its own chemical badge (that's how they know if they are enemy or not)

# Building a simulator

## Introduction

## Exploration of Language and drawing frameworks [NOK] [NRV] 

Many technics can be used to build a good simulator, and yet, it is difficult for one to select the best within the ocean of languages and framework that exists. Many of these usually fit specifics kinds of implementation. This chapter is a deep through of some of the most relevant ones. We will go deeper on the understanding of a good drawing tool in the specific case of the ant war simulation and this will also be the occasion to have a first sight at the overall implementation.

The first step before plunging into google and look at every language and framework that exists is to specify the needs. As we have not yet a good understanding of the complexity of the simulation (this problem will arise later deeper phases), one needs to think on a more abstract level. Figure [N] is a first very simple high-level not to scaled representation of an ongoing epoch in the simulator. Firstly, we need to be able to draw. This might sounds a bit too abstract but it already narrows down the scope as many languages such as C or C++ are low-level language, which would only add more complexity to the project (don't get me wrong, one can use these languages to draw, but there are a lot of easier ways to do it with higher-level languages). Server side languages like PHP, which depends on client side action to be able to draw, are also out of the basket. Secondly we will need to draw very simple shapes (mainly pixel alike) in a large quantity, which means that we don't need complex 3D render technics or polygon like software such as WebGL, ThreeJS and such. Thirdly We don't need to perform a lot of complex mathematical operations (such as integration, derivative, or trigonometry), as the agents will be evolving in a 2D plan. Finally, it is very likely that threads will be useful in the simulation (controlling the time, nests and such), so we need a language where using these is more or less easy. This conclude a first good definition of preliminary needs.

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/sim1.png?raw=true" alt="alt text" title="simulation rep 1" style="zoom:100%;" />

Given that I do not master every languages that exist and since this project is not about the  discovering and use of a new language, this narrows down the scope even more. In the above section we got rid of the low-level languages and the server-side ones since they would only add more complexity in an already quite complex task, this leaves me with JavaScript, Python and Java, three interesting candidates. From there, it is more of a personal choice than an actual language to language comparison. Each of these three languages implement drawing technics and can perform all of the above described needs. I will nonetheless explain the advantages and inconveniences of each, based on my personal experiences and knowledges I acquired throughout my developer’s life. 

 Let’s start with Python. Python is a very light, high-level language and is surprisingly simple and satisfying to work with. Being non-typed and almost “Human language” alike makes it a very appealing language to choose. However, python is the slowest of the three at “Calculation steps per seconds”, which is highly important when one needs to create a simulation, as it will defined how much item can the program handle at a given time T.

 Secondly, Java. It is broadly known (which makes it one of the most documented language in the market) and can be used for more or less everything. It already implements a lot of structure, function, drawing technics and basic graphic tools because it has been designed to be a somewhat higher-level version of C with oriented object programming. It uses the JVM (Java Virtual Machine) to run the Java compiled bytecode, which adds a lot of overhead at the start compared to interpreted languages, but saves you from dummy mistakes. It however has the highest “Calculation steps per second” score compared to the two others as Figure N demonstrates it. All of that being said, Java would almost be the perfect candidates. The only downside one could really think of is the lack of “good” drawing frameworks. It become quickly frustrating to work with drawing and threading in Java (but this is highly personal).

**Javascript**

- Top 1 candidate
- Even vanilla javascript is super good a drawing in canvas.
- WebGL and TreeJS are good but they are optimised for 3D render and we don't need that
- Preprocessing is a very nice and easy library that one can use on top of vanilla JS
- Light and Web based language (easy to deploy, test and maintain)
- Powerful, even for math based simulation
- Mid for calculation

**Python**

- Top 2 candidate
- Powerful
- Slowest at calculation
- Some powerful drawing frameworks such as PyGame or Arcade
- Light

**Java**

- Top 3 candidate
- Fastest at calculation
- Java implements framework such as swing and very basic graphics tool
- Heavy language



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

# Sources	

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

- https://en.wikipedia.org/wiki/Army_ant#/media/File:Army_ant_Eciton_Burchelli.svg

The army ant life cycle, and the book that goes with it => just cost about 3000$, so Ya know bye bye

- https://www.sciencedirect.com/topics/agricultural-and-biological-sciences/army-ant

- https://www.youtube.com/watch?v=7_e0CA_nhaE&ab_channel=Kurzgesagt%E2%80%93InaNutshell

**Swarm robotic**

- https://www.frontiersin.org/articles/10.3389/frobt.2020.00036/full

Pic: java step calc

- http://dvschroeder.blogspot.com/2013/07/java-vs-javascript-vs-python.html

# Question for supervisor

**4** is seems interesting that the more I wrote the more the subject differs from "wars". The simulator could just result in a very mid-accurate simulation, where "war" is a feature, but not the main one. To discuss



