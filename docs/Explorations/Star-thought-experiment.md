---
layout: page
title:  A Thought Experiment on Stars
exclude: true
permalink: /StarThoughtExperiment/
usemathjax: true
---

In many of my astronomy classes, I talk about the scene in
*Star Trek: Generations* where the evil Doctor Soran shoots a
missile into a star which causes all fusion in the star to stop,
leading the star to immediately collapse.  I don't do this because
I'm a fanatical *Star Trek* fan.  As a Trekkie, I'd rather pretend
that *Star Trek: Generations* never happened.  It's because this
scene gets the astrophysics wrong in such a wonderfully instructive way.

What would actually happen to a star, say the sun, if all nuclear
reactions in it were to suddenly cease?  Let's take this in two passes,
one for everyone, and then another for the physics majors.  Even physics
majors should go through the first pass first.

**For everyone**

Introductory astronomy books sometimes say or imply that what keeps a
star like the sun at a constant size and brightness is a balance between
gravity and nuclear forces.  This isn't quite right.  In fact, there are
two different types of balance going on in the sun.

First, there is a balance of *forces*.  The sun is a ball of gas, and gas
likes to expand.  This is the force of pressure.  Each bit of gas has some
mass and so also pulls on each other bit of mass by the attractive force of
gravity, which overall tries to squeeze the star.  Each part of the sun is
in force equilibrium between gas pressure and gravity.

Second, there is the balance of heating and cooling, the *thermal* balance.
The sun's store of heat energy is depleted by radiation coming off the
surface.  It is replenished by nuclear fusion reactions in the core.  In
each part of the sun, heat generation and flow are balanced.

The connection between the two is that the pressure of a gas depends on its
temperature.  Now, though, you'll see what the issue is.  Even if nuclear
reactions stop inside a star, so that no more heat is being released by fusion,
the star's store of heat energy doesn't immediately disappear.  Energy is
conserved, so the thermal energy has to go somewhere, and the way stars get
rid of energy is by radiation.

Even my non-physics major readers should follow me on an estimate of how long
it would take for the sun to radiate away an appreciable amount of its store
of thermal energy.  How do we do this?  It's just like calculating how long
you can spend money before you exhaust your bank account:  take the current
balance and divide by how much you spend per day.  We need two numbers:  the
thermal energy content of the sun and the rate it is lost by radiation.  The
second number is easy:  it is, by definition, the luminosity of the sun:
$L_{\odot}=3.8\times 10^{26}$ Watts.

The second number, the energy in the
sun, requires a bit of work.  Here's one way that only involves a little bit
of physics, namely that the temperature $T$ of a gas gives the average energy
per particle $E$.  The rule is $E=\frac{3}{2}k_BT$, where $k_B=1.38\times 10^{-23}\,$J/K.  Temperatures deep in the sun are around $\sim 10^7\,$K.  We also
need the number of particles in the sun to go from energy per particle to total
energy.  Let's assume the sun is made entirely of ionized hydrogen, so almost
all of the mass is in protons.  To get the number of protons, take the mass of
the sun $M_{\odot}$ and divide by the mass of a proton $m_p$:
$N=M_{\odot}/m_p=2\times 10^{30}$kg/$1.7\times 10^{-27}$kg
$= 1.2\times 10^{57}$.  That's a big number, but in astronomy we're not afraid
of big numbers.  Actually, we should multiply by two because there are an
equal number of electrons, but I'm going to be throwing away numerical factors
like 3/2 or 2 pretty soon.  I get a total thermal energy
$Nk_BT\approx 10^{41}$J.

Dividing, I get the time to radiate a significant portion of the thermal
energy, the *Kelvin-Helmholtz timescale*,
$t_{\rm KH}=Nk_BT/L_{\odot}\approx 10^14$
seconds $\approx 10^7$ years (tens of millions of years).

So the star will slowly change over the course of millions of years.  It
will indeed shrink, but rather than cooling down, it will actually get
*hotter*.

**For physics majors**

To understand this, consider the timescale on which force balance is
maintained.  If pressure were to disappear, the star would collapse on a
free-fall timescale:  $t_{\rm ff}=(GM/R^3)^{-1/2}$, which is of order
an hour.  So
the star can respond very quickly, compared to $t_{\rm KH}$, to any changes
in the star's heat content.  It will adjust its size nearly instantaneously
(compared to $t_{\rm KH}$) to maintain force balance.  (Furthermore, we might
expect that, if pushed a little bit away from equilibrium, it will oscillate
*adiabatically* on timescale $t_{\rm ff}$.)  This equilibrium is expressed
via the virial theorem as an equality (up to factors of order unity) between
internal energy and gravitational potential energy.  Let us make order
of magnitude guesses for the average internal energy per proton and the
average gravitational potential energy per proton and then equate them.  Let's
be general and say the star has mass $M$ and radius $R$ which are not
necessarily the same as the sun's and will change with time as the star
loses energy by radiation.  To order of magnitude, an average proton will
be at distance $R$ from the center with interior mass of order $M$.

$$ \frac{GMm_p}{R} = k_B T $$

As the star shrinks, the temperature must go *up*.  This makes sense because
the star is always in hydrostatic (force balance) equilibrium.  As the
star shrinks, gravity becomes stronger, so the pressure must also be growing
to balance it.

Let's make a model of what will happen to the star as it shrinks.  We will
continue to assume that the star is pure hydrogen.  We will also assume
that thermal energy travels through the star by radiative diffusion, i.e.
by photons random walking their way through the hot interior until they
find their way to the surface.  This will make for a nice simple model.

What's the time it takes for a photon to random walk its way out of a star
from the deep interior?  In a very hot, dense, ionized gas, opacity is
dominated by electron scattering, which has Thomson cross section
$\sigma_T=6.7\times 10^{-29}\,{\rm m}^{-2}$.  The distance photons travel
between scatters is the mean free path $\ell = (n\sigma_T)^{-1}$, where
$n$ is the number of density, i.e. electrons per volume.  Using the fact
that there is one electron per proton, we can estimate
$n\sim N/V\sim M/(m_pR^3)$.  (I've taken the volume of the star to be
$V\approx R^3$.  Given all the approximations we'll be making, it wouldn't
make sense to keep track of factors of $\pi$ and whatnot.)

Hopefully you've studied random walks in at least one of your classes,
because you'll encounter it in many contexts.  If a photon takes steps
of size $\ell$ in random directions, the number of steps it takes to
travel a distance $R$ is on average $(R/\ell)^2$.  The time per step is
just the time it takes light to travel a distane $\ell$, that time being
$\ell/c$ naturally.  Thus, the total escape time, the ``diffusion time'',
is

$$ t_{\rm diff} \sim \frac{R^2}{\ell c} $$

That's how long it takes photons to stumble their way out of the star.  How
much energy do they take with them?  Well, what we have is a gas of trapped
photons, so they obey blackbody formulae.  In particular, the radiation energy
density is $a T^4$, where $T$ is some average interior temperature.  Note that
$T$ will probably change as the star shrinks.  Note also that $T$ will probably
be orders of magnitude higher than the temperature of the ``surface'' (more
precisely from the photosphere from which radiation escapes) $T_{\rm surf}$.
Thus, even though we're being sloppy, we can't equate $T$ and $T_{\rm surf}$.
Now, to go from an energy density to an energy, we must multiply by a volume,
the volume of the star, which is roughly $R^3$.  So we have radiation energy

$$ E_{\rm rad} \sim a T^4 R^3 $$

The energy released per time is the luminosity $L$:

$$ L \sim \frac{E_{\rm rad}}{t_{\rm diff}} \sim \frac{a T^4 R^4 c m_p}{M\sigma_T} $$

Now plug in the virial theorem equilibrium condition for $T$:

$$ L \sim \frac{a G^4 m_p^5 c}{\sigma_T k_B^4}M^3 $$

Ignore the mess of constants.  The main point is that luminosity depends
on $M^3$, which (assuming the star doesn't blow off much matter) is a
constant, and it doesn't depend on radius.  Thus, as the star shrinks,
its luminosity stays constant.

(How do we know the star shrinks rather than expands?  It's probably
intuitive that this is what will happen, but if you want an argument,
you can use energy conservation.  As the star radiates, its total energy
must go down, so it must sink into its gravitational potential well.)

The photons escape when they reach the surface (i.e. the photosphere).  This
is the radiation of trapped photons leaking off the surface of a dense,
opaque gas, so it will obey the Stefan-Boltzmann law for blackbody emission.
The flux (luminosity per surface area) is $F=\sigma T_{\rm surf}^4$.  The
flux and the luminosity are related by $L=FA$ where $A\sim R^2$ is the surface
area.  We already know what $L$ is--it's dictated by the interior physics.
For a given radius $R$, we can solve for $T_{\rm surf}$:

$$ T_{\rm surf} \sim \frac{L}{R^2} \propto R^{-2} $$

The surface heats up as the star shrinks, and (using Wein's law) the
star becomes bluer.  On a Hertzprung-Russell diagram (addressing myself
now to the astronomy majors), the star would move horizontally to the left.

Come to think of it, something like this might be expected to happen in
real life when stars are forming, before their interiors become hot enough
for pp-chain nuclear fusion. Sure enough, this horizontal H-R track in
pre-main sequence stars sufficiently massive to be radiative is
called the Hayney track.  (If energy transport is by convection, the star
follows a vertical path on the H-R diagram called the Hayashi track.)  So
something like this happens in real life outside of science fiction.  It
is stopped precisely by the initiation of nuclear fusion and establishment
of thermal equilibrium.

