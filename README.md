```
NOK = Not Ok 

MOK = More or less ok

OK = Done.

NRV = Need revision (grammar and spelling)

[Nothing] = Actually not ok but I was just too lazy to write [NOK] or [MOK]
```

# Question for supervisor

Even though mechanisms havent' been discovered, I can "imagine" how it works

1. In the regard of Q[DELETED], we could imagine the simulation to be: 1 colony of army ants, with their behaviours, fighting again other colonies of a diffrent species ?
2. A bit hard of a question but, how much hours a week do you expect me to work at least? That would really help.

Have a look on what exist, what does not (in their mechanisms).

Look at other insects (their algorithms), to see how people asbtract and implement algorithm based on quite vague information they know about the mechanisms

# TODO

Do research on

## Biology

- [ ] Wood ants
- [ ] Some species like black crazy ants and pheroe ants have multiple queen within a singe colony
- [ ] Leaf cutter ants
- [ ] The Queen in an ant colony
- [ ] Carpenter ant
- [x] Army ants

## PEOPLE

- [ ] [Alex wild, photographer and researcher](https://www.alexanderwild.com)

### To read

https://www.cell.com/current-biology/pdf/S0960-9822(06)01834-3.pdf (communication in ants)

# Introduction

## The context [NOK]

This project is part of the "[Research project (K-CS and K-SD) Autumn 2020 (KIREPRO1PE)](https://learnit.itu.dk/course/view.php?id=3020186)" ITU course. The aim is to create a preliminary work for a Master thesis.

## The subject [NOK]

This project aims on studying the abstract mechanisms employed by ants during attack between colonies of given species. Ants are one of the various social species that can be studied to create bioinspired algorithms and models of collective behaviors. They are very interesting because as a single unit, an ant is a very simple being, but as a swarm they show a lot of exciting collective behaviours and their underlying mechanisms can be studied and used for everyday problems.

The art of studying the nature to replicate its behaviors into robotic to solve complex human problems is called Bio-inspired robotic (or more commonly “Biomimetic”). There are numerous examples such as the very famous “Japanese Bullet train” (Shinkansen) which gets its nose design from the Kingfisher bird’s beak (who’s aerodynamic ), reducing the train’s energy consumption by 15%, making it 10% faster and quieter. 

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/bullet_train.jpg?raw=true" alt="alt text" title="The Shinkansen bullet train" style="zoom:25%;" />

or the hook and loop fastener (also known as the Velcro), created by the Swiss engineer George de Mestral in the 1950s. This two part binding system was inspired by burrs, which de Mestral studied under microscope after he figured how surprisingly easy these would stick to its dog's hair. He discovered that burrs had micro hook that were able to catch anything with a loop.

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/burrs.jpg?raw=true" alt="alt text" title="Burrs and their loops" style="zoom:60%;" />

Nowadays, the hook and loop fastener is used throughout the world.

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

Even though it exists thousands of species, ant colonies have a somewhat structured and space-and-time proof hierarchy.

- Scout
- Queen
- Soldier
- Worker
- Larvae
- Drones (Their only purpose is to mate with the queen)
- Winged male, once they mature live colony in swarms to create new colonies. We could imagine that the newly created colony could enter war with the original one (after a few gene epoch)

## The army ants

From all the known ants species, there is a category of ant legitimately called "the army ants". This category, that the "evolutionary tree" has brought to be combatants, are dreadful warriors among the ground. They have been given large mandibles, painful sting and armour, and it exists about 200 hundred of species. They don't have a nest, they rather crawl on the ground in a very long and narrow group, consuming up to 500'000 prey animals each day.

**behaviour**

Interestingly enough, army ants do not fight between them. When encountered in the nature, they pretend like the other colony do not exist. This makes sense from an evolutionary stand points, as throughout time, army ants that were attacking other army ants eradicate themselves to extinction. 

Army ants adopt what scientist call a "Nomadic live style", which consist of..

**structure in the colony**

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

### Carpenter ants

https://en.wikipedia.org/wiki/Carpenter_ant#Behavior_and_ecology

They have a primary nest and create satelite nest

Only eggs, the newly hatched [larvae](https://en.wikipedia.org/wiki/Larvae), workers, and the queen reside in the primary nests

### Wood ants

### Leaf cutter ants

### Black crazy ants

### Pheroe ants



-----

## Q

Q: Should we add insects like wasps and bees?



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

## To include in it

- Passing day
- Being able to pause it and to click on any entity to get its details??

I think the idea is to first be able to generate one colony and see it construct/gather food and breed workers. Implement the war rules as well.

```javascript
// This is an abstract implementation of object

World {
	var is_day;
	var temperature;
	var day;
	var season;
	var time;
	var speed;
  var is_paused;
	Nest nests[];
	Terrain terrain;
	...
}

Terrain {
	var width;
	var height;
	Pixel map[width][height];
	...
}

Pixel {
	var height;
	var type; // Nest, ant, food, ...
	...
}

Nest {
	var size;
	var food_supply;
	var health;

	var nb_eggs;
	
	Colony colony;
	...
}

// Colony of ants
Colony {
	var color; // which refers to the chemical attributes
	var nb_ants;
	Queen queens[]; // One or many queens
	Worker workers[]; 
	...
}

Ant {
    var type;
    var health;
    var size;
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
```

## Introduction

## Exploration of Language and drawing frameworks [NOK] [NRV] 

Many technics can be used to build a good simulator, and yet, it is difficult for one to select the best within the ocean of languages and framework that exists. Many of these usually fit specifics kinds of implementation. This chapter is a deep through of some of the most relevant ones. We will go deeper on the understanding of a good drawing tool in the specific case of the ant war simulation, and this will also be the occasion to have 

we *will also get to know many of the existing* tools that are out there. => too much "tool", but need to elaborate more on what the chapter is about.

The first step before plunging into google and look at every language and framework that exists is to specify the needs. As we have not yet a good understanding of the complexity of the simulation (this problem will arise later in the development), one needs to think on a more abstract level. Figure [N] is a first very simple high-level representation of an ongoing war in the simulator. Firstly, we need to be able to draw. This might sound a bit too abstract but it already narrows down the scope as many languages such as C or C++ are low-level language, which would only add more complexity to the project (don't get me wrong, one can use these language to draw, but here are a lot of easier ways to do it with higher-level languages), or server side languages like PHP, that depends on client side action to be able to draw. Secondly We will need to draw very simple shapes (mainly pixel alike) in a large quantity, which means no need for complex 3D render technics or polygon like software. Thirdly We don't need to perform a lot of complex mathematical operations (such as integration, derivative, or trigonometry), as the agents will be moving in a 2D plan. Finally, As discussed in the previous chapter, we won't need / we will need to use the concurrent process as.... 

<img src="https://github.com/alevani/ant_war_simulation/blob/master/assets/img/sim1.png?raw=true" alt="alt text" title="simulation rep 1" style="zoom:100%;" />

This conclude a first good definition of preliminary needs. 

**Languages**

Languages that I will be going through -> because I know them the best. This thesis is meant to create a simulator, not spend time on discovering a new language 

- Python (pygame, acade)
- Java
- Javascript (vanilla, preprocessing, webgl, treeJS)

**Javascript**

- Top 1 candidate
- Even vanilla javascript is super good a drawing in canvas.
- WebGL and TreeJS are good but they are optimised for 3D render and we don't need that
- Preprocessing is a very nice and easy library that one can use on top of vanilla JS
- Light and Web based language (easy to deploy, test and maintain)
- Powerful, even for math based simulation

**Python**

- Top 2 candidate
- Powerful
- Some powerful drawing frameworks such as PyGame or Arcade
- Light

**Java**

- Top 3 candidate
- Java implements framework such as swing and very basic graphics tool
- Heavy language

## Interesting collective behaviours to replicate and can be included in the simulation

- Nomadic and stationary phase of an army ant colony

- Include heat and night/day period? 

- Include small difference in terrain height?

- Include seasons?

should we have no nest in start and workers have to create it by gathering dirt (can look back at the simple rule to building structure from the article). 

## Sketch of model

## POC?

# Robotic

## Swarm robotic

Swarm robotic is the art of collectively run a lot of robots to solve problems by forming complex structures and behaviors such as the one observed in nature.

## State of art

## In my case

### Talk about the mini swarm robot ITU has 

### The limitation of the technology and cost

- [Robot that can replicate swarm behaviours](https://newatlas.com/colias-swarm-robot/33897/)

# Conclusion

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







