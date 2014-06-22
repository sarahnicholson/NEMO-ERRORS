LOGBOOK - NEMO ERRORS 
=================================================================================================================


Time-stepping errors:
------------------------------------------------------------------------------------------------------------------

![time_stepp_err](timesteperror1.png?raw=true)

**Solution:**  

    the time step needs to be divisible by the number of seconds in a day (86400), Example: I was using 3000 but  86400/3000=28.8 so I should be 3200 -> 86400/3200 = 27

![title](file://localhost/Users/sarahnicholson/Dropbox/BYWORD_DOCUMENTS/timesteperror2.png)

**Solution:**

    The time-step is to large, reduce the size.  Also: refer to: http://www.hector.ac.uk/cse/distributedcse/reports/nemo/nemo_notes/node46.html


Lateral diffusion errors:
-------------------------------------------------------------------------------------------------------------------

![title](file://localhost/Users/sarahnicholson/Dropbox/BYWORD_DOCUMENTS/latdiffuseerror.png)

Error because of incorrect activatation of GM (Gent McWilliams Paramterization for eddies) - defined cpp keys ldfeiv and ldfslp set rn_aeiv _0=500.

**Solution:**

    Change operator from Bilaplacian to laplacian and diffusion from horizontal to iso-neutral.

-----------------------------------------------------------------------------------------------------