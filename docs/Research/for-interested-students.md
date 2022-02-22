---
layout: page
title: A Letter for Interested Students
exclude: true
permalink: /ForInterestedStudents/
usemathjax: true
---

Information for students interested in working in my group, or numerical relativity in general

Table of Contents
- [Who we are and what we do](#who-we-are-and-what-we-do)
- [Gravity takes on a life of its own](#gravity-takes-on-a-life-of-its-own)
    - [Light cones and the meaning of temporal order](#light-cones-and-the-meaning-of-temporal-order)
    - [Gravitational waves](#gravitational-waves)
    - [Black holes](#black-holes)
    - [What equations go into a numerical relativity simulation](#what-equations-go-into-a-numerical-relativity-simulation)
- [Thick disks and hypermassive stars](#thick-disks-and-hypermassive-stars)
    - [Neutron stars and their binaries](#neutron-stars-and-their-binaries)
    - [Supramassive and hypermassive stars](#supramassive-and-hypermassive-stars)
    - [Dynamical vs secular evolution](#dynamical-vs-secular-evolution)
    - [Categories of astrophysical equilibria](#categories-of-astrophysical-equilibria)
- [Turbulence and the great paradoxes of fluid dynamics](turbulence-and-the-great-paradoxes-of-fluid-dynamics)
    - [The difficulty of falling into a black hole](#the-difficulty-of-falling-into-a-black-hole)
    - [Peculiarities of almost perfect fluids](#peculiarities-of-almost-perfect-fluids) 
    - [Subgrid turbulence modeling](#subgrid-turbulence-modeling)

## Who we are and what we do  

Hello!  I’m pleased that you’re interested in the work going on in the
WSU numerical relativity (NR) group.  It’s a good idea for any student
to investigate many research fields and groups.  Numerical relativists
smash neutron stars and/or black holes into each other in computer
simulations to see what happens.  For many of us working in the field,
this is intrinsically fun enough to demand no further justification,
but NR simulations do have scientific value for two fields.  First,
they contribute to gravitational physics, the study of strongly curved
spacetimes.  Black holes and neutron stars are the best laboratories
for studying extreme gravity and testing general relativity that
nature has provided us.  Second, they contribute to multimessenger
astronomy, the study of violent phenomena in the universe that can be
observed using different types of signals, as opposed to just
different wavelengths of electromagnetic radiation.  The events we
model are detectable both electromagnetically and via gravitational
waves, and models are needed to make sense of the observations.  The
application to gravitational physics justifies our (fairly steady)
funding from NSF, and the application to multimessenger astronomy
justifies our (intermittent but very helpful) funding from NASA.  Most
of this money goes toward supporting graduate students; we’re grateful
to these agencies and to the taxpayers.

The NR group at WSU is led by me, Prof. Matt Duez.  It is part of the
“Simulating eXtreme Spacetimes” (SXS) collaboration, that includes
multiple academic institutions, most prominently Caltech and Cornell,
united by our common code.  There is also another relativity group at
WSU, led by Prof. Sukanta Bose and more directly connected to
LIGO-Virgo, which I also encourage you to check out.

Now for more detail on the physics we work with.


## Gravity takes on a life of its own  

### Light cones and the meaning of temporal order  

Consider for a moment the momentous consequences of the fact that
*nothing can travel faster than the speed of light*.  Imagine an event,
a particular place at a particular time (something like “the fall of
the Bastille”).  Call it P.  We can mark it on a spacetime diagram,
with time chosen to be the vertical axis.  Events are points on such a
diagram.  Light rays are 45 degree lines.  The possible light rays
(the light cone) passing through P divide all of spacetime into three
regions.  Above is the future of P.  A signal or object traveling at
less than the speed of light can go from P to any of these events.
These events can be affected by what happened a P; participants at
those events might remember P.  Below is the past of P.  Signals and
objects moving at less than the speed of light can go from these
events to P.  What happens at P is affected by them.  These relations
of influence and memory, of cause and affect, are what we mean by
“past” and “future”.  Time simply is the order of causality.  If this
is so, then the other events, not connectable to P by a physically
traversable path, are neither in P’s past nor in its future.  They
have no causal, hence no temporal, relation to it.  Indeed, different
global Lorentz frames will disagree about whether P or any of these
other events happen first.

{% include image.html url="/assets/light-cone.jpg" width="width:30%" description="Event P and its light cones" %}

When we think of gravity, we usually think of it as the pull of one
object on another.  The sun pulls on the Earth (and vice versa), etc.
From introductory physics classes, we know there is another way of
thinking of it.  Rather than saying that the sun pulls on the Earth,
we can say that the sun creates a gravitational field, and the
gravitational field at our location is what pulls on the Earth.  For
weak-gravity, slow-moving systems like the solar system, this
complication may seem unimportant, even pedantic.  The sun makes a
radial field pulling everything toward it; why not just say the sun
pulls everything toward it?

Well, if there is fast motion or strong gravity, the difference
becomes very interesting.  Does the sun’s gravitational field at
Earth’s location point toward where the sun is right now?   From what
we said above, one can’t really say what event on the sun’s path
through spacetime corresponds to “right now” on Earth.  If nobody’s
moving relativistically, we can define an approximate global Lorentz
frame to give “right now” a meaning (although one that the laws of
physics don’t care about).  Even so, if no signal can travel faster
than light, the field here can at best be affected by where the sun
was a light-travel time (8 minutes) ago.  We are pulled not toward
where the sun is, but toward where it was.

### Gravitational waves

o far, there’s nothing special about gravity.  You remember that
electromagnetic fields also depend on charges and currents at retarded
times.  You’ll also remember that if the charges and currents are
accelerating, electromagnetic waves are produced.  These waves are
much longer-ranged than static fields.  The electric field of a static
charge goes like $$1/r^2$$, but that of a radially outgoing EM wave falls
off like $$1/r$$.  (The energy flux, which goes like $$E\times B$$, falls
off like $$1/r^2$$.)  Once generated, EM waves require no further help from
charges and currents; they continue traveling through space forever.
In fact, there are perfectly good solutions of Maxwell’s equations
with nothing but EM waves (no charges or currents anywhere at any
time).  With Maxwell’s completion of the theory of electromagnetism
and discovery of EM waves, the electromagnetic field could be seen to
have a dynamics, a “life”, all of its own.  In any causal theory of
gravity, including general relativity, gravity will likewise take on a
life of its own, and there will be gravitational waves which will fall
off like $$1/r$$ and be detectable much further away than we could ever
hope to feel the source’s gravitational pull.

Electric charges and currents act as sources for electromagnetic
fields.  Mass and mass currents acts as sources for spacetime
curvature.  Gravitational waves are vacuum (i.e. source-free)
solutions of Einstein’s field equations, just as electromagnetic waves
are vacuum (source-free) solutions of Maxwell’s equations.  Although
neither type of wave needs sources to continue in existence and
propagate, sources are important for generating these waves.   A
time-varying electric dipole generates an electromagnetic wave; a
time-varying mass quadrupole generates a gravitational wave.
Remember, this is what dipoles and quadrupoles look like:

{% include image.html url="/assets/quadrupole.jpg" width="width:30%" description="example dipole and quadrupole distributions" %}

More precisely--in the appropriate weak-gravity approximation--the
gravitational wave perturbation of the spacetime metric is

$$\frac{2}{r} \frac{d^2}{dt^2}
\int \rho(x_i x_j - \frac{1}{3}\delta_{ij}r^2) d^3x$$

The quadrupole shape looks kind of like two blobs of matter (in that
it has two peaks of the same sign), so you won’t be surprised that
binary systems make the best gravitational wave sources, with the
time-dependence supplied by the motion of the two objects orbiting
each other.

### Black holes

Strong gravity allows gravity to take on a life of its own in an even
more shocking and menacing way.  If gravity is really spacetime
curvature, then it can influence light cones and, in extreme cases,
tip them over, like this:

{% include image.html url="/assets/tipped-light-cones.jpg" width="width:40%" description="tipped light cones, inspired by a Schwarzschild black hole in ingoing Eddington-Finkelstein coordinates" %}

Of course, I’ve had to suppress two dimensions, so this is only
showing time and a radial variable; all of the light rays shown are
radial, traveling directly towards or away from the origin.
(Remember, on a spacetime diagram, the origin appears as the vertical
axis.)  All observers must travel within their light cones, and all
signals of any sort must travel in or on their light cones, so you can
see that it’s impossible for any sort of signal to leave the region to
the left of the purple dotted line.  Things and information can go in, but
they can’t go out.  The dotted line is an event horizon, and inside of
it is a black hole.

Our Newtonian intuition is that when things fall into a black hole,
the black hole is pulling them in, but that can’t be right at all.
There can be no communication of any kind from the black hole to the
outside—for that to happen, a signal would have to break out of its
own light cone.  The interior of the black hole is inaccessible in
exactly the same way as the future is inaccessible to the past.  Using
light cones to define “past” and “future”—as one should—we see that no
event inside the black hole is in the past of any event outside.  The
matter that collapsed to form the black hole might have vanished
without a trace, and we outside observers could be none the wiser.

So what pulls an object toward the black hole?  It can only be the
gravitational field—actually, the spacetime curvature—at the location
of the object.  And what makes the spacetime have that curvature at
the object’s location?  Once again, it can’t be anything inside the
black hole.  In fact, no matter needs to be involved at all.  The
spacetime curvature of a black hole can maintain itself.  It’s the
most dramatic case one could imagine of spacetime curvature driven
by its own dynamics.

*But what if I just look at a black hole.  Won't I see something?*

Remember, what you see when you look in a particular direction isn't
necessarily what is *there* in that direction, just what light is hitting
your eye coming from that direction.  Given some light sources near a
black hole, one can trace the paths of light rays through the curved spacetime
to determine what an observer at some location would see.  Often there is a "shadow" range of directions in which a close observer would see black.  This means that no light is coming to your eyes from these directions.

*What if I stick my hand inside the horizon to feel what's going on inside?*

This is not recommended.  To stay in one piece, the rest of you will
be crossing inside soon afterward.  On the bright side, your hand that
crosses the horizon first won't go numb--by the time nerve signals
from your hand reach your head, your head will be inside the horizon.
As a matter of fact, you won't even know when you've crossed the
horizon.  It's empty space and locally won't seem in any way special.
From the perspective of an observer right at the horizon, the horizon
is moving outward at the speed of light, and the observer would need
to move at the speed of light just to keep up.  (This can be seen by
looking at the light cones above.)


### What equations go into a numerical relativity simulation  

Let’s take a sample system:  the merger of a black hole with a neutron
star.  This problem has a lot of ingredients.  There is a fluid star.
There is a black hole.  As the two move, they give off gravitational
waves.

First, consider how one would simulate this system on a computer using
Newtonian physics.  The neutron star is a fluid, so at each point it
can be described by its density $$\rho$$, internal energy density $$U$$,
and velocity $$\vec{v}$$.  These obey the equations of hydrodynamics:

$$ \frac{\partial\rho}{\partial t} + \nabla\cdot(\rho v) = 0 $$

$$ \frac{\partial}{\partial t}(\rho v^i)
+ \frac{\partial}{\partial x^j}(\rho v^i v^j + P\delta^{ij}) = \rho g^i $$

$$ \frac{\partial}{\partial t}\left(\frac{1}{2}\rho v^2 + U\right)
+ \nabla\cdot\left[\left(\frac{1}{2}\rho v^2 + U + P\right)\right]
 = \rho g\cdot v $$

where $$P$$ is the pressure and
$$\vec{g}=-\vec{\nabla}\phi$$ is the gravitational acceleration.  These
equations are just the laws of conservation of mass, momentum, and
energy, respectively.  The first, for example, just says, in the
language of a partial differential equation, that the mass in a region
only changes because of the flux of mass in and out through the
region’s boundary.  To complete the description of the fluid, one
must specify an *equation of state*, a rule for computing the pressure,
e.g. a function $$P=P(\rho,U)$$.

In a Newtonian simulation, the black hole is a point mass.  It has mass
$$M_{\rm BH}$$ and position $$\vec{x}_{\rm BH}$$.  If we like, we can
set by hand a "horizon radius" and arrange that any fluid matter
inside this distance from the point mass is removed from the
simulation, with its mass and momentum incorporated into the point
mass.  The "black hole" will have its own equation of motion $$M_{\rm
BH} \ddot {\vec{x}}_{\rm BH} = \ldots$$ which makes the point mass's
momentum change because of forces from the fluid and momentum of
matter that has "fallen in".

The gravitational potential will come from the black hole and the
neutron star:

$$\nabla^2\phi = 4 \pi G [\rho + M_{\rm BH} \delta(\vec{x}-\vec{x}_{\rm BH})]$$.

Gravitational waves don’t exist
in Newtonian physics, but one can do an integral to get the quadrupole
moment, measure its time-dependence, and estimate the gravitational
wave signal from that.

Having thought through the Newtonian way, you are now ready to
appreciate how different things are in general relativity.  First,
we’ll consider the evolution of the neutron star fluid.  That actually
isn’t much different.  One still evolves the same conservation laws of
mass, momentum, and energy.  They look almost like their Newtonian
equivalents, and the differences aren’t interesting.  The big
difference is in the other stuff.

In Newtonian physics, gravity is a force caused by the field $$\phi$$.  In
GR, there is no gravitational force; there is only curvature in the
geometry.  The equivalent of $$\phi$$ is the spacetime metric tensor **g**.
Recall that the metric tensor tells you how to measure the proper
distance between nearby points.  In Newtonian physics, with the usual
Cartesian coordinates, this is just the Pythagorean theorem:

$$\Delta s^2 = \Delta x^2 + \Delta y^2 + \Delta z^2$$

In special relativity, time and space intervals depend on the observing
frame ("time dilation", "length contraction"), but there is a combination
which is an invariant separation between events:

$$\Delta s^2 = -c^2\Delta t^2 + \Delta x^2 + \Delta y^2 + \Delta z^2$$

In the presence of curvilinear coordinates ($$x^0$$,$$x^1$$,
$$x^2$$,$$x^3$$)--Note that there are four of them because spacetime is
4D--and/or curvature, the equation will be more general.  It
will still depend on quadratic combinations of the coordinate intervals
$$\Delta x^a$$, but there may be a coefficient in front of each term, and
each coefficient can be a function of space and time.

$$\Delta s^2 = g_{ab}\Delta x^a\Delta x^b
= g_{00}\Delta x^0\Delta x^0 + g_{01}\Delta x^0\Delta x^1 + \ldots
+ g_{22}\Delta x^2\Delta x^2$$

The metric components $$g_{ab}$$ contain all the information about the
spacetime.  In particular, they provide the light cones, which are the
*null paths* for which $$\Delta s^2 = 0$$. They have their own equations
of motion, which are partial
differential equations and are in fact fairly similar to wave equations

$$ \left(\frac{\partial^2}{\partial t^2} - \nabla^2\right) g_{ab}
\sim 16\pi T_{ab} $$

$$T_{ab}$$, the stress-energy tensor, contains information about the
mass, energy, and momentum, which serve as sources of the spacetime
curvature.   I put the $$\sim$$ sign because the above isn't exactly
right.  The full Einstein field equations are a bit more complicated;
they have nonlinear terms which made it difficult to figure out how to
evolve them stably.  Those problems are solved now, though, so we
needn’t bother about the nonlinear terms; they must be added, but they
don’t change the general picture of what goes into these simulations.

We still have to add the black hole and the gravitational waves,
right?  Nope.  We’re done.  All of that is contained in the metric
tensor.  Black holes and gravitational waves are just aspects of
spacetime curvature.  Just setting $$g_{ab}$$ appropriately makes
there be a black hole; just evolving $$g_{ab}$$ according to its field
equations makes the black hole move and grow appropriately.  Waves of
$$g_{ab}$$ propagating out to the outer boundaries just are
gravitational waves.

That’s what goes into a numerical relativity simulation.


## Thick disks and hypermassive stars  

### Neutron stars and their binaries  

Nearly all the NR work at WSU involves neutron stars in one way or
another.  Neutron stars are fascinating objects, made of the densest
known form of matter in the universe.  You know that in ordinary
matter, nearly all of the mass is concentrated in the atomic nuclei,
which take up a very small fraction of volume.  For an atom, the
nucleus takes up $$\sim 10^{-15}$$ of the volume.  The nuclei
themselves are incredibly dense, around $$10^{15}$$ g cm$${}^3$$.  The
interior of neutron stars is nuclear matter, meaning it is the density
of nuclei—no empty space in between.  One can imagine it as what would
happen if the atomic nuclei in atoms were to be brought so close
together that they touched and dissolved into a single gigantic
nucleus.  A typical neutron star has a mass a little more than that of
the sun and a radius of around a dozen kilometers (an oddly humanly
comprehensible scale for an astronomical object).  It’s a city-sized
atomic nucleus.

Besides their high compaction, the important thing to know about
neutron stars is that they are degenerate objects, meaning that the
pressure that holds them up against their own gravity is not thermal
pressure.  It is pressure that would be there even if the temperature
were absolute zero.  The sources of pressure in neutron star matter
are 1) nuclear forces, which can become repulsive if particles get too
close together, and 2) kinetic energy that particles are forced to
have just because of the Pauli Exclusion Principle even in the absence
of thermal energy.  Because the effect of nonzero temperature is
usually so small, neutron stars can usually be treated as “cold”
objects, even when their temperature is billions of degrees.

Two neutron stars caught in each other’s gravity will also form a
binary system, will also emit gravitational waves that slowly extract
orbital energy, will thus slowly spiral toward each other and
eventually merge.  When two neutron stars merge, one would expect the
result to be a more massive neutron star—after all, the nuclear
density matter from the two neutron stars goes into this post-merger
blob, and what else would one call something made out of that stuff?
The issue with this is that there is a maximum mass a cold,
nonspinning neutron star can have.  Above this mass, there is no
equilibrium configuration (stable or otherwise).  The exact value of
the maximum mass is not known, but adding two typical neutron star
masses will often put one above this maximum for reasonable guesses of
its value.  So, if the merger remnant were cold and nonspinning, it
could not persist for long.


### Supramassive and hypermassive stars  

### Dynamical vs secular evolution  

### Categories of astrophysical equilibria  

## Turbulence and the great paradoxes of fluid dynamics  

### The difficulty of falling into a black hole  

### Peculiarities of almost perfect fluids  

### Subgrid turbulence modeling

This is an equation:  $$y = x^2$$
