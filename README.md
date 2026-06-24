# Where is the Math in... Molecular Symmetry Approximations
By: Trejo Aceves Luis Enrique
Research made for understanding the purpose of the 5th power rule and the usefulness for approximating real behavior of materials
## About Me
<div align="center">
<img width="50%" height="50%" alt="SAM_0009" src="https://github.com/user-attachments/assets/bd0babb6-93ed-4bb7-9b2c-6ccde2de30dc" />
</div>

My name is Luis Trejo, as of today I am pursuing my bachelors degree in Chemistry with minors on Mathematics and Biological Sciences. During this studies I came across physical chemistry and Inorganic Chemistry courses, dedicated intensively on the behavior of molecules as well as the energy splitting that gives out the common and known colors of reactions we are used to see behind "classic" science experiments. This gave me a huge interest on understanding the behavior of this molecules when trying to achieve this colors, getting involved in terms such as molecular symmetry, wavefunctions, vectors, and coordinates giving me a major focuse on molecular models to predict reactions. This topic can be complex to understand for which I prepared by taking the following math courses that allowed me to understand the concepts behind this branches of theoretical chemistry:

- Calculus I
- Calculus II
- Calculus III
- Physical Chemistry I
- Physical Chemistry II
- Mathematical Modeling (currently being taken)

The idea behind my research is to give a meaning to the theoretical models, which studies metals and their compounds. These metals often arrange themselves in beautiful, symmetrical shapes. But real molecules are never perfectly symmetrical. So chemists use mathematical approximations to correct for these imperfections. These models however are often optimized into "ideal" forms that don't perfectly match real life. This is why I'm fascinated by molecular symmetry approximations, especially where we work with coordination metals and a very important concept named "The Crystal Field Theory".

For the motives behind my research and the interest in mathematical modeling in this area please look at the following video:

(Inserta video con feedback de mis compañeros que aun no tengo aqui._.)

## Part 1: What Are Molecular Symmetry Approximations? (Non-Chemist friendly)

Imagine a friend asks for the hour, you can read your analog watch but instead of saying it's 10:58 you say it's 11 o'clock, you could address the real value but you choose to approximate the hour to the nearest full hour, the answer was "good enough". On greater scale imagine you're trying to predict the weather. The "perfect" model would consider every single air molecule on Earth. But it is unachievable so meteorologists use approximations because they are "Good enough" (and yet we find a downpour when it is supposed to be sunny).

<div align="center">
<img width="50%" height="50%" alt="If-You-See-a-40-Chance-of-Rain-This-is-What-It-Means-1200x1200-1" src="https://github.com/user-attachments/assets/b5be5820-ce72-4ed8-aed1-f8b452bbf576" />
</div>

Chemistry works on the same principle, >90% of the achievements are based on theories and approximations and molecules are the basics behind it. When chemists study molecules, the "perfect" model (grabbed from quantum mechanics) is incredibly complex. So we use approximations, since simpler mathematical models that give us good enough answers to work with. However we are still working with the idea of symmetry which unfortunately does require as much accuracy as possible.

### What Does "Symmetry" Mean in Chemistry?

Imagine working with a metal cube that has the same look in all faces, if you rotate it 90º you will see the same look of it, so for 180º, so for 270º, since it is symmetrical you can rotate it and will look the same, split it in half in any face and will be symmetrical. Molecules work under the same principle but way more complex. For example:

- **Octahedral** (like a 6-sided dice): 6 ligands (atoms or molecules) arranged around a central metal
- **Tetrahedral** (like a pyramid): 4 ligands arranged around a central metal
- **Cubic** (like a cube): 8 ligands arranged around a central metal

<div align="center">
<img width="50%" height="50%" alt="xxewzsjdib" src="https://github.com/user-attachments/assets/74c22987-52af-4dc6-ae32-e7d14b8fe801" />
</div>

So far ideally we should be able to understand the behavior of it except by the small problem...

### The Problem with Perfect Symmetry

Real molecules are never perfectly symmetrical. They bend, stretch, and wiggle. The ligands (the atoms surrounding the metal) might be slightly different sizes or at slightly different angles.

So chemists have two choices:
1. Do the exact math (which is incredibly difficult and time-consuming)
2. Use approximations (trading accuracy but and give us "good enough" answers)

## Part 2: The Core Concept - Crystal Field Theory (In simple terms)

Now let's look at one specific approximation: **Crystal Field Theory**.

### Part 2: What Is Crystal Field Theory?

Let's say we have a metal atom (imagine any metal but it would be better if it is on the d-block of the periodic table) with electrons orbiting around it. Around this metal, you have ligands, this ligands can be basically any atom that can be attracted by the metal, although normally it is preferred that it is an organic molecule (composed of carbon or nitrogen)

But how How do these ligands affect the electrons?

In an ideal world, all the electrons would have the same energy. But what really happens is that these ligands push and pull on the electrons, causing them to have higher or lower energy.

These changes in energy is defined as crystal field splitting

A simple way to explain this splitting is by the following video:

https://www.youtube.com/watch?v=V1WSesBeURw

This is also a great explanation for the color change in metallic complexes

<div align="center">
<img width="50%" height="50%" alt="SAM_0012" src="https://github.com/user-attachments/assets/d091ec9e-1e87-4493-838e-b442285c8fc3" />
</div>
(Yes, I took this photo)

But how can we take this for our modeling?

For this we must pretend each ligand is just a tiny, negatively charged point, then we calculate how these point charges affect the electrons on the metal using good Coulomb's Law

<div align="center">

$$F = \frac{k q_1 q_2}{r^2}$$

</div>
(In case anyone forgot)

With this we can use the math to predict how the electron energies split
And that's it right? Well... no, it is a good approximation but it doesn't give the full image. Because ligands aren't really point charges, but rather complex molecules with their own electrons. But it is "good enough" to predict patterns.

So in order to get closer we now get to use tons of math... I would lie if I tell you it is gentle, but here is in the most simple terms that are possible to have:

First we need spherical coordinates (r, θ, φ)
<div align="center">
<img width="50%" height="50%" alt="Screen Shot 2026-06-22 at 10 32 15 PM" src="https://github.com/user-attachments/assets/785ef98a-05ea-40da-98c7-f87f847b0048" />
<img width="50%" height="50%" alt="Screen Shot 2026-06-22 at 10 35 48 PM" src="https://github.com/user-attachments/assets/f5f3f13d-e851-4d43-9be7-a00ac0aadea0" />
</div>

Well this same idea can be applied for atoms in this concept since we need to know exactly where each ligand is located around the metal. Using this idea we correlate

- **r** = distance from the metal (bond length)
- **θ** = angle from the z-axis
- **φ** = angle from the x-axis

Now we can actually start working with physics
$$F = \frac{k q_1 q_2}{r^2}$$

From Coulomb's law we can know how charged particles interact. applied to our topic, we use this to calculate the force between:

- The negatively charged ligands (q₁)
- The electrons on the metal (q₂)
- The distance between them (r)

In case anyone is interested into a deeper meaning for Coulomb's law feel free to check this very well explained video for it. https://www.youtube.com/watch?v=kCp5yYjo9zE

All this leads us to use a model called **PCEM** (Point Charge Electrostatic Model). And while we can remain with it as it is this can give us a good amount of information about the ligands... but not about the length. How can we fix this? With series and Harmonics (Buckle up... this will be awful, no more sweet terms)

As very straightforward as Coulomb's law seems it can be very complex to work with, so the solution for it is to expand it on simpler terms... This achieved by the Laplace expansion and Taylor series. Why this? Coulomb's law depends on both distance and direction and we want to cover them independently. So the expansion makes it an infinite series where we get a radial and angular parts

## In 1D, Taylor series says:
Any smooth function f(x) can be written as:

<div align="center">
  
$$
f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n
$$

</div>


## In 3D, Laplace expansion does the same thing for functions on a sphere:

<div align="center">
  
$$
\frac{1}{|\mathbf{r} - \mathbf{R}|} = \frac{1}{R} + \frac{r}{R^2}\cos(\theta) + \frac{r^2}{R^3}\frac{3\cos^2(\theta)-1}{2} + \cdots
$$

</div>

And each term represents a greater complexity...

While we could work with Taylor series "Good enough" we level it up a notch by making it 3D with Laplace and now that we work with volumes we have:

<div align="center">
  
$$
\frac{1}{|\mathbf{r} - \mathbf{R}|} = \sum_{k=0}^{\infty} \sum_{q=-k}^{k} \frac{4\pi}{2k+1} \frac{r^k}{R^{k+1}} Y_{kq}^*(\theta, \phi) Y_{kq}(\theta', \phi')
$$

</div>

If it sounds confusing... it's because it is, so this can be helpful in understanding this concept:

https://www.youtube.com/watch?v=cAARX18-74g

Then with Laplace we expand into Spherical Harmonics, the first physical chemistry concept that we need for derivating

**What Are Spherical Harmonics?**

Spherical harmonics (Yₖᑫ) are special functions that describe how something varies over a sphere. They're the 3D equivalent of the sine and cosine

**in order to see them better think of them like this:**
- Y₀⁰: A perfect sphere (like a ping pong ball)
- Y₁⁰: Like a peanut shape (dipole)
- Y₂⁰: Like a dumbbell shape (quadrupole)
- Higher k values: More complex, petal-like shapes

<div align="center">
<img width="50%" height="50%" alt="Complex_Spherical_Harmonics_Figure_Table_Complex_Radial_Magnitude" src="https://github.com/user-attachments/assets/fba6c682-ee7a-42c1-b684-00dedfc81a7c" />
</div>

Here is the charm though... the reason why we need this harmonics is because this expansion allows us to grab for all infinite values, we want to cover them all. In very short terms we can say that we use series, harmonics and expansions to get a full set of values, we cover it all.

Now we can grab it and actually work on Crystal Field Theory and the so called fifth power rule... (Finally)

## Why does it work?

For d-electrons (which have angular momentum quantum number l = 2):
  
Before reaching this part we must begin with a CRUCIAL definition, "k". What is this? This are tensors or ranks

## What is a tensor?

Is just a fancy word for something that transforms in a specific way when you rotate your coordinate system. it works in the format of ranks where:

Scalar (rank 0)	Just one number, like temperature
Vector (rank 1)	A list of numbers pointing in space, like	Velocity
Tensor (rank 2)	A grid of numbers like pressure or inertia
Rank-k tensor	A multi-dimensional grid like our spherical harmonics

With that in mind...

1. We have selection rules from quantum mechanics which tell us that only certain k values can contribute:
   - k = 0, 2, 4 (all even numbers up to 2l)
   - k = 1, 3, 5 (odd values) are forbidden
    
2. The k=0 term just shifts all energies equally (no change at all)
   - Scale: 1/R¹

3. The k=2 term gives a 1/R³ dependence
   - This is the "quadrupole" contribution that we find in tetrahedral molecules

4. The k=4 term gives a 1/R⁵ dependence
   - This is the "hexadecapole" contribution (our 5th power rule for octahedrals)
  
Finally... we can actually derivate this rule

## Part 3: The fifth power rule

### What Is the 5th Power Rule?

In simple terms it is the energy splitting of electrons depends on the 5th power of the bond length.

<div align="center">
  
$$
\Delta \propto \frac{1}{R^5}
$$

</div>

Where:
- **Δ** = energy splitting (how much the electron energies separate)
- **R** = bond length (distance from metal to ligand)

Ok... and for non chemists? What does that mean?
Imagine you have a rubber band. If you stretch it the force changes... That's it

The 5th power rule is like that

- If the bond length changes by 1%, the energy splitting changes by about 5%
- If the bond length changes by 10%, the energy splitting changes by about 61%!

So small changes in molecule structure cause HUGE changes in properties

All this for that? Yes, tiny yet complex... but now that we have the pieces we add them up together:D

## But first... a very quick recap
1. We start with the potential energy equation (Coulomb's law)
2. We expand it using spherical harmonics (Laplace expansion)
3. For d-electrons (the ones we care about in metals), only certain terms survive
4. In octahedral symmetry (our "perfect" case), the terms that survive have a fifth power rule dependence

So we get from this and a very excruciating derivation final energy splitting is:

<div align="center">
  
The final energy splitting is:

$$
\Delta = \frac{2}{7}B_{40}
$$

Since $B_{40} \propto \langle r^4 \rangle / R^5$, we confirm:

$$
\Delta \propto \frac{1}{R^5}
$$

</div>

And that's it right? Ideally yes, on perfect octahedral symmetry that is in fact all there can be... But real life is not perfectly symmetric, meaning we need to approximate to the ACTUAL values.

In short... 

## Part 4: Adressing when the rule fails

The 5th power rule works beautifully for perfect octahedral symmetry. But real molecules aren't perfect

In a low symmetry environments (like garnets, nitrides, or distorted molecules), the rule breaks down because:

<div align="center">
  
- The $k=2$ terms don't cancel out anymore
- This adds a $1/R^3$ dependence

So the energy splitting becomes:

$$
\Delta = A \cdot \frac{1}{R^3} + B \cdot \frac{1}{R^5}
$$

Where $A$ and $B$ are constants determined by the specific symmetry.

</div>

# Why does this matter? 

This mix of 3rd and 5th power rules is what makes luminescent materials (like those used in LEDs and phosphors) work The colors they emit depend on exactly how these terms combine.

Taken to a greater scale... this alone allows us to address for actual behavior of all types of octahedral molecules... without fancy equipment, without the an inmense use of money... with pure mathematical modeling.
