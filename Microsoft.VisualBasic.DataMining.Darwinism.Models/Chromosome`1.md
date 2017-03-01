﻿# Chromosome`1
_namespace: [Microsoft.VisualBasic.DataMining.Darwinism.Models](./index.md)_

In computer programming, genetic representation is a way of representing 
 solutions/individuals in evolutionary computation methods. Genetic 
 representation can encode appearance, behavior, physical qualities of 
 individuals. Designing a good genetic representation that is expressive 
 and evolvable is a hard problem in evolutionary computation. Difference 
 in genetic representations is one of the major criteria drawing a line 
 between known classes of evolutionary computation.

 Terminology often comes by analogy With natural genetics. The block Of 
 computer memory that represents one candidate solution Is called an individual. 
 The data In that block Is called a chromosome. Each chromosome consists Of 
 genes. The possible values Of a particular gene are called alleles. A 
 programmer may represent all the individuals Of a population Using binary 
 encoding, permutational encoding, encoding by tree, Or any one Of several 
 other representations.

 Genetic algorithms use linear binary representations. The most standard one 
 Is an array Of bits. Arrays Of other types And structures can be used In 
 essentially the same way. The main Property that makes these genetic 
 representations convenient Is that their parts are easily aligned due To 
 their fixed size. This facilitates simple crossover operation. Variable 
 length representations were also explored In Genetic algorithms, but crossover 
 implementation Is more complex In this Case.

 Evolution strategy uses linear real-valued representations, e.g. an array 
 Of real values. It uses mostly gaussian mutation And blending/averaging 
 crossover.

 Genetic programming(GP) pioneered tree-Like representations And developed 
 genetic operators suitable For such representations. Tree-Like representations 
 are used In GP To represent And evolve functional programs With desired 
 properties.

 Human-based genetic algorithm (HBGA) offers a way to avoid solving hard 
 representation problems by outsourcing all genetic operators to outside 
 agents, in this case, humans. The algorithm has no need for knowledge 
 of a particular fixed genetic representation as long as there are enough 
 external agents capable of handling those representations, allowing for 
 free-form And evolving genetic representations.



### Methods

#### Crossover
```csharp
Microsoft.VisualBasic.DataMining.Darwinism.Models.Chromosome`1.Crossover(`0)
```
In genetic algorithms, crossover is a genetic operator used to vary the programming 
 of a chromosome or chromosomes from one generation to the next. It is analogous to 
 reproduction and biological crossover, upon which genetic algorithms are based. 
 Cross over is a process of taking more than one parent solutions and producing a 
 child solution from them. There are methods for selection of the chromosomes.

|Parameter Name|Remarks|
|--------------|-------|
|anotherChromosome|-|


#### Mutate
```csharp
Microsoft.VisualBasic.DataMining.Darwinism.Models.Chromosome`1.Mutate
```
Mutation is a genetic operator used to maintain genetic diversity from one generation 
 of a population of genetic algorithm chromosomes to the next. It is analogous to 
 biological mutation. Mutation alters one or more gene values in a chromosome from its 
 initial state. In mutation, the solution may change entirely from the previous solution. 
 Hence GA can come to better solution by using mutation. Mutation occurs during evolution 
 according to a user-definable mutation probability. This probability should be set low. 
 If it is set too high, the search will turn into a primitive random search.

 The classic example Of a mutation Operator involves a probability that an arbitrary bit 
 In a genetic sequence will be changed from its original state. A common method Of 
 implementing the mutation Operator involves generating a random variable For Each bit 
 In a sequence. This random variable tells whether Or Not a particular bit will be modified. 
 This mutation procedure, based On the biological point mutation, Is called Single point 
 mutation. Other types are inversion And floating point mutation. When the gene encoding 
 Is restrictive As In permutation problems, mutations are swaps, inversions, And scrambles.

 The purpose Of mutation In GAs Is preserving And introducing diversity. Mutation should 
 allow the algorithm To avoid local minima by preventing the population Of chromosomes 
 from becoming too similar To Each other, thus slowing Or even stopping evolution. This 
 reasoning also explains the fact that most GA systems avoid only taking the fittest Of 
 the population In generating the Next but rather a random (Or semi-random) selection 
 With a weighting toward those that are fitter.


