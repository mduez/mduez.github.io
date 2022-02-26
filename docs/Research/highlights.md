---
layout: page
title: Highlights of Research Results
exclude: true
permalink: /Highlights/
---

**Exploring black hole-neutron star parameter space**

Binary systems composed of one black hole and one neutron stars (hereafter
"black hole-neutron star" or "BHNS" binaries) are an important source
of gravitational waves, gamma ray bursts, and kilonovae.  However, there
is a lot of variety in BHNS binaries, in that black holes and neutron stars
come in a variety of masses and spins.  These binary parameters have a large
effect on the merger outcome.  For example, binaries with low black hole
mass or high black hole spin are more likely to leave post-merger disks
and outflows and thus to make electromagnetic signals.  
Much WSU SXS research a decade ago
was devoted to simulating types of BHNS systems which had previously been
too difficult to model in full general relativity--above all the cases
of [more massive](https://arxiv.org/abs/1111.1677) black holes and very
high black hole spin.  (In one [case](https://arxiv.org/abs/1302.6297),
the black hole spin was 97% of the Kerr limit.)

**Adding Microphysics to Black hole-neutron star simulations**

{% include image.html url="/assets/Images/bhns-disk.jpg" width="width:50%" description="A postmerger disk, 3D contours of neutrino luminosity, from Deaton et al ApJ 776, 47 (2013)" %}

Early numerical relativity simulations of BHNS binaries used simplified
equations of state, so that the neutron structure was not very realistic
and neutrino cooling (the dominant way heat is removed) was absent.  We
implemented nuclear theory-based equations of state in the SpEC code together
with an approximate neutrino cooling model.  My student Brett Deaton
[carried out](https://arxiv.org/abs/1304.3384) the first fully relativistic
BHNS simulation to include all of these microphysical effects, and soon
afterward [we used](https://arxiv.org/abs/1405.1121) his recipe to simulate
BHNS mergers with a whole range of black hole masses and spins.

{% include image.html url="/assets/Images/bhns-disruption.png" width="width:50%" description="A neutron star tidally disrupted by a black hole, equatorial temperature profile, from Brege et al PRD 98, 063009 (2018)" %}

Neutron star matter is too dense to be studied in the laboratory, so the
correct neutron star equation of state at the highest densities deep in the
core is unknown.  This is in fact one reason for scientific interest in these
binaries, because signals from mergers can carry information about unknown
nuclear physics.  Numerical relativity assists this process by modeling
systems with different assumed equations of state.  (Unlike the binary
parameters considered above, this is not something that really varies from
one BHNS system to another.  There is one neutron star equation of state;
we just don't know what it is.)  My student Wyatt Brege
[carried out](https://arxiv.org/abs/1804.09823)
simulations with a few different equations of state produced by nuclear
physicists and investigated the differences in merger outcomes.

Since these early simulations, my University of New Hampshire collaborator
Francois Foucart has
[implemented](https://arxiv.org/abs/2103.16588)
much more sophisticated and accurate
modeling of the neutrino fields and their effect on the hot nuclear matter.
We are in the process of using these methods to study BHNS and binary
neutron star mergers with a new level of physical realism.

Matter that escapes the BHNS merger undergoes nuclear reactions until it
settles on some distribution of stable nuclei.  With several outside
collaborators and their codes, we were able to track the movement of
the outgoing matter predicted by our simulations and [follow the nuclear
reactions](https://arxiv.org/abs/1601.07942) to learn what elements these
mergers create and release into surrounding space.

**Long-time post-merger evolutions**

{% include image.html url="/assets/Images/MagnetizedDisk.jpg" width="width:50%" description="A magnetized postmerger disk, from Nouri et al 97, 083014 (2018)" %}

After merger, the subsequent evolution is driven by neutrinos and magnetic
fields.  Magnetic fields trigger instabilities and turbulence in the disk,
which drives accretion into the center.  They can also be responsible for
polar jets--low-density relativistic outflows that may be associated with
gamma ray bursts.  Many simulations have studied the effects of magnetic
fields on black hole accretion disks, but most use simple initial conditions
that do not resemble post-merger states, and most neglect neutrino effects
and thus cannot capture the thermal evolution of the disk accurately.  My
student Fatemeh Nouri [carried out](https://arxiv.org/abs/1710.07423)
simulations of magnetized, neutrino-cooled disks using one of our merger
outcomes as initial data.  She used an interesting new analysis to study
the thermal balance between MHD-reconnection heating, neutrino cooling,
and advective cooling.

Like most 3D simulations, these did not evolve nearly far enough to see
what ultimately happens to the disk, and in particular how much and what
kind of outflows are ultimately produced.  To address these questions,
we have been working on 2D simulations, using the approximate axisymmetry
of the post-merger state to eliminate one (azimuthal) dimension.  While
3D simulations take months to go tens of milliseconds, 2D simulations allow
us to on similar timescales go ten seconds.  My student Jerred Jesse
[worked out](https://arxiv.org/abs/2005.01848) an interesting new method
to implement axisymmetry on
multipatch-type codes, and he demonstrated it in SpEC for hydrodynamics,
magnetohydrodynamics, and neutrino transport.  My student Milad Haddadi
has used these methods to carry out our first multisecond simulations
tracking the late-time evolution of BHNS post-merger disks and their
outflows.

On long timescales, the
angular momentum transport that drives accretion must be included.
Simulations that do not explicitly include magnetic fields often model
the missing turbulent transport as a viscosity.  We have
[studied](https://arxiv.org/abs/2008.05019) how to do this in general
relativistic simulations, comparing different possible methods, and
showing how to incorporate other (heat and particle) transport effects
as well.

