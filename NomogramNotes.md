
The file 5eNomogram.png contains a nomogram (a type of visual calculator) built for quick and easy probability calculations for Dungeons & Dragons 5e.

# Intro
Basically, you use the chart to compute the "expected damage" that your weapon would do in various situations.  Here, "expected" is used in the mathematical sense meaning you multiply the probability of hitting the monster by the average damage for the weapon.

In mathese:
Let:
- E(Dam) be "expected damage per round"
- P(hit|AC=?) be "the probability of hitting a monster with AC of the value given by "?"
- WD = average weapon damage

$ E(Dam) = P(hit|AC=?) \times WD $

So, if the probability to hit a monster with AC=13 is 40% and you're attacking with a weapon that does 1d4:

$$ P(hit|AC=13) = 40% = 0.4$$
$$ WD = 2.5 $$

$ E(Dam) = 0.4 * 2.5 = 1 $
So on average with this weapon vs that AC you would expect to do 1 point of damage per attack.

# Computing the Probability of Success (Probability to Hit)

To compute these numbers on the nomogram is very easy.  First , look at the left-most scale and notice there are columns labeled "D", "A", "d20", and "P(hit)".

These are respectively:
- D: 1d20 rolled with Disadvantage against the noted AC
- A: 1d20 rolled with Advantage against the noted AC
- d20: 1d20 rolled in the typical way against the noted AC
- P(hit): The probability of rolling a number greater than or equal to the given AC.

So, to figure out the probability of hitting a 15 AC, go do the column labeled d20, and find the 15.  Note that the 15 is next to the indicator for 0.3 under the P(hit) column.  This means that there is a 30% chance of hitting the AC=15 monster.

The "D" and "A" columns are used similarly. If you're rolling with advantage, find the 15 in the "A" column.  Sight across to the P(hit) column and see that the 15 lands at around 51%.  

If you're rolling with disadvantage, use the "D" column and see that the probability of hitting is about 9%.   

You can see that for AC=15, there's a **HUGE** change between the "normal" roll and rolling with advantage and disadvantage. 

### Fixed bonus to hit

Some weapons and abilities afford a fixed offset to hit.  For example, a +1 longsword always gives +1 to whatever roll you make.  This is the same as *reducing* the AC by 1.   Thus, if you're attacking AC=15 with a +1 longsword, it's the same as attacking AC=14.   This is seen on the P(hit) scale to have a probability of 35% instead of 30%

## Finding the typical Weapon Damage
The central, diagonal scale contains a range of possible damages (in black) and common die rolls for damage (in red).  If your weapon does 2d8 damage, the typical damage would be the center of all possible rolls, or 4.5 + 4.5 = 9.   This is shown on the nomogram with 9 and 2d8 occupying the same position on the scale.   Similarly, 4d8 damage is typically 19.

### With fixed offsets
If a weapon has a fixed +/- attached, such as a +1 dagger, simply compute the value and move one tick along the scale.  For example. 2d4 damage is 5.  2d4+2 damage is 5+2=7.


# Comparing Possible Courses of Action
The main use case I had in mind was for comparing the likely results of various courses of action.


For example:

You're playing a magic user.  For a given round, you're trying to decide which of the following is the "best" choice.

1. Attack with your dagger
2. Cast a buff spell to give everyone in your party a +1 damage bonus on all hits.
3. Cast Faerie Fire to give everyone in your party advantage on attacks.

For this example, assume that your party 
- consists of yourself and a tanky paladin swinging a longsword and 
- you're engaged in a scrap with a kobold fighter with an assumed AC=12.


## Option 1: Attack with a dagger.
Being a wizard, you're a pretty lousy melee fighter and you only get a +1 to hit with and +1 damage with your dagger.

- You get +1 to attack with is the same as assuming the kobold has AC=11
	- This equates to a 50% chance of hitting (P(hit) columns)
- Typical damage is on the diagonal scale: 1d4+1=3.
- Multiplying these gives 0.5* 3 = 1.5.   
- You can use the nomogram for computation by running a line that starts on the P(hit) column at 0.5, runs *through* the 3 on the diagonal scale and the ends on the E(dam) scale at 1.5.

All this means that your dagger attacks will generate 1.5 points of damage on average.


## Option 2: Buff the Paladin.
The paladin is already pretty tanky and gets +4 to hit and +4 damage from his longsword.  If you cast your buff spell, this would go up to +4/+5.

### Without the buff
- +4 to hit is equivalent to attacking AC=12-4=8.  
- P(hit) = 75%
- longsword damage is 1d8+4 = 8.5avg
- E(dam) is about 5.5

### With the buff
Re-do the nomogram compute but move the damage up to 9.5
- E(dam) is abou 6.25



