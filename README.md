[TOC]

This project is part of the ITU 2020 "Research project" course. This paper is about [Study on ants collective mechanisms during war between colonies of the same species](https://learnit.itu.dk/course/view.php?id=3020439#section-0)

```
NOK = Not Ok 

MOK = More or less ok

OK = Done.

[Nothing] = Actually not ok but I was just too lazy to write [NOK] or [MOK]
```

# Question for supervisor

1. We need to define to what extent the simulation will be accurate. Because there's a lot of small cool behaviours but that only apply to few species or, some species are really interesting but some behaviour totally counter the good of simulation (like; army ants do not fight together, or they don't have nest). I need to keep in mind that I am not a biologist but a engineer, that is, accuracy is less important (but still to take into consideration)
2. In the regard of Q1, we could imagine the simulation to be: 1 colony of army ants, with their behaviours, fighting again other colonies of a diffrent species ?
3. A bit hard of a question but, how much hours a week do you expect me to work at least? That would really help.

# TODO

Do research on

## Biology

- [x] Wood ants
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

This project aims on studying the abstract mechanisms employed by ants during attack between colonies of the same species. Ants are one of the various social species that can be studied to create bioinspired algorithms and models of collective behaviors. They are very interesting because as a single unit, an ant is a very simple being, but as a swarm they show a lot of exciting collective behaviours and their underlying mechanisms can be studied and used for everyday problems.

## The subject [NOK]

what will be studied and why

Bio-inspired robotic (or more commonly “Biomimetic”) is the art of studying the nature to replicate its behaviors into robotic to solve complex human problems. There are numerous examples such as the very famous “Japanese Bullet train” (Shinkansen) which gets its nose design from the Kingfisher bird’s beak (who’s aerodynamic ), reducing the train’s energy consumption by 15%, making it 10% faster and quieter. Other examples are the use of insect-inspired algorithms for coordination within groups of robots, on land, air, or even underwater.

## Goals [NOK]

what should be the learning outcome and product outcome

## State of art [NOK]

what exists?

Even though biomimetic on ants is a very studied topic with numerous papers, videos and books about the subject, there is no proper implementation of an ant war simulator. The closest implementations of it are simulations of pathfinders (here is an example found on Github: http://bwiklund.github.io/ant-simulator/). It is very likely that this project will be a reflection of all the studies, such as “Combat between large derived societies: A subterranean army ant established as a predator of mature leaf-cutting ant colonies” written by Scott Powell or “The Remarkable Self- Organisation of Ants”, written by Emily Singer.

https://github.com/computationalcore/ants-simulation -> nice! ant colony simulator, the brain of each ant is fairly simple but that's a start

https://github.com/karask/AntSim -> could be useful but poorly documented

http://ants.aichallenge.org/

https://github.com/ultimape/PixelAntColony

write way more here, find examples video and relevant study on the subject

# Ants

> Fact: Each ant will belong to a nest and that's how they now if another ant is enemy or not. Surely nature use more sophisticated way for it, but I am not a biologist.

[Some species of ant have queen that lay up to 1000 eggs a day for up to seven years](https://www.terminix.com/blog/education/what-is-an-ant-colony/) -> That could give me information on of much eggs to breed in one epoch

#### Subtype

- Scout
- Queen
- Soldier
- Worker
- Larvae
- Drones (Their only purpose is to mate with the queen)
- Winged male, once they mature live colony in swarms to create new colonies. We could imagine that the newly created colony could enter war with the original one (after a few gene epoch)

## Some interesting ants I could take behaviour from

### Carpenter ant

https://en.wikipedia.org/wiki/Carpenter_ant#Behavior_and_ecology

They have a primary nest and create satelite nest

Only eggs, the newly hatched [larvae](https://en.wikipedia.org/wiki/Larvae), workers, and the queen reside in the primary nests

### Army ants

> Now it seems pretty obvious that I will use them, in regards of Q2. https://en.wikipedia.org/wiki/Army_ant#/media/File:Army_ant_Eciton_Burchelli.svg has a lot of SUPER interesting stuff about them. I of course need to further study them (more that what wikipedia, that is). Super super nice.

https://www.youtube.com/watch?v=7_e0CA_nhaE&ab_channel=Kurzgesagt%E2%80%93InaNutshell

- "200 diff species"

- They don't really build nest.
- 5000

#### Type

- Neotropical Army Ants
- Army Ant solider
- Bullet Ant
- Giant Amazonian Ant

> ! Army ants do not fight army ant :(

https://en.wikipedia.org/wiki/Army_ant

**Army ant syndrome**

Usually ant colony would send one scout to look for food or threat, army ants send a leaderless group of foragers to detect and overwhelm the prey at once

#### from wikipedia -> Nomadic and stationary phase

Army ants have two phases of activity—a nomadic (wandering) phase and a stationary (statary) phase—that constantly cycle, and can be found throughout all army ants species.[[8\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Franks&Nigel&Holldobler_1987-9)

The nomadic phase begins around 10 days after the queen lays her eggs. This phase will last approximately 15 days to let the larvae develop. The ants move during the day, capturing [insects](https://en.wikipedia.org/wiki/Insects), [spiders](https://en.wikipedia.org/wiki/Spiders), and small [vertebrates](https://en.wikipedia.org/wiki/Vertebrates) to feed their brood. At dusk, they will form their nests or bivouac, which they change almost daily.[[8\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Franks&Nigel&Holldobler_1987-9) At the end of the nomadic phase, the larvae will spin pupal cases and no longer require food. The colony can then live in the same bivouac site for around 20 days, foraging only on approximately two-thirds of these days.[[2\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Schneirla,_T._C._1971-2)[[8\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Franks&Nigel&Holldobler_1987-9) Among the army ants are some species that venture out only at night, but no adequate studies of their activities have been made.

The stationary phase, which lasts about two to three weeks, begins when the [larvae](https://en.wikipedia.org/wiki/Larvae) pupate. From this point on, the prey that were previously fed to the larvae are now fed exclusively to the queen.[[8\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Franks&Nigel&Holldobler_1987-9) The abdomen ([gaster](https://en.wikipedia.org/wiki/Gaster_(insect_anatomy))) of the queen swells significantly, and she lays her eggs. At the end of the stationary phase, both the pupae emerge from their cocoons ([eclosion](https://en.wikipedia.org/wiki/Eclosion)) and the next generation of eggs hatch so the colony has a new group of workers and larvae. After this, the ants resume the nomadic phase.[[5\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Gotwald,_William_H._1982-6)[[8\]](https://en.wikipedia.org/wiki/Army_ant#cite_note-Franks&Nigel&Holldobler_1987-9)

**Very interesting, could be added to the simulation that's quite fun**

## Q

Q: Should we add insects like wasps and bees?



### Queen

If there is multiple queens, workers might kill all of them but one at some point. Queens will produce fewer workers so that they have more fighting power if needed

https://www.livescience.com/10635-queen-ant-sacrifice-colony-retain-throne.html

-------

Some ants keep "domestic animals" who generate honey for them. They carry them along.

https://www.livescience.com/747-ants-rule-world.html

- Ants emerged 120 millions years ago but really became something big only 60 millions years after

- about 20'000 ant species (11'000 classified, 1/3 of all insect biomass)

- They adapt to each env, that's why they exist everywhere.

>  They come in a range of colors from yellow and red to black. They exist in deserts, rain forests, and swamps—anywhere but the coldest and highest places on Earth.

Many ants feed from flowering plants rich in carbohydrates

Some carpenter species construct defensive shelters around base of plants to guard them from other insects (food supply protection, could be cool to implement)

- Hymenoptera, females do all the work

https://www.quantamagazine.org/ants-build-complex-structures-with-a-few-simple-rules-20140409/

-> they talk about structure and bio robotic, not the same topic but it could be relevant to write a bit about it here.

https://www.sciencedaily.com/releases/2007/10/071009212548.htm

https://theconversation.com/leafcutter-ants-are-in-a-chemical-arms-race-against-a-behaviour-changing-fungus-97892

-short introduction on ants, the species, the population, why they are interesting

# Mechanisms

## Individual

short paragraph explaining what an ants alone can do (not a whole lot)

**source ytb**

Scout find food and mark the way (also here https://www.youtube.com/watch?v=NJ3pLY819hA&ab_channel=TerraMater) 

for surface extension, they send scout, once scout from each colonies encounter they rush to their nest and ring the alarm.

## Collective

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

I think the idea is to first be able to generate one colony and see it construct/gather food and breed workers. Implement the war rules as well, then it should be failry easy to create a new object nest. and see how they behave

```javascript

// draft object, more to add§
Nest[] {

size, nb_eggs, food_supply, "health", 

	colony {
		nb_ants,
    ants [] {
      type, health,size, traits
    }
	}

}
```

**Maybe we could have multiple species each with their own properties for individuals, cause it could be interesting to see their behaviours as well. as for instance, if too much of ants there is of one colony at a specific location, then some ants from other colonies/species will be afraid of getting close (number is power?)**

## Introduction

## Exploration of framework and drawing techniques

I am doing some test on multiple drawing technics at https://github.com/alevani/random-agents

- Graphical

- comparisons

## Intersesting colletive behaviours to replicate

should we include heat and night/day periode? 

Should we inlcude small diffrence in terrain height?

Should we inlcude seasons?

should we have no nest in start and workers have to create it by gathering dirt (can look back at the simple rule to building strucutre from the article). 

## Sketch of model

## POC?

# Robotic

[Robot that can replicate swarm behaviours](https://newatlas.com/colias-swarm-robot/33897/)

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



<style>
  h2 {border: solid 0px}
</style>

