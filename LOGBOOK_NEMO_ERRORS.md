LOGBOOK - NEMO ERRORS 
=================================================================================================================
GENERAL (ie. NOT CONFIGURATION SPECIFIC)
========================================
Time-stepping errors:
------------------------------------------------------------------------------------------------------------------

![time_stepp_err](timesteperror1.png?raw=true)

**Solution:**  

    the time step needs to be divisible by the number of seconds in a day (86400), Example: I was using 3000 but  86400/3000=28.8 so I should be 3200 -> 86400/3200 = 27

![title](timesteperror2.png?raw=true)

**Solution:**

    The time-step is to large, reduce the size.  Also: refer to: http://www.hector.ac.uk/cse/distributedcse/reports/nemo/nemo_notes/node46.html


Lateral diffusion errors:
-------------------------------------------------------------------------------------------------------------------

![title](latdiffuseerror.png?raw=true)

Error because of incorrect activatation of GM (Gent McWilliams Paramterization for eddies) - defined cpp keys ldfeiv and ldfslp set rn_aeiv _0=500.

**Solution:**

    Change operator from Bilaplacian to laplacian and diffusion from horizontal to iso-neutral.

-----------------------------------------------------------------------------------------------------

-----------------------------------------------------------------------------------------------------
 JET CONFIGURATION:
========================
 
 **Northern Boundary Condition**
 
 At the dx=100km we had issues with reaching steady state temperature. The issue was at the  northern boundary restoring, because at this coarse resolution the sponge layer needed to be widen to include more points. 2800- 2600.
 
 ![title](NBrestoringerror.png?raw=true)
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

