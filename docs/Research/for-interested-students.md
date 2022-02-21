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
    - [Binary neutron star mergers](#binary-neutron-star-mergers)
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


### What equations go into a numerical relativity simulation  

Let’s take a sample system:  the merger of a black hole with a neutron
star.  This problem has a lot of ingredients.  There is a fluid star.
There is a black hole.  As the two move, they give off gravitational
waves.

First, consider how one would simulate this system on a computer using
Newtonian physics.  The neutron star is a fluid, so at each point it
can be described by its density $$\rho$$, temperature $$T$$, and velocity
$$\vec{v}$$.  These obey the equations of hydrodynamics:

$$ \frac{\partial\rho}{\partial t} + \nabla\cdot(\rho v) = 0 $$

## Thick disks and hypermassive stars  

### Binary neutron star mergers  

### Supramassive and hypermassive stars  

### Dynamical vs secular evolution  

### Categories of astrophysical equilibria  

## Turbulence and the great paradoxes of fluid dynamics  

### The difficulty of falling into a black hole  

### Peculiarities of almost perfect fluids  

### Subgrid turbulence modeling

This is an equation:  $$y = x^2$$
