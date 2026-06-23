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

### What Is Crystal Field Theory?

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
<img width="50%" height="50%" alt="electrostatic-force-equation" src="https://github.com/user-attachments/assets/1f540163-715a-4dc1-9f19-470283c19c6d" />
(In case anyone forgot)
</div>

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
