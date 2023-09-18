# <p align="center">DnD Enemy study - what's the best aoe cantrip? </p>

# <p align="center">DEX vs CON</p>

This study comes from the idea of determining which AoE cantrip is better. Since the damage is the same, the only determining factor is the damage type and the save. The damage resistances are easy to determine. This study will thus be centered around determining which one is best between CON saves and DEX saves for AoE cantrips in DnD 5th edition. 

Disclaimer: The data is based only on DnD Player's Handbook monsters. Although there are extra campaign modules and additional rule sets containing an additional amount of monsters, we consider the player handbook contains enough to make a preliminary study. The inclusion of this additional data can also prove itself redundant or biased depending on the source. This additional data might be used in the future to confirm or deny the conclusions of this study, or to extend it to skewed sources.


## Table of content:


- Preliminar
    - 1.1 Database
    - 1.2 Resistances

- Observational study
    - 2.1 Correlations between stats
    - 2.2 Correlations between saves
    - 2.3 Mean dex and con by cr
    
- Conclusion #conclusion
    - 1.1 Verification and Rule of thumb




### Preliminar

#### 1.1 Database (link)


#### 1.2 [Resistances](Resistances.ipynb)

![resistances_and_immunities_phb](https://github.com/ThomasBoutonnetAntelo/AoE_pre_publication/assets/12410931/42eca2ef-ccec-4b5b-9438-f057d9d310ba)

Apparently thunder offers the worst coverage, while force is resisted by no one. While this database is short, this proportion of resistances is transposable to the totallity of monsters published in alternative books, per common consensus.
<br />

### Observational study
<br />

#### 2.1 Correlations between stats

<br />
Now, there's a logical assumption that when a GM puts creatures on the field map, they have a tendency to be "lighter" creatures if they are numerous ("light" being highly dependant on GM interpretation) compared to when they put fewer or a single creature, where they tend to be bigger, or more resistant. This could mean if they are numerous, they could be more dexterous, making it worse for dex save cantrips, and better for con saves.

There's also the rule for the Challenge Rating (cr), i.e. the monster level. If several creatures are in the field they should have the same summed up level of difficulty than a single creature if they were to fight the players.

This idea is logical mathematically. If one creature has to endure all the damage from the players they need to be resistant. If the threat is divided among several creatures, the need for them to have higher resistance isn't important, it could even make the combat too hard. It could mean that when more creatures are present their resistance should be lower, so lower con stats.

This could indicate that when a GM decides to put several smaller creatures (making a perfect situation for the use of aoe cantrips) the monsters could have different stats than when individual biggers ones are summoned

Thus, lets start by study the influence of size and challenge rating in the stats and also the stats correlation to each other.

![stat_corr](https://github.com/ThomasBoutonnetAntelo/AoECantripSaveStudy/assets/12410931/b2b25dda-f833-4ee5-a55e-c0c5e1f43221)


Interesting relations:

- dex is negatively correlated to size, con and str: the bigger, the stronger, the sturdier the monster, the less dexterous. There's definitelly a difference between big sturdy monster and agile ones
- following this, con is negatively correlated with dex: if con raises, dex doesn't
- dex seems almost untouched by cr: the harder the monster, not necesarily the dexterous
- con seems heavily influenced by cr: a harder monster definitely means more constitution and more life
- surprisingly speed hasn't got a big correlation with dex, con is more correlated to it, although it could be because of the size of the creature

Now, size definitely seems a factor in a monster's dex and con attributes. If a monster is bigger, it tends to be less dexterous, and it gets stronger and more resistant.

Cr though seems less of a factor for higher dex stats.

One hypothesis about independance of dex from cr could be that the dex stat is quite relevant in many abilities like evading attacks (magical or influencing ac), attacking first (initiative), or making attacks. It's prevalence and utility could make things too hard if it would augment in relation to monster difficulty aka cr. Lets see dexterity values over cr levels. 

![dex_by_cr](https://github.com/ThomasBoutonnetAntelo/AoECantripSaveStudy/assets/12410931/863f5fca-cc0b-48e6-a30c-b4229435b88b)


In any case, the higher the level - and thus the challenge rating- the higher the con stat. This could be a lead.


![con_by_cr](https://github.com/ThomasBoutonnetAntelo/AoECantripSaveStudy/assets/12410931/9bf2c4ad-dfe1-49fd-946b-831efef35582)



But, as we are interested in dex/con saves, are we really onto something right now?

<br />

 #### 2.2 Correlations between saves
 
<br />
There's an important thing we already commented: stats saves are not necesarily dependant on stats modifiers -> some monsters have alternative save attributes

![mods_vs_save_table](https://github.com/ThomasBoutonnetAntelo/AoECantripSaveStudy/assets/12410931/beea2e96-ae16-424e-a50a-7bcfc2af759b)



Thus this correlation heatmap, while it can help us with knowing what type of creature to deal with, is not gona help us with con/dex saves.

Lets study the correlation using the alternative save attributes when applicable 


![saves_corr](https://github.com/ThomasBoutonnetAntelo/AoECantripSaveStudy/assets/12410931/25160e32-4675-4c1c-b2e2-e801246b4f18)



As we can see the values are less drastic.

Interesting relations:

- The correlation between size and dex saves, and str saves and dex saves is now positive, although still quite low
- Dex saves and con saves are more correlated, possibly indicating higher saves in higher level monsters
- There's a high relation between higher ac and higher dex saves, not found in simple dex stat, also probably because of higher monster level
- Dex save is positivelly influenced by cr as we would expect (although less than con save) contrary to dex stat. This also helps the theory that a higher dex might be problematic and instead alternative dex saves are put in place.
- Con saves are almost identically correlated to cr as the con stat

zoom:

![corr_zoom](https://github.com/ThomasBoutonnetAntelo/AoECantripSaveStudy/assets/12410931/f78b0be6-d37f-4a5f-87f1-23b404543907)


So, saves have a higher positive correlation over all between them. The obvious hypothesis is that when a monster has a higher difficulty rating -cr-, it needs to have higher defenses for harder hitting heroes. Because stats can affect a variety of things, rising stat saves is an effective method of making them more resistent without completely making them invincible. This gives a natural augmentation depending on monster cr that affects every stat save, making them more correlated.



The question is: How much does higher cr monster affect the correlations?

Lets see the distribution of stats modifiers and stat final saves (taking into account alternative saves) of monsters

![saves_distribution](https://github.com/ThomasBoutonnetAntelo/AoECantripSaveStudy/assets/12410931/1b2325dc-3f43-42ed-afed-197037c787e7)


Clearly the correlations are very influenced by the challenge ratings. Stat saves get way higher and different than stat mods depending on cr.
This means correlations might be skewed by the strong relation with the challenge rating depending on the cr bracket.


<br />

---

Summary:

We have seen smaller creature gets higher dex, but not by that much. The dex stats is also quite static all along the monsters' cr level, making size the only variable, even if subtle. But, dex saves do scale very slightly with size and strength. So, the smaller the creature, it might actually get lower dex saves (although not by that much again, it's practically static until higher sizes). What is sure is if it's smaller it definitely get smaller con saves.

![dex_saves_by_size](https://github.com/ThomasBoutonnetAntelo/AoECantripSaveStudy/assets/12410931/52ac49a5-b89e-4e63-a884-7b40240c5968)


We have also seen that the dex stat doesn't get higher when the challenge rating augments, so a bunch of lower level creatures can be as dexterous as a single big bad boy on the field. But the dex save slightly augments as cr augments too, so that big bad boy might get better saves than the smaller ones, who could be more vulnerable to our dex cantrip.

As we explained just above, cr has a big effect on saves. This means we cannot have an overall look into monsters without considering cr. Anyways a group of adventurer won't fight monsters with very different crs, instead they will fight monster in a specified bracket more adjusted to their level. So, a better look could be based on cr.


#### 2.3 Mean dex and con by cr
 
<br />

Lets try to see mean mods and saves by cr levels. We will plot the amount of creatures in each cr level to better see why some numbers are so out of line (see cr 12)

![mean_dex_con_by_cr](https://github.com/ThomasBoutonnetAntelo/AoECantripSaveStudy/assets/12410931/0b7144a5-f66b-4d36-90f9-fbe8cb2391b3)

![mean_dex_con_SAVES_by_cr](https://github.com/ThomasBoutonnetAntelo/AoECantripSaveStudy/assets/12410931/f4f7c292-06c6-49b7-ac34-4925ada5655f)



Now this is something

We can clearly see the observations we made before on this.

- Dex stat varies over a static bracket
- Dex saves do get higher but, as explained before, it's thanks to the augmentation in higher cr brackets. If we take the bracket between 0 and 5 cr it is more or less constant, it even gets lower from 1 to 5.
- Con stat and its saves simply gets higher with cr

Well, that is quite conclusive. What we can see is that depending on the cr it might be better to use con over dex stat at lower levels, while it is normally much more preferable to use dex saves at higher levels. Of course the possible deviation from the mean has to make us wary of this simplification, but as a rule of thumb:

When cr is lower than 2:
**CON saves are the winner!**

Wehn cr is higher than 2:
**DEX saves are the winner!**

<br />

### Conclusion

<br />

#### 3.1 Verification and Rule of thumb

<br />

So, we have created thanks to our observation a rule of thumb where ***con*** **saves are lower thus better against at cr<2, and** ***dex*** **saves are lower thus better against at cr>2**. This is quite the predicament, is it really an useful rule of thumb? To be critical of our own conclusions, lets verify our predictive rule.

Lets calculate the precision of the rule on each cr level to see how it applies. We will calculate the percentage of monsters whose dex & con relation (<, = or >) is the same or not as the relation between the means. 
        
        i.e. : 
        monster's dex save > con save, 
        but monster's cr dex save mean < con save mean 
        => our means relation doesn't encompass this monster's save relation, thus rule of thumb fails for monster


![rule_of_thumb_accuracy](https://github.com/ThomasBoutonnetAntelo/AoECantripSaveStudy/assets/12410931/096c0bcc-94ef-4a4f-9b02-8d2ccc979122)



Taking into account that monsters whose dex and con saves are equal don't skew our choice, we can safely say that our rule of thumb has around 75% accuracy throughout every cr level in the Player's Handbook monster list. (The cr 12 dip is caused by the very small pool of monsters skewing the results)

This resolves the debate about which is best between **dex** or **con** saves. It is evident that at higher cr than 2 dex saves are lower for us to abuse, in front of an ever rising constitution. In lower cr brackets constitution is lacking, making it perfect for our low level AoE spells. We have also proven a misconception about size: **smaller creatures don't have strictly higher dex saves**, it stays quite static by size until the biggest ones which see an augment. On the other hand constitution saves do get lower depending on size. Comparing these two will give constitution a better outcome, but for tiny and small creatures only. 

Maybe other stats or characteristics might influence our choice of save, but as an overall choice our rule of thumbs has a pretty high succes rate. 


Keeping in mind this study was done only using the Player's Handbook as a source, adding other sources might complete or change our study. Future research should be interesting.




As a conclusion statement we can only but frame our rule of thumb:  

      When cr is lower than 2 use **CON saves** when cr is higher than 2 us **DEX saves**
