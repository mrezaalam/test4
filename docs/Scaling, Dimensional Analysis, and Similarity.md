
## Motivation
Is there anything we can learn about forces on and behavior of a big ship if we do a laboratory test on a scaled model (smaller replica) of that ship?  

In the old days, people used to think that the only way to study a ship's performance is to build a full-scale prototype and test it in the actual ocean environment (say under strong waves). They used to look down on any laboratory experiment as playing with toys with little to no relevance to real world response of a full-scale prototype. 

Basically, this was the question:
- Let's assume we make a 1/10 scaled model of a big ship. 
- If we want the scaled replica (that is, the model) to move with the speed 1/10 of the speed of the actual ship
- Then how much propulsion power do we need? 1/10 of the propulsion power of the actual ship? more? less?

The first thing that may come to mind could be that, yes, let's scale everything by the scaling factor. But laboratory experiments showed that with a 1/10 of the propulsion of the actual ship, the model would move much faster than the 1/10 of the actual ship speed, and also the wave pattern on the water has no resemblance to the wave pattern of an actual ship. So, people were right to be skeptical of scaled model tests. No qualitative nor quantitative agreement could be seen between the two tests. 

We already know that not everything scales with geometric scaling. For example, a block of double size of another block weighs 8 times higher (see the question below). Therefore, why should velocity and propulsion scale the same as geometric scaling of a model vs a prototype?

##### Question: Does weight scale with size?

Consider two weights made of the same material. The larger weight is a gematrical replica of the smaller one with the scaling factor $s=2$. Does the weight of the larger weight scale with the same scaling factor $s=2$? In other words, does the larger weight weigh double the smaller weight?

![[Pasted image 20230403233634.png|300]]
Figure: Two weights, with scaling factor $s=2.$

Answer: This is a simple question to show that not everything scales with the geometric scaling. Clearly, weight is proportional to volume (for the same materail), and therefore
$$
\frac{W_L}{W_\ell}=\frac{M_L\ g}{M_\ell\ g}=\frac{\rho_L V_L}{\rho_\ell V_\ell}=\frac{V_L}{V_\ell}=\frac{\pi R_L^2 h_L}{\pi R_\ell^2 h_\ell}=\frac{R_L^2h_L}{R_\ell^2h_\ell}=s^3.
$$
Therefore, for two objects of the same geometric shape but scaled with the scale $s$, weights scale with $s^3$. In our example, the larger weight is 8 times heavier than the lighter weight. 

#####

As for the ship problem, William Froude was the first who showed that if we scale different parameters (time, speed, force, power) properly, then the scaled model behaves exactly the same as the actual full-scale prototype. And this was easy to show. Many researchers around the time of Froude had came up with a similar idea for other fields of science and engineering. The technique is called today "dimensional analysis" or "dynamic similarity"



## Dimensions
Every physical quantity has a nature which is universal. For example, the width of the room that you are sitting in has a nature of *length*. The nature of the *width of the room* is not mass nor time. It is length and it is universal. That is, if you go to Mars or Jupiter or anywhere in the world, it is still *length*. We call this nature of physical quantities their **dimension**. The three most important dimensions that are relevant to fluid dynamics are Length, Mass and Time. We show them respectively with $L$, $M$ and $T$. When talking about, say, width of a room $\w$, we write $[\w]=L$ and read *the dimension of the width of the room (or $\w$) is length*. 

##### Question What is the dimension of $2\w$?
The dimension of two times the length of a room ($2\w$) is still length. Remember options here are length, mass and time, and the dimension of $2\w$ is not mass or time, but it is still length. Therefore we write
$$ 
\ba \nn
[2\w]=L.
\ea 
$$
#####
When working with physical quantities, we have to be careful to only compare quantities with the same nature (or dimension). This sounds trivial: of course we cannot compare the width of a book with the mass of a laptop. Therefore, let's express this as a principle:
> [!danger]+ Principle
> We can only compare quantities that have the same dimensions.

By compare what I mean is equality ($=$), inequalities ($<,>$), and approximations ($\sim,\approx$, read respectively *about* and *approximately equal to*). Clearly, also we can only add or subtract quantities with the same dimension. Can we add the life of an animal to its mass? of course not!

We use the above principle in two ways:
> [!danger]+ Application
> - To find out dimensions of new quantities 
> - To check whether an equality or inequality is *meaningful*

To find the dimension of a new quantity, we need to find a formula that relates our new quantity to quantities with known dimensions. Let's see how we do that through an example.
##### Example: What is the dimension of the area of a room?
Area of a room $A$ is given by
$$ 
\ba \nn
A=\w\times \ell
\ea 
$$
where $\w$ is the width and $\ell$ is the length of the room. According to our principle, the two sides of the above equation must have the same dimensions, therefore,
$$ 
\ba\nn
[A]=[\w\times \ell]=[\w] \times [\ell] = L \times L = L^2.
\ea 
$$
#####
##### Example: What is the dimension of Force ($F$)? 
The same procedure can be followed to find dimensions of other quantities. For example to find the dimension of force, we first have to look for an equation that expresses $F$ as a function of more basic quantities, for example $F=ma$ where $m$ is the mass of a particle and $a$ is its acceleration. We know that $[m]=M$, but We need to find the dimension of acceleration. One equation that relates acceleration to more basic quantities is $a=v/t$ where $v$ is velocity and $t$ is the time, and velocity can be given by $v=x/t$ where $x$ is the distance. Therefore,
$$ 
\ba\nn 
[v]=[x/t]=[x]/[t]=L/T=LT^{-1},
\ea 
$$ 
and then 
$$ 
\ba\nn 
[a]=[v/t]=[v]/[t]=LT^{-1}/T=LT^{-2},
\ea 
$$ 
and then 
$$ 
\ba\nn 
[F]=[ma]=[m]\times [a]=M\times LT^{-2}= MLT^{-2}.
\ea 
$$ 

Similarly, dimensions of volume ($\V$),  density ($\rho$), Energy ($E$), Power ($\P$), pressure($P$) are as follows: $$\ba
[\V]&=L^3,\nn\\
[\rho]&=ML^{-3},\nn\\
[v]&=LT^{-1},\nn\\
[a]&=LT^{-2},\nn\\
[F]&=MLT^{-2},\nn\\
[E]&=ML^2T^{-2},\nn\\
[\P]&=ML^2T^{-3},\nn\\
[P]&=ML^{-1}T^{-2}.\nn
\ea$$
#####
##### Question: In calculating dimension of a quantity, does it matter which equation we use?
No, For example consider Energy, and use the following formula to calculate its dimension:
$$ 
\ba\nn 
E&=F.x, \nn\\
E&=mc^2, \nn\\
E&=\frac{1}{2}mv^2, \nn\\
E&=mgh. \nn
\ea 
$$ 
where $x$ is the distance traveled, $c$ is the speed of light, $v$ is the speed of the object, $g$ is gravitational acceleration and $h$ is the height. 
You should get $[E]=ML^2T^{-2}$ from all these four formulae.

#####
##### Question: What is the dimension of the angle $\theta$? 
To answer this question, we have to note the way we define an angle. An angle $\theta$ is defined as the ratio of the length of the arc $AB$ (denoted by $S$ is the figure below) to the radius of the arc $R$, that is
$$ 
\ba\nn 
\theta=\frac{S}{R}.
\ea 
$$ 
For example, when we say an angle is 1 radian, it means its arc length is equal to the radius of arc. An angle $2\pi$ radian (i.e. full circle) means the arc length is $2\pi R$ which is the perimeter of a circle with the radius $R$.

![[definition_of_angle 1.svg]]

Therefore, it is easy to see that
$$ 
\ba\nn 
[\theta]=[S/R]=L/L=1.
\ea 
$$ 
In other words, the dimension of the angle is unity or we say that the angle is *dimensionless*.

Three dimension angle (or solid angle) is called *Steradian* and is defined similarly. It is the area of a surface cut by the 3D angle (A), divided by the square of the radius, that is, 
$$ 
\ba\nn 
\Omega=\frac{A}{R^2}.
\ea 
$$ 
Solid angle is also dimensionless. 
![[Steradian.svg]]

#####
##### Example:  What is the dimension of Planck's constant? What unit do we use to express its value in the SI system of units?

Photon energy is given by the so-called  Planck-Einstein relation:
$$ 
\ba\nn 
E=\hslash \omega
\ea 
$$ 
in which $E$ is the energy, $\hslash$ is called Planck's constant and $\omega$ is the frequency of light. 

Angular frequency $\omega$ is defined as how much angle ($\theta$) is covered in unit time, in other words $\omega=\frac{d\theta}{dt}$ (compare this with linear velocity which is distance covered in unit time). Therefore$$ 
\ba\nn 
[\omega]=[\theta/t]=1/T=T^{-1}.
\ea
$$ Dimension of $\hslash$ then can be readily found from the Planck-Einstein relation
$$ 
\ba\nn 
[\hslash]=[E/\omega]=ML^2T^{-2}/T^{-1}=ML^2T{-1}.
\ea 
$$ 

To find the unit for $\hslash$ in the SI system of units, we have to use kilogram for mass, meter for length, and second for time. Therefore the unit for $\hslash$ is $kg.m^2/sec$. From accurate measurement we know that $\hslash=1.0546\times10^{-34}\ kg.m^2/sec$. Note that since $\hslash=E/\omega$, and *Joules* is another unit for energy, $\hslash$ is sometimes expressed in units of Joules.seconds, in other words $\hslash=1.0546\times10^{-34}\ J.s$.

#####

The second use of our principle, as mentioned before, is to check whether an equality or inequality is *meaningful*. If I am comparing (or adding or subtracting) the width of my table with the mass of my computer, this is simply meaningless. But if I compare the width of my table with the length of the table, then this comparison is (at least dimensionally) meaningful, although it may be correct or incorrect. For example, if the width is equal to the length and if I say *the width of the table is larger than the length of the table*, then this statement is (dimensionally) meaningful but is incorrect. If I say *the width of the table is equal to the length of the table*, then this statement is (dimensionally) meaningful and also correct. 

##### Example: Is the expression $P=\rho g h  + \rho v^3$ dimensionally correct?
Let's assume you have solved a complicated problem and you arrived at the final answer above $P=\rho g h  + \rho v^3$, where $P$ is the pressure. Let's check and see whether this expression is dimensionally correct and hence is meaningful. 
$$ 
\ba
[P]&=ML^{-1}T^{-2}\\
[\rho g h]&=ML^{-3} \times LT^{-2} \times L =ML^{-1}T^{-2}\\
[\rho v^3 ]&=ML^{-3} \times (LT^{1})^3= MT^{-3}
\ea 
$$ 
clearly the third term has a different dimension than the first and second term.

We usually can go further by looking at why there is a dimension mismatch. For example, here it seems that a $T/L$ is missing in the third equation. The dimension $T/L$ can be the dimension of $1/v$  (it can be also the dimension of millions of other quantities). Therefore, maybe the correct expression *could be* $\rho v^3/v=\rho v^2$, or $\rho v^3/v_1$, or else. These guesses usually are very helpful in tracing back the final expression and find the mistake within the derivation.
#####

The expression in Example above is dimensionally incorrect. This expression is as *ridiculous* as comparing the width of a table with its mass. Obtaining such expressions, which are not uncommon, usually arises from a mistake in the derivation. Note that how easily and with such a basic mathematics we are able to catch a mistake in a formula. The *dimension check* has helped many scientists and engineers catch mistakes in their work, and has helped projects save a lot of money, time and even lives. 

Dimensional mismatch is considered the biggest sin in science and engineering. When the author was a highschool student, in one of his midterm exams he fully solved a very difficult problem that no one else in his class was able to solve. But his final answer, because of a stupid mistake in one of the steps, was *dimensionally incorrect*. He received zero on that problem. As a revenge to that memory, the author now gives an absolute zero to every dimensionally incorrect final answer that his students turn in. 


## Units
Physical quantities are measured in terms of units. Contradictory to dimensions that are universal, units are not. People use different units to measure physical quantities. For instance, for length some use meters and some use feet. They are all fine, as long as you are consistent in your calculations (that is, you cannot use one set of units for part of your calculations and another set for another part). 

Units for length include, for instance, meter, kilometer, inch, mile, foot, and the length of your arm (yes, you can define your own unit). Units for Mass include, for example, gram, kilogram, and pound. Units for time include, for instance, second, hour, minute, day, and month. 

##### Question: *Light year* is a unit for what quantity?
Light year is the *distance* that light travels over a time period of one year. Therefore it is a unit for length. It is 9.5 $\times$ 10$^{15}$ meter which is about 25 million times the distance of earth from the moon, or about 65 thousand times the distance of earth from the sun. So really a long distance. 
#####

Different fields in science sometimes use their own units. For example in astrophysics, mass of stars are expressed as a function of the mass of the sun (or *solar mass* shown with $M_\odot$$\sim 2\times 10^{30}$ kg). This is a good choice, because otherwise we have to work with extremely large numbers which are difficult to write, read and memorize and also do not immediately give insights into relative size of each planet. 

##### Question: What happens to our sun at the end of its life? Does it turn into a black hole?
No. Our sun at the end of its life swells to a very large size (called a red giant) and swallows mercury, Venus and probably Earth (this happens in a bout 5 billion years from now, so no worries, we have plenty of time!). It then sheds its outer layer and its core squeezes to a so-called *white dwarf*. A white dwarf is like a large planet with no fusion inside (and therefore little to no brightness). If earth is not already evaporated by the red giant phase of the life of the sun, then when our sun turns into a white dwarf it will freeze to death.   

Stars as large as 10$M_\odot$ still likely turn into a white dwarf at the end of their lives. I used the word *likely* because the exact answer depends on how much red giant sheds away, and how much of core mass is left. As long as the core is 1.4$M_\odot$, then the core turns into a white dwarf. This limit of 1.4$M_\odot$ is called the Chandrasekhar limit. 

Stars with a mass between 10$M_\odot$ and 30$M_\odot$ collapse into a *Neutron Star*. For such stars, the core mass (or remaining mass after outer layer shedding) and its resultant gravitational field is so heavy that electrons and protons are fused together to form dense Neutrons. The constituent of a Neutron star is so heavy that a table spoon of it weights about one billion tonne! 

If a star core has a mass larger than 3.2$M_\odot$, then Neutrons also break and the star turns into a hyper dense body called a black hole. The gravitational pull of a black hole is so strong that even light cannot escape from it. To give you an idea of how much density we need let's consider earth. If we want to make a black hole out of earth, then its mass must be squeezed to a sphere of diameter 1cm! (you can calculate this radius yourself through the Schwarzschild's radius formula: $R_s=2G\M/c^2$, where $\M$ is the mass (in kg), $G\sim 6.7 \times 10^{-11} \ m^3/kg.s^2$ is the gravitational constant, and $c\sim 3\times 10^8 \ m/s$ is the speed of light.
#####
The mostly wide system of units used in the world is the "International System of Units" or in brief "SI" unit (abbreviated from the French *Systeme international*). SI unit is based on decimal system, or numbers in a base 10. In a base 10 numerical systems, we count numbers from 0 to 9 with unique characters (e.g. 7 and 8 look different), but then after 9, the character for follow up numbers is a combination of the previous characters (e.g. 10, 278, etc). In a binary numeral system, which is base 2, the same story holds, we numbers up to the base (which is 0 and 1), and then for the base(that is, 2) we use a combination of characters before. So 2 in a binary system is 10, 3 is 11, 4 is 100, and so on. 

##### Question: Why does everybody use decimal numeral system?
First of all, not everybody uses decimal numeral system, at least not throughout history. For example Babylonians ($\sim$ 3000 BC) used a base 60 numeral systems, Mayas ($<$ 5th Century) had a base 20 numeral system, some languages in African have had base 12, and some languages in Papua New Guinea have a base 27. 

But the likely reason most cultures and civilizations are based on 10 is that we have 10 fingers. Therefore, that is the first thing that should have come to people's mind. 
#####
##### Question: Is this decimal system really the optimum? or maybe we should think to change?
It will likely result in not much difference if we change the base a few numbers below or above 10 (say 7 or 14). The issue with much lower numbers is that the length of numbers become large. For example 100 in base 10 when converted to base 2 becomes 1100100, meaning you have to use 7 digits instead of 3 by going from base 10 to 2. With a larger base the number of digits required to represent a specific number decreases, but we need to memorize more characters for the basic numbers comprising the numeral system. For instance for base 12, we need to define new symbols for 10 and 11 (Some argue the the reason *eleven* and *twelve* are written slightly different from their constituents (that is, one ten and two ten) is because 12 has been the base in the past). 

Therefore, 10 may seem to be a good compromise. Isn't 12 better? well, maybe, maybe not. Number 12 is a neater number, with many interesting properties. It is divisible by 2,3,4 and 6, whereas 10 is only divisible by 2 and 5. But then the counter argument is what is the advantage of our base being divisible by more numbers? Isn't it better that we use a prime number (e.g. 11 or 7) that is not divisible at all? The argument can go forever. Therefore, in the absence of a strong argument for any specific other base, we keep base 10. 
#####
Once we set a numeral system as our standard, it is much easier to use a system of units based on the chosen numeral system. That has been the argument behind SI system of units: since we have chosen *decimal numeral system* then we try to define units that are easily convertible by factors of 10. For example, 250 meters is simply a quarter of a Kilometer, or 500 grams is half a Kilogram. 
##### Question: Should SI extend to more realms, e.g. number of hours in a day? Number of days in a week?
French in fact thought about that during the revolution. They even invented the 10-hour clock (figure below, which I personally believe is a good idea. If it is for the total 24 hour, then it eliminate the need for AM/PM, and also calculations become much easier. For example, do you know 20 minutes is what fraction of a day? In a 10 hour clock system, when you say I studied 15 Centi Hour, it is immediately clear that you have studied for 0.015 of a day (which is close to 20 minutes).
![[ten_hour_clock.jpg|300]]
Figure: Ten hour clock ([ref](http://nowiknow.com/the-failed-attempt-to-create-a-ten-hour-day/)).
 
They went on to make a 10 day week. If it was adopted, we now would work 7 consecutive days and then had a 3 day weekend, wouldn't that be nice? But then there is this element of history and religions that must be taken into account. It is also to be noted that we cannot extend this to everything. A year is a creepy 365.25 days that does not fit in SI nor Imperial nor any other integer-based numeral system. 

At the end the standard decimal units was accepted for mass and length, but not for time. Reason: likely because trade was based on mass and length but much less based on time. So people thought the current system for time is good enough and that if they stick to it, they don't have to change their clocks which seemed unnecessary to them.
#####
There has been a long political, logical, cultural, etc. debate whether Untied States has to convert to SI or keep using Imperial units. Getting into those debates if beyond the scope of this book, so we accept the fact that there are two system of units in the world, SI and Imperial, and try to become adept in converting the two to each other quickly and accurately so that we can design safe machines and bridges and spacecrafts both in the US and in the rest of the world.

## Dimensional Analysis


Debt-To-Income (DTI) ratio is a critical number to get approved for a mortgage. DTI is the percentage of your income that goes toward paying your monthly debts. Lenders are usually not comfortable to give loans to people whose DTI become larger than 33%. Note that here the net income does not matter, the net loan value does not matter, but it is the ratio. Also, it does not matter whether your income is in US dollar, or EURO, or Yuan or else. It is the *dimensionless* ratio of DTI that matters. 

Golden ratio
 $$ 
\ba
\phi=\frac{1+\sqrt{5}}{2}\approx1.618
\ea 
 $$ 