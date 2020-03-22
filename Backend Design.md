# Backend Design

## Constants
- loosingInfectionRate (70%, game end)
- deathRateAboveICU
- deathRateBelowICU
- startRegions
    - which regions
    - infected population per region
- startReproducion rate
- dailyIncome
- initialIncome
- initialHappiness

## Entities

### GlobalState
- money
- clock (week/round counter)
- activeActions

### Region
- totalPopulation (constant)
- infectedPopulation
- reproductionRate
- maxICU (Intensivkapazität, Threshold ab dem Sterblichkeit steigt)
- happiness (percent)

### Measure
- cost (money)
- fn apply(state)
- successProbabilty

### Event
- fn apply(state)
- duration
- warnPlayer

### ScheduledGameEvent: GameEvent
- whichTick

~~RandomGameEvent: GameEvent~~
- ~~probability~~


## Game Loop
- **input**: user chosen action
- increment clock
- apply measures
- apply effects of game events (eg. random infections)
- calculate new infections based on infectedPopulation and reproductionRate for every region
    - `newInfections = (new infections from last round) * reproductionRate * modifier`
    - `infectedPopulation += newInfections`
- calculate deaths
    - `deaths += min(newInfections, maxICU) * deathRateBelowICU`
    - `if newInfections > maxICU:`
        -  `deaths += (newInfections - maxICU) * deathRateAboveICU`
- check loosing condition
- **output**