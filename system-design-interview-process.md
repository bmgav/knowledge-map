# System Design Interview Process

## General Info/Advice

There are 3 reason why engineers find SDI interviews challenging:

1. Interview is unstructured in nature (design problems don't have a standard answer)
2. Lack of experience in developing complete/large systems
3. Didn't spend enough time preparing

In general, interviewers will be looking for:

- The thought process behind the design choices you make
- Can you take ownership of an open-ended problem? Can you be trusted to work without a lot of supervision
  - Note that this requires you to be able to communicate effectively

## Grokking SDI Suggested Problem Solving Process

1. Requirements Clarification + Establish Scope
   - Clarify which parts you should focus on (establish the scope)
     - What is the goal of the system?
     - Who are the users? What do they need it for? How are they going to use it? How many users will there be?
     - What are the inputs and outputs from the system
   - Make sure you agree with your interviewer about what features are important to the system
     - what clients need to be supported? Web? Mobile?
     - Do we need authentication? Analytics? Integrating with existing systems?
2. Back of the envelop calculations
   - what scale is expected? how much storage -- will it fit on 1 machine or will you need many?
     - Note: videos and photos take significantly more storage
   - What is the expected network bandwidth usage?
   - How many concurrent requests? How many requests per second?
   - Average expected response time?
   - Expected read to write ratio?
3. System interface definition
   - Define the APIs expected from the system -- will help make sure we haven't forgotten any requirements or misheard something
4. Define the data model
   - identify the various entities in the system and how they interact
   - consider aspects like storage, transportation, encryption etc.
   - Which database should we use? MySQL? NoSQL? why?
5. High-Level Design
   - draw a block diagram with the core components (generally want to identify enough components to solve the problem from end-to-end)
     - Include different clients, backend services, offline processes, network architecture + how they interact
   - Identify system entry points -- user interaction? external API calls? offline processes?
6. Detailed Design
   - Dig deeper into 2-3 major components )interviewer feedback should guide which components you dig into) -- should be able to present the pros/cons of various options
   - Be sure to explain the tradeoffs of the choices you make
     - what type of DB? why?
     - what caching solutions are there? which should we use?
     - what frameworks could we use?
   - Can help to think of commonly used data structures/algorithms
     - URL shortener -> hash function
     - Need to scale -> sharding
7. Identify and Resolve Bottlenecks
   - Are there any single points of failure? Can we mitigate them?
   - Do we have enough replicas of data assuming servers will fail
   - Do we have enough copies of different services running to avoid a total shutdown if/when something fails?
   - How do we monitor performance? Do we get alerts if critical components fail? What about as performance starts to degrade?
   - Would using any of the following help address scalability issues?
     - Load balancer
     - Horizontal scaling
     - caching
     - database sharding
