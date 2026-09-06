# Shared product brief

The following is a normalized Markdown copy of the long-form brief used for the same-brief comparison. Formatting has been cleaned for readability, but the product requirements are preserved.

---

You are the lead game engineer, simulation architect, gameplay designer, technical artist, and product designer responsible for building the first playable vertical slice of a potentially commercial premium PC simulation game.

## Working title

**WHAT IF? CIVILIZATION LAB**

Product description:

A living AI civilization simulation where players create initial conditions, observe societies evolve, intervene in history, run “What If?” experiments, and eventually compare parallel timelines.

Core tagline:

**Create the conditions. Watch history emerge.**

Secondary product idea:

**Change one variable. Watch history diverge.**

Important:

Do not treat this as a disposable tech demo.

Do not only write a design document.

Do not only generate code.

Actually build the project, run it, open it in the browser, visually inspect it, interact with it, test the simulation, identify weaknesses, fix them, and iterate.

The final result should be a genuinely playable vertical slice.

---

## 1. Product vision

WHAT IF? Civilization Lab is **not**:

- a WorldBox clone
- a city builder
- a traditional RTS
- a destruction sandbox
- a pixel-art simulation
- a low-poly mobile-style game
- a static AI visualization
- a collection of scripted scenarios
- a dashboard with random event text pretending to be simulation

The player creates the conditions of a world and watches civilizations evolve autonomously.

Civilizations should:

- grow
- migrate
- trade
- cooperate
- compete
- create institutions
- develop beliefs
- form governments
- create leaders
- make alliances
- develop grievances
- discover technologies
- experience inequality or abundance
- respond to environmental pressures
- sometimes fragment
- sometimes unify
- sometimes go to war
- create persistent history

The player does **not** micromanage every citizen.

Instead, the player:

1. Creates the starting conditions.
2. Observes civilization.
3. Inspects important events and people.
4. Understands why things happened.
5. Intervenes at meaningful moments.
6. Changes social, technological, informational, or environmental conditions.
7. Watches the consequences propagate through history.

The core emotional goal is:

> “I want to keep watching because I genuinely want to know what happens next.”

---

## 2. Three connected product pillars

Design the architecture around three experiences that all use the **same simulation engine**.

### A. Living World

Create civilizations and watch centuries of emergent history develop.

### B. What If? / Scenario Lab

Create unusual positive, negative, neutral, or experimental initial conditions and see what civilization does with them.

### C. Parallel Worlds

Future flagship feature.

Branch the same simulation, change one variable, run both histories, and compare the outcomes.

The first vertical slice should deeply implement A and a useful version of B.

Architect for C without sacrificing the quality of the first build.

---

## 3. Visual quality is critical

The game must immediately feel like a modern 2026 premium indie PC simulation.

Do **not** make it look:

- pixelated
- retro
- crude
- cheap
- low fidelity
- generic low-poly
- like a Three.js tutorial
- like a mobile game
- like a student project
- like an AI-generated asset collage
- like WorldBox
- like colored cubes moving around a map

Visual target:

**MODERN STYLIZED REALISM.**

Not photorealism.

Not cartoonish low-poly.

Use intelligent art direction to make a small-team simulation feel expensive and contemporary.

Aim for:

- beautiful miniature-world presentation
- sophisticated terrain
- attractive topography
- natural-looking biome transitions
- modern terrain materials
- convincing water
- soft shadows
- atmospheric haze
- dynamic sunlight
- appealing day and night
- subtle environmental motion
- elegant vegetation
- readable architectural miniatures
- settlements that physically evolve
- farmland
- roads
- ports where appropriate
- settlement lights at night
- restrained smoke and activity
- subtle particles where appropriate
- excellent camera movement
- premium UI
- strong visual hierarchy

The game should be:

**Readable from far away. Beautiful up close. Performant at scale.**

Do not chase photorealism.

Do chase strong composition, lighting, materials, animation, atmosphere, camera quality, and UI polish.

---

## 4. World layer vs observer layer

Create two complementary visual identities.

### World layer

The simulated world should feel:

- organic
- warm
- natural
- historical
- tactile
- alive

### Observer layer

The UI should feel like a sophisticated civilization observation system.

It should feel:

- elegant
- contemporary
- minimal
- analytical
- premium
- slightly futuristic

Do not make it a spaceship dashboard.

The player should feel like they are observing a living civilization aquarium through a sophisticated analytical interface.

This concept should influence the visual identity without making the world itself look artificial.

---

## 5. First vertical-slice scope

Build one small but rich simulation environment.

Default scope:

- one polished 3D miniature world
- three civilizations in normal Living World mode
- several visible settlements
- hundreds to a few thousand efficiently simulated inhabitants
- approximately 3 to 10 important named characters at a time
- population
- food
- resources
- wealth
- territory
- settlement growth
- trade
- economy
- diplomacy
- relationships
- political pressure
- social trust
- migration
- technological development
- conflict pressure
- possible wars
- major historical events
- civilization beliefs
- persistent memory
- interventions
- world chronicle
- multiple camera modes
- time controls
- civilization inspection
- character inspection
- “Why Did This Happen?”
- at least one convincing character conversation
- What If? Scenario Lab

The goal is approximately 15 to 30 minutes of genuinely interesting observation and interaction.

Prefer ten deeply connected systems over fifty shallow features.

---

## 6. Genesis

Create an elegant world-creation flow called **Genesis**.

Allow the player to configure important starting conditions.

### World type

- Balanced
- Fertile
- Harsh
- Island World
- Cold World

### Resource distribution

- Balanced
- Uneven
- Scarce
- Abundant

### Civilization count

Default 3.

Allow civilizations to have:

- name
- color / visual identity
- starting location
- cultural tendencies
- social values
- strategic tendencies
- initial strengths
- initial weaknesses

Examples:

- Scientific
- Commercial
- Collectivist
- Individualist
- Expansionist
- Isolationist
- Spiritual
- Militaristic
- Diplomatic
- Curious
- Hierarchical
- Egalitarian

These must affect behavior. They are not cosmetic tags.

---

## 7. Natural-language civilization beliefs

Allow an optional short cultural belief prompt for civilizations.

Examples:

> “Knowledge belongs to everyone, and war is the greatest failure of society.”

> “Individual freedom is sacred, but outsiders cannot be trusted.”

> “Order is more important than liberty, and strong leadership protects civilization.”

> “Material wealth matters less than reputation and service to the community.”

Do not translate these into one simplistic stat.

Interpret them into structured tendencies such as:

- openness
- aggression
- cooperation
- hierarchy
- curiosity
- expansion
- social trust
- individualism
- collectivism
- tolerance
- risk tolerance
- knowledge openness

Use those values as inputs to decisions.

Keep the interpretation layer separate from the simulation.

---

## 8. Simulation architecture

This requirement is critical.

Do not make every citizen a continuously running LLM agent.

Use layered simulation.

### Layer 1: Simulation core

Efficient deterministic or probabilistic systems for:

- population
- demographics at useful aggregate levels
- food
- resources
- wealth
- production
- consumption
- settlements
- territory
- migration
- infrastructure
- economy
- trade
- military strength
- stability
- unrest
- inequality
- environmental pressure
- social trust

### Layer 2: Civilization intelligence

Each civilization maintains state including:

- strategic goals
- fears
- opportunities
- relationships
- ideology
- grievances
- current priorities
- perceived threats
- perceived allies
- internal pressure
- resource needs
- technological priorities

Civilizations should make decisions from actual world state.

### Layer 3: Important characters

Important characters may include:

- rulers
- diplomats
- generals
- scientists
- philosophers
- religious figures
- reformers
- rebels
- explorers

Important characters maintain:

- identity
- personality
- loyalty
- relationships
- ambitions
- fears
- memories
- beliefs
- role
- influence
- historical experiences

### Layer 4: Ordinary population

Ordinary people are simulated efficiently.

They do not need individual continuous AI calls.

An ordinary person may become a named historical character when circumstances make them important.

---

## 9. Commercial-grade code architecture

Treat this project as the possible foundation of a commercial game.

Keep these systems separated.

### A. Simulation core

- world state
- population
- economy
- resources
- civilizations
- diplomacy
- characters
- history
- interventions
- scenario state

### B. Rendering layer

- terrain
- water
- vegetation
- settlements
- architecture
- roads
- farms
- units
- particles
- lighting
- atmosphere
- post-processing
- camera

### C. UI layer

- Genesis
- HUD
- civilization inspector
- character inspector
- timeline
- interventions
- Scenario Lab
- Why Did This Happen
- comparison UI
- camera controls

### D. Content / data layer

- civilization archetypes
- beliefs
- technologies
- scenario definitions
- events
- visual definitions
- interventions
- world-generation parameters

### E. AI adapter layer

Keep AI/model functionality behind clean interfaces.

Do not tightly couple the game to one AI provider.

The simulation must not depend on specific 3D assets.

The visual layer should be replaceable or dramatically upgraded later without rewriting the simulation.

Do not create one giant game component or one enormous file.

Another senior engineer or AI coding agent must be able to continue development later.

---

## 10. Emergent history

This is one of the most important requirements.

Do not fake emergent simulation using random story events.

For example, do not start a war because `random() > 0.9`.

A war may emerge because of combinations such as:

- resource scarcity
- border competition
- strategic geography
- ideological hostility
- historical grievance
- leadership ambition
- military imbalance
- internal instability
- failed diplomacy
- migration pressure
- economic dependency
- perceived opportunity
- alliance obligations

Then the war must create persistent consequences:

- casualties
- migration
- territorial change
- economic damage
- political legitimacy changes
- new leaders
- new grievances
- ruined infrastructure
- future alliances
- ideological changes
- future revenge motives

History must compound.

---

## 11. Historical memory

Civilizations and important characters should remember meaningful events.

Examples:

- wars
- alliances
- betrayals
- territorial disputes
- trade agreements
- famine assistance
- broken promises
- revolutions
- assassinations
- ideological movements
- diplomatic rescues
- technological gifts

Historical memory should influence later decisions.

Example:

Civilization A helps Civilization B survive a famine. Twenty years later, B may be more willing to support A during a crisis.

Another example:

A ruler’s parent was killed during a previous war. That memory may affect future diplomacy.

---

## 12. World Chronicle

Create a persistent visual history timeline.

Example:

- YEAR 0 — Veloria, Ardan, and Nemea were founded.
- YEAR 31 — Veloria established the Southern River settlement.
- YEAR 56 — Ardan discovered advanced irrigation.
- YEAR 72 — The Grain Crisis began.
- YEAR 84 — The First Northern Trade Agreement collapsed.
- YEAR 103 — General Oran became commander.
- YEAR 117 — The Velorian-Ardan War began.
- YEAR 129 — Reform movements spread through western Veloria.
- YEAR 143 — The Velorian monarchy collapsed.

The timeline should become enjoyable to inspect on its own.

Important events should connect to actual simulation state.

---

## 13. Why Did This Happen?

Make this a showcase feature.

Major events should have a button or action: **WHY DID THIS HAPPEN?**

Applicable to:

- wars
- rebellions
- alliances
- political collapse
- major migration
- ideological changes
- assassinations
- diplomatic crises
- economic crises
- social fragmentation

Example:

### The Velorian-Ardan War

Major contributing factors:

- Veloria’s food security declined by 31%.
- Both civilizations claimed the southern river.
- Two trade agreements failed.
- General Oran’s political influence increased.
- Relations remained hostile after the Border Crisis.
- King Arel believed military victory could stabilize his government.

These explanations must be generated from actual simulation factors.

Do not expose hidden chain-of-thought.

Use concise game-state-based causal explanations.

---

## 14. Player intervention

The game should not primarily revolve around dropping bombs, meteors, or destroying civilizations.

Interventions should mainly affect:

- information
- ideas
- diplomacy
- knowledge
- technology
- leadership
- resources
- social conditions

Implement several interventions such as:

- Whisper an Idea
- Reveal a Secret
- Give a Prophecy
- Inspire a Person
- Introduce a Technology
- Introduce an Idea
- Call a Summit
- Alter a Resource
- Bless a Region
- Curse a Region
- Reveal Another Civilization
- Create a Communication Link

Interventions should cost or use a limited Influence resource in normal play.

A Sandbox mode may eventually remove the limits.

---

## 15. Intervention chains

Interventions must not force immediate canned outcomes.

Example:

Player whispers to King Arel:

> “General Oran may be preparing to overthrow you.”

Possible chain:

- Arel investigates Oran.
- Oran loses influence.
- Oran becomes suspicious.
- Oran starts building support.
- The king attempts an arrest.
- Oran escapes.
- A neighboring civilization secretly supports him.
- Civil war begins.
- The king’s daughter sides with reformists.
- Decades later, a republic emerges.

The exact result should depend on world state.

---

## 16. Ideas as a game mechanic

Make the spread of ideas one of the defining mechanics.

Example:

Player introduces:

> “Representative democracy.”

Do not instantly convert a civilization.

Possible propagation:

- a philosopher adopts the idea
- students learn it
- writings spread
- elites resist
- rulers suppress it
- neighboring societies become curious
- reform movements form
- protests emerge
- peaceful reforms occur
- revolution occurs
- or the idea disappears

Ideas should have:

- origin
- supporters
- resistance
- geographic spread
- cultural compatibility
- important advocates
- possible institutional impact

This helps distinguish the game from physical god-sandbox games.

---

## 17. Important characters

Important characters must feel persistent.

Example:

### Mira

Age: 31  
Role: Blacksmith  
Civilization: Veloria

Traits:

- Independent
- Protective
- Distrustful of authority

History:

- Father died during the Northern War.
- Family farm was confiscated after unpaid grain taxes.

Current attitude:

- Dislikes King Arel.
- Sympathetic to reformists.

Depending on history, Mira could later become:

- activist
- rebel
- politician
- leader
- historical figure
- ordinary citizen who never becomes important

Do not predetermine her destiny.

---

## 18. Talk to Character

Implement at least one convincing character conversation experience.

The player can ask questions like:

- Why do you support this war?
- Why do you hate the king?
- What do you think about Ardan?
- What does your society believe?
- What are you afraid of?
- What do you want to happen next?
- What happened to your family?
- Would you support a rebellion?

Responses must be grounded in:

- actual world state
- character history
- relationships
- personality
- civilization history
- current politics
- social conditions

Do not generate disconnected random flavor text.

If live LLM access is unavailable, create a clean AI adapter interface and a grounded local fallback.

The rest of the simulation must remain fully playable without remote AI.

---

## 19. What If? / Scenario Lab

Scenario Lab is a defining product pillar.

This is **not** a disaster mode.

It is a civilization experimentation system.

The player creates unusual initial conditions and asks:

> “What happens if...?”

Scenarios may be:

- extremely positive
- extremely negative
- neutral
- utopian
- difficult
- socially unusual
- economically unusual
- technologically unusual
- geographically unusual

Do not assume positive conditions create utopia.

Do not assume difficult conditions cause collapse.

The same underlying simulation should determine what happens.

Scenario Lab defines **initial conditions**. It does not define the ending.

---

## 20. Scenario categories

### A. Abundance

Examples:

- What if everyone was wealthy?
- What if nobody needed to work for survival?
- What if housing, food, education and healthcare were universally available?
- What if energy became nearly free?
- What if material scarcity largely disappeared?
- What if everyone had excellent education?

Possible emergent questions:

What becomes scarce instead?

- status?
- attention?
- political influence?
- land?
- reputation?
- meaning?
- exclusive experiences?
- knowledge?
- prestige?

Do not script the answer.

### B. Scarcity / survival

Examples:

- 120 strangers on an isolated island
- several survivor groups with unequal supplies
- one extremely scarce resource
- a harsh environment
- isolated settlements later discovering each other

For fictional shipwreck or aircraft-survival scenarios, start after the event.

The survivors are alive and able to act.

Do not spend scope on graphic accident cinematics.

The interesting question is: **What society emerges afterward?**

### C. Social conditions

Examples:

- extremely high social trust
- extremely low social trust
- universal starting wealth
- extreme inequality
- no initial concept of private property
- strong individual freedom values
- strong collective stability values
- direct democracy
- expertise-selected leadership
- no government
- inherited monarchy

### D. Technology and knowledge

Examples:

- one civilization is 300 years ahead technologically
- advanced AI appears centuries early
- one society knows a drought will happen in 40 years
- all knowledge is public
- knowledge is controlled by elites
- instantaneous communication becomes possible
- nearly limitless energy appears
- one civilization has modern medicine much earlier

Technology must affect more than one number.

Potential effects:

- population
- resources
- warfare
- inequality
- migration
- political power
- information spread
- cultural influence
- diplomacy
- social organization

### E. Geography and isolation

Examples:

- separate islands
- unequal islands
- isolated valleys
- one civilization controls the only sea passage
- civilizations evolve separately for centuries
- isolated societies suddenly discover each other

---

## 21. Reusable Scenario Engine

Do not hard-code each scenario as a separate game.

Build reusable Scenario Definitions.

Useful parameters include:

- initial population
- population groups
- starting location
- geography
- resources
- wealth distribution
- material abundance
- technology level
- social trust
- cultural values
- knowledge distribution
- political organization
- starting infrastructure
- starting relationships
- communication
- transportation
- environmental danger
- survival pressure
- special knowledge
- initial crisis

Make future scenarios primarily data-driven.

---

## 22. First scenario presets

Do not build 30 shallow presets.

Build approximately five polished starting scenarios using the reusable Scenario Engine.

### 1. Genesis

Normal living-world simulation. Three civilizations evolve over centuries.

### 2. The Island

Approximately 120 fictional people begin isolated on one island.

No established government.

Resources are adequate but not unlimited.

Observe:

- leadership
- factions
- cooperation
- division of labor
- property
- institutions
- settlement structure

### 3. After the Wreck

A fictional passenger ship was lost before the simulation begins.

Several survivor groups reached different locations.

They have unequal:

- supplies
- skills
- population
- geography

They may:

- discover each other
- cooperate
- trade
- merge
- fragment
- compete
- become separate societies

The wreck itself is not the entertainment. Civilization formation is.

### 4. Post-Scarcity

Basic material needs are effectively solved.

Everyone has excellent access to:

- food
- housing
- energy
- healthcare
- education
- basic goods

Observe what becomes socially important.

Do not predetermine the outcome.

### 5. Mirror Civilizations

Two civilizations begin with nearly identical:

- seed
- geography
- population
- resources
- wealth
- technology

Only one major variable differs.

Example:

Civilization A: “Individual freedom is the highest social value.”

Civilization B: “Collective stability is more important than individual freedom.”

Make long-term differences observable.

---

## 23. Everyone Is a Millionaire

Include this in Post-Scarcity or as another preset if scope allows.

Every household begins extremely financially wealthy.

But physical reality still has finite:

- land
- influence
- political power
- exclusive locations
- prestige
- attention
- rare experiences
- some natural resources

Do not simply set every resource to infinity.

The simulation should explore what enormous universal monetary wealth means when some forms of scarcity still exist.

Do not script the conclusion.

---

## 24. Custom “What If?”

Architect the game so a player can eventually write:

> “Put 200 people on three islands. One island has abundant food, one controls valuable minerals, and one has almost nothing.”

or:

> “Everyone is wealthy, nobody needs to work, and energy is free.”

or:

> “Create two identical civilizations but make one extremely trusting and the other suspicious of outsiders.”

or:

> “Three societies evolve separately for 300 years before discovering each other.”

Natural language must not generate arbitrary executable game logic.

Convert the request into validated structured scenario parameters.

If full AI interpretation is outside the first build:

- create the proper architecture
- create the UI
- implement either a limited parser or structured fallback

---

## 25. Scenario Builder

Create a visually polished Scenario Builder.

Do not make it feel like a developer settings page.

Example controls:

### Population

- 100
- 500
- 1,000
- 5,000

### Material conditions

- Critical
- Scarce
- Balanced
- Abundant
- Post-Scarcity

### Wealth distribution

- Equal
- Moderately Unequal
- Extremely Unequal
- Universal Wealth

### Social trust

- Very Low
- Low
- Moderate
- High
- Very High

### Technology

- Primitive
- Early Civilization
- Industrial
- Modern
- Advanced

### Knowledge access

- Open
- Mixed
- Restricted
- Elite Controlled

### Political start

- None
- Clan
- Council
- Monarchy
- Representative
- Authoritarian

### Geography

- Single Landmass
- Separate Islands
- Resource-Unequal Islands
- Isolated Regions
- Balanced World

Use elegant controls, explanations, visual previews, and good hierarchy.

---

## 26. Change one variable

This should become an important fantasy.

The player watches history and then asks:

> “What if I changed only this?”

Examples:

- increase food availability
- remove material scarcity
- increase social trust
- reduce social trust
- reveal another civilization
- introduce advanced medicine
- introduce a political idea
- give one society warning of a future drought
- create instantaneous communication
- give everyone housing
- introduce advanced AI
- remove an important natural resource
- reveal a valuable resource

After the change, the world continues simulating.

Do not generate a canned conclusion.

---

## 27. Parallel Worlds foundation

Architect simulation state for a future flagship feature: **Parallel Worlds**.

At Year 100, create Branch A and Branch B.

Example:

A: King receives warning.  
B: King never receives warning.

Or:

A: Post-scarcity energy introduced.  
B: Nothing changes.

Run both to Year 300 and compare outcomes.

Full branching does not need to ship in this first vertical slice if it threatens core quality.

However:

- use explicit world state
- use seeded randomness where practical
- avoid hidden mutable systems that make reproducibility impossible
- keep architecture compatible with save snapshots and branching

---

## 28. Comparison view

Comparison is an important future differentiator.

Support a useful initial comparison experience.

Ideal:

**SIDE-BY-SIDE — WORLD A | WORLD B**

Possible comparisons:

- high trust vs low trust
- abundance vs scarcity
- equality vs inequality
- isolation vs connection
- technological advantage vs equal technology
- two belief systems

If true simultaneous split-screen 3D rendering is reasonable, implement it.

If it would significantly hurt performance or consume too much first-build scope, create a polished synchronized comparison UI with locked cameras, shared metrics, and rapid switching.

Architect so true simultaneous comparison can be added later.

---

## 29. Camera system

Camera quality is part of perceived game quality.

Do not use one generic orbit camera.

Implement polished camera modes.

### A. Orbit view

Cinematic global observation.

### B. Top-down strategic view

Smoothly transition to a strategic angle.

Clearly show:

- borders
- settlements
- roads
- trade
- resources
- migration
- conflict zones
- infrastructure

### C. Settlement view

Zoom closely into a settlement.

Its physical growth should become visible.

### D. Follow view

Follow:

- an important character
- migration group
- expedition
- military movement
- trade group

### E. Comparison view

Optimized for Scenario Lab and future Parallel Worlds.

### F. Cinematic observer

Slow, visually attractive automatic observation mode.

Useful for:

- watching
- showcasing
- screen recording
- social content

Create smooth transitions.

Avoid debug-camera feeling.

---

## 30. Camera angles and perspective

Allow players to meaningfully change how they observe the simulation.

Support:

- angled 3D world view
- near top-down strategy view
- close settlement perspective
- cinematic low-angle or horizon-oriented views where appropriate
- focused entity tracking

Camera-angle changes should reveal different kinds of information, not simply rotate the same presentation.

Top-down should improve analytical clarity.

Angled world view should improve beauty and immersion.

Close views should improve emotional attachment.

---

## 31. Settlement evolution

Settlements must physically evolve.

Do not keep one city icon forever.

Visual progression may include:

### Stage 1: Camp / tiny settlement

### Stage 2: Village

### Stage 3: Town

### Stage 4: City

Communicate development through:

- increasing building density
- road networks
- farms
- ports
- defensive structures
- civic buildings
- industrial areas where historically appropriate
- nighttime illumination
- smoke/activity
- resource infrastructure

Keep rendering efficient.

---

## 32. Modern UI

The UI must feel like a premium 2026 game.

Avoid:

- Bootstrap feel
- giant debug tables
- oversized text blocks
- generic admin dashboard design
- mobile game UI
- excessive windows
- old-fashioned strategy chrome

Create:

- excellent typography
- subtle transparency
- contextual panels
- restrained animation
- clear icons
- intelligent hierarchy
- modern interactions

Required areas:

- Main HUD
- Time controls
- World information
- Civilization inspector
- Character inspector
- World Chronicle
- Intervention panel
- Why Did This Happen
- Genesis
- Scenario Lab
- Camera controls

Example civilization panel:

**VELORIA**

Population: 12,841  
Stability: 71  
Food Security: 43  
Scientific Development: 68

Current Strategy: Secure access to the southern river.

Leader: Arel III

Social Pressures:

- Food shortage
- Military influence
- Growing reform movement

Do not make the player stare at spreadsheets.

---

## 33. Time

Implement:

- Pause
- 1x
- 5x
- 20x

The simulation must remain stable when time speed changes.

Do not tie important simulation behavior directly to frame rate.

---

## 34. Visualizing the simulation

Make invisible systems visually understandable.

Examples:

Trade: visible routes or subtle movement.  
Migration: population movement between regions.  
Conflict: border pressure and meaningful military movement.  
Ideology: subtle overlays or influence visualization.  
Resources: optional map overlay.  
Territory: elegant borders.  
Settlement growth: physical development.  
Relationships: diplomacy interface.

Do not cover the beautiful world with permanent overlays.

Make layers contextual and optional.

---

## 35. Graphical polish

Use modern browser rendering techniques intelligently.

Where useful:

- directional sunlight
- ambient environment lighting
- physically plausible materials
- soft shadows
- good water
- atmospheric fog / haze
- subtle post processing
- anti-aliasing
- restrained bloom
- dynamic day/night colors
- instancing
- level of detail
- efficient vegetation
- optimized settlement representation
- subtle animation

Do not add visual effects just because they exist.

Every effect should improve atmosphere or readability.

---

## 36. Performance

Target a modern desktop browser.

Avoid:

- one mesh per simulated citizen
- unnecessary React rerenders
- excessive draw calls
- constant AI calls
- expensive per-frame simulation logic
- unbounded historical data rendering

Use:

- batching
- instancing
- aggregate population representation
- proper simulation ticks
- caching
- efficient state architecture
- LOD where useful

The game should continue to feel smooth as settlements grow.

---

## 37. Content-creation value

The game should naturally generate shareable stories.

Potential video concepts include:

- “What happens if everybody is rich?”
- “I gave three civilizations unlimited food for 500 years.”
- “I created a society where nobody needed to work.”
- “I put 120 strangers on an island and simulated 200 years.”
- “I created two identical civilizations with opposite values.”
- “I gave one civilization advanced AI 500 years early.”
- “Three civilizations lived separately for 300 years. Then they met.”
- “I changed one idea and watched 400 years of history diverge.”

Design camera presets, chronology, world events, comparison view, and minimal-HUD viewing so the game is pleasant to record.

Do not build a video editor.

---

## 38. Scenario outcome summaries

Allow useful milestone summaries.

Example:

### Post-Scarcity Experiment

**Year 0**

Population: 500  
Basic Needs: Fully Available  
Material Wealth: Universal

**Year 200**

Population: 3,410  
Average Stability: 78  
Scientific Development: 91

Major Sources of Competition:

- Political influence
- Prime land
- Prestige
- Cultural leadership

Major Historical Events: [...]

Treat this as a fictional simulation.

Do not imply that simulated outcomes prove truths about real human societies.

---

## 39. Political and social modeling principle

The game may simulate different:

- economic structures
- political systems
- social values
- technology levels
- cultural tendencies

But do not encode simplistic conclusions such as:

- X ideology always succeeds.
- Y political system always collapses.
- Z culture is superior.

Variables influence incentives and probability.

Outcomes emerge from interactions.

This is a fictional computational model, not a claim to scientifically predict real humanity.

---

## 40. Technology

Choose the best practical browser technology yourself.

Three.js and React Three Fiber are reasonable choices if they help.

Use another stack if clearly better.

Optimize for:

- visual quality
- maintainability
- simulation performance
- fast iteration
- modular architecture
- future extensibility

Do not optimize for theoretical engineering elegance while failing to deliver a working game.

---

## 41. First-build priorities

If scope becomes too large, prioritize in this exact order:

1. Strong modular architecture.
2. Beautiful modern interactive world.
3. Excellent camera.
4. Stable simulation clock.
5. Three meaningfully different civilizations.
6. Settlement growth.
7. Persistent history.
8. Economy / resources / population.
9. Diplomacy and political pressure.
10. Events caused by actual state.
11. Scenario Engine.
12. Three to five strong Scenario presets.
13. Player interventions.
14. Why Did This Happen.
15. Important characters.
16. Grounded character conversation.
17. Scenario Builder polish.
18. Comparison foundations.
19. Additional graphical polish.

Do not destroy core quality in order to tick every checkbox.

A smaller deeply working simulation is better than a huge fake feature list.

---

## 42. Iterative agent loop

Use an iterative development process.

Do not consider the task complete after the first successful compilation.

Repeat this cycle:

1. Implement one meaningful part.
2. Run the project.
3. Open it in the browser.
4. Inspect the game visually.
5. Actually interact with it.
6. Run the simulation at 1x, 5x and 20x.
7. Test relevant controls.
8. Observe whether history is genuinely changing.
9. Identify the most important weakness in visuals, simulation, gameplay, UX, performance, or architecture.
10. Fix it.
11. Run and test again.

Continue while meaningful improvements are possible within the available session.

Spend the majority of available work building and testing, not describing your plans.

---

## 43. Visual self-review

During development repeatedly ask:

Does this look like:

- a coding demo?
- a generic Three.js example?
- a cheap low-poly project?
- an AI-generated game?
- a mobile prototype?
- an unfinished editor?

If yes, improve:

- composition
- terrain
- materials
- lighting
- atmosphere
- architecture
- vegetation
- camera
- animations
- UI
- world detail

The target reaction is:

> “I would believe this is an early build of a real premium 2026 indie PC game.”

Not:

> “This is impressive considering AI made it.”

---

## 44. Simulation self-review

Repeatedly test whether the simulation is genuinely stateful.

Ask:

Would the world develop differently if:

- food decreased?
- resources became abundant?
- a leader died?
- social trust changed?
- one civilization became technologically superior?
- an alliance failed?
- the player introduced democracy?
- everyone became wealthy?
- two civilizations discovered each other earlier?
- an important resource disappeared?
- one society learned about a future crisis?

If changing these conditions produces little meaningful difference, improve the simulation.

Do not fake depth with text.

---

## 45. Commercial foundation

Do not spend this first build implementing:

- Steam integration
- monetization
- DLC
- accounts
- multiplayer
- cloud infrastructure
- huge content libraries
- advanced save management
- full branching UI
- production analytics

But avoid architectural choices that would make these impossible later.

---

## 46. Success criteria

The build is successful if:

- it actually runs
- it is genuinely playable
- it looks modern and premium
- it does not resemble WorldBox
- it does not feel low quality
- it feels appropriate for a 2026 PC game
- the world is visually enjoyable to observe
- camera movement feels polished
- civilizations behave meaningfully differently
- settlements visibly grow
- history accumulates
- major events arise from simulation state
- earlier events influence later events
- Scenario Lab changes actual simulation conditions
- both positive and negative scenarios are supported
- player interventions create persistent consequences
- Why Did This Happen explains actual causal factors
- important characters maintain identity and history
- at least one character conversation feels grounded
- time acceleration remains stable
- the player wants to keep observing
- the codebase is modular enough for another senior engineer or AI agent to take over

---

## 47. Final instruction

Work autonomously.

Make reasonable engineering, gameplay, and artistic decisions yourself.

Do not ask routine questions.

Ask me only if something is genuinely blocking or irreversible.

Do not stop with planning.

Do not stop with code generation.

Do not stop just because the project builds.

**BUILD. RUN. OPEN. INSPECT. PLAY. SIMULATE. FIX. POLISH. REPEAT.**

Before declaring completion, perform a final browser playtest and visual inspection.

At the end, provide only a concise implementation report containing:

1. What is genuinely implemented.
2. Which gameplay systems are truly connected to simulation state.
3. Which Scenario Lab presets work.
4. Which systems are simplified or mocked.
5. Current architecture.
6. Performance limitations.
7. Known visual limitations.
8. Known simulation limitations.
9. The five highest-impact next improvements.
10. Any files or systems that a future senior AI coding agent should inspect first.

The majority of your effort should go into producing the playable game, not explaining it.
