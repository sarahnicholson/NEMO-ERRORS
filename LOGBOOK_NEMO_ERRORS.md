LOGBOOK - NEMO ERRORS 
==============================================
Time-stepping errors:
-----------------------------------------------------------------------------------------------

![title](file://localhost/Users/sarahnicholson/Dropbox/BYWORD_DOCUMENTS/timesteperror1.png)

>> **Solution:**  the time step needs to be divisible by the number of seconds in a day (86400), Example: I was using 3000 but  86400/3000=28.8 so I should be 3200 -> 86400/3200 = 27

![title](file://localhost/Users/sarahnicholson/Dropbox/BYWORD_DOCUMENTS/timesteperror2.png)

>> **Solution**: The time-step is to large, reduce the size.  Also: refer to: http://www.hector.ac.uk/cse/distributedcse/reports/nemo/nemo_notes/node46.html

Lateral diffusion errors:
-----------------------------------------------------------------------------------------

![title](file://localhost/Users/sarahnicholson/Dropbox/BYWORD_DOCUMENTS/latdiffuseerror.png)>>Attempted to activate GM (Gent McWilliams Paramterization for eddies) - define cpp keys ldfeiv and ldfslp set rn_aeiv_0=500.
>>**Solution:**  Change operator from Bilaplacian to laplacian and diffusion from horizontal to iso-neutral.


