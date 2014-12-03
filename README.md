Documentation & notes for the LAR continuous SF6 detector
=========================================================

The inert gas SF6 is routinely used in atmospheric research, especially for
studies of tracer dispersion and pollutant dilution. [WSU LAR](http://lar.wsu.edu)
has several custom-built SF6 analyzers which are essentially gas chromatographs
(Hewlett-Packard Model 5890A) outfitted with electron-capture detectors (ECDs).
At the time of construction, no comprehensive user's manual was created and so
such documentation is being generated now, in this repo.


### Theory of Operation

The analyzer produces a signal in direct proportion to the concentration of SF6
present in a sample. By measuring the signal produced by blanks and known SF6
standards, the response of the analyzer[^1] can be determined. And with the 
analyzer response known, the concentration of SF6 in each sample can be derived
by simple linear scaling.

  [1]: the absolute response will vary over time, therefore it is important to
       re-analyze blanks and standards at regular intervals (perhaps as
       frequent as every dozen samples)

Samples (collected in syringes) are introduced into the analyzer inlet stream
via a gas chromatograph (GC) injection valve manifold. A small pump pushes
ambient air into the injection manifold, past the inlet to the catalytic chamber
and back to ambient atmosphere. A second small pump draws sample into the
catalytic chamber, through the counter-flow dryer, through the ECD reactor, and
finally exhausts to ambient atmosphere. 

As sample is drawn into the catalytic chamber, an excess of hydrogen (H2) also
flows in and reacts completely with atmospheric oxygen to form water vapor. As
the moist stream passes through the counter-flow dryer, water vapor passes
through the nafion tubing to be carried away by a pure nitrogen (N2) stream. A
dry, oxygen-free gas stream then enters the reactor where an electron-capture 
detector (ECD) reports a signal in proportion to the remaining SF6.[^2]

  [2]: the ECD is almost certainly responding to other gases in the sample but
       since highly-reactive gases (i.e. oxygen) have been removed, it's 
       responsable to attribute all response to SF6


### Setup

Since each analyzer is custom-built, the exact physical configuration of valves,
switches, etc is device-dependent. Be particularly careful when referring to 
buttons on the analyzer front control panel since the different zone heaters 
may be associatd with different buttons on individual devices.


1. Connect gas supply lines:
    a. nitrogen
    b. hydrogen
2. Setup loop injection & pump, if not already
3. For use with integrator (recommended):
    a. connect instrument network cables (both)
    b. power on integrator
4. For analog voltage output:
    a. plug cable into 'signal 1' slot
    b. connect signal wires: signal/blue (+), reference/green (-)



### Operation

* The dryer and ECD heaters must reach temperature before operation can begin
  so turn on the analyzer several hours before intended use.
    * Even afer reaching temp, analyzer will complain "Not ready" because oven
      temp is out-of-range; this is fine, operation can begin despite the 
      warning since oven temp is not regulated






