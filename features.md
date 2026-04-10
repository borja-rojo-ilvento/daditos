# Daditos game

This game is a dice-based game where a player builds their pool of dice through encounters. These
encounters are themselves passed by usage of dice, where a player would roll their pool.

## Dice

Dice are the main interaction mechanic for the game. Dice can have many different qualities which
change their effect in the game.

### Properties

These different characteristics of a dice combine to implement different effects on a

- Count of sides
- Color
- Pattern

#### Count

The side of the dice simply determine the number that is rolled out of the dice.

- 4 sided dice
- 6 sided dice
- 8 sided dice
- 10 sided dice
- 12 sided dice
- 20 sided dice

#### Color

Each color adds a different character to the roll of a dice.

- Blue; 
- Red; Critical effects?
- Green
- Yellow
- Orange
- Purple
- Black
- White

#### Pattern

Allow for different color effects to be present on a dice which each combine to have a particular
new type of effect.

- Solid
- Dotted
- Stripped
- Swirled
- Speckled

#### Material

- Plastic
- Metal
- Crystal
- Wood
- Air
- Water

#### Enchants

Blessings and curses that generate different effects? Adds in the aspects of soft-magic over the
very hard-magic nature of dice rolling and math mechanics.

### Rolls

Rolls as a whole can have their own interactions between dice. For example, a dice roll can fulfill
a 'full house' set of numbers, which would result in an enhancement. Other patterns with other
properties should also be concidered. For example, if you have a dice set with one of the primary
colors, that effect could also trigger an enhancement.

Also, more simply, dice of certain properties might have base interctions (which I need to flesh
out). For example, Blue dice could always roll +2 (or something).

### Building

Dice are meant to be configurable. How this is done is still up in the air.

- A crafting bench with the ability to combine and break dice?
- Items as ingredients? Helps add dice modifiers, perhaps. The ingredients could be very flavorful
in that they are a feedback loop between the work interaction and the dice themselves, adding a
narrative layer by marking the results of your journey and decisions. (maybe needs to be more
permanent/ appendy semantics. Reversion is done with a removal item, not an undo.)
- The ability to replace numbers on a dice with other things! Specific numbers can get
swapped out entirely. A number could get swapped out with someting that isn't a number at all! I
don't even know what that means in this system but I want it.

## Relics, cards, overlays (working concept name)

Here is a kind of 'filter' mechanic which can affect the outcome and effect of a certain class of
dice. The idea is that modifications here can enhance your rolls in a variety of different ways,
perhaps adding extra effects for certain combinations of dice, effecting the number outcomes of
certain dice classes (targeting their color, material, pattern), and other things.

## Equiment

This might be the same as relics. I was thinking that maybe you could have different thematic tools
that would effect roll sets. Concidering that there might be a roll of dice done sequentially for an
interaction, but that one roll could have multiple dice from your pool but not all, then perhaps
rolls sets themselves could be a target for modification.

- A different kind of dice cup could change the roll set (maybe this is where you place traits
specific to multiple-dice interations, like full house and stuff??)
- A dice box that rolls are thrown onto could have an effect on the whole interaction itself, if
dice are thrown into a collection?



## Encounters

- Monsters
- Chests
- NPCs, with lore?
- Entrances to other structures and subden

## Maps

The way that the map works is fog-of-war style. Think Age of Empires, League of Legends, or Dota.
The player moves around trying to find the boss to defeat (for now), while also potentially
encountering other events, which can vary. Path of Exile has a great tiling mechanism for their
maps, which can be of great inspiration.

### Locations

Special/ unique locations, which hold lore and all that, could be an element of altering typical
sets of interations. Perhaps there are items, monsters, and NPCs would normally only are around in
specific locations.

More siginificantly to the character of the location, though, are things a
player could interact with in the location itself. Maybe there are shrines that can be used to bless
dice. ! The character and properties of maps themselves (almost like their own NPCs) needs to be
explored as well !

## Notes

- Encounters are quick and many, in order to be able to quickly build a bunch of small modifications
- Bosses are longer encounters which acts as build checks
    - Certain encounters could allow for bosses to be modified for the round, which would augment
    the character of the reward
- I would like to flesh out more of the gameplay in terms of interactions and world, which can
obviously be pretty vanilla but would like to see if the dice lend to a kind of interaction that
wouldn't be possible without dice or would play very well with them. Especially given dice-set
property mechanics. For example, would NPCs all share a master set of potensial fields which would
be affected by an interaction (the NPC state). Maybe, this could be modeled as attempting to hit
the right NPC state after an interaction to get the outcome you wanted.
    - As an aside, I think it could be fun to have hidden or non-obvious rare outcomes in
    interactions. Kind of like pulling a secret-rare or from a pack? Idk. For example, you're
    fighting a monster, and one of the outcomes is a friendly battle ending.

- I think it could be cool to also have multiple dice rolls in an interaction as part of the build.
Perhaps this would require more stats act as resources to enable and limit this, such as energy.
- Are dice pools a set or a list, which determines the character of how a pool is evaluated on roll.

- If the gameplay is very build specific, in that a way someone decides to roll their dice per
interaction becomes important, then maybe there are QoL features that could become important to
think about. For example, if someone decides to split how they roll their dice pool to facilitate a
certain kind of Interaction, then selecting that specific sequence over and over can be really
annoying. Due to that, it could be cool to have someone build or select a roll sequence to easy
reuse.
- Mechanic for a chance to refresh the dice-pool roll?
- Logging for builds and their successes, for later analysis by players and devs?

- I do want to have the ability to design different aspects of interactions, filters, attributes and
  other discrete sets of stuff to slot into this system. I would like it to be extensible. It
reminds me of the joker mechanism in Balatro, in that you can just create discrete cards with
different rules. Maybe, that requires also a kind of `ctx` idea where the Joker is activated in a
stack with the ability to read and interact with the global state. Idk.

- An thought regarding modification elements such as relics or equipment makes me think of the
'appropriate' place to have customizations modify different aspects of rolling. A practice of
identifying what each piece of the process actually is could inspire classes of items to be able to
customize.

## Data Model

```lua

--[[ Single die unit representation. ]]
let Die = { 
    ...
}

--[[ Set of dice rolls creating a final basket of effects? ]]
let Interaction = { 
    ...
}
--[[ This is the building of the dice roll into an Interaction payload.

Having consecutive dice rolls should bleed into each other, stacking the interaction.
Not sure if there is a kind of check that would be best to do as a set of dice unordered, or if
that doesn't actually matter and
]]

let Roll = function (Interaction, die_set) -> Interaction -- Maybe `function(Interaction, die)`

end

--[[
Maybe not hard stats, because I honestly don't like stats much.
Instead, could be a bunch of attributes with intaction rules?
]]
let Stats = {
    ...
}



```
