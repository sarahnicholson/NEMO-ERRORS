PISCES ERRORS

================================================


General PISCES errors:
-----------------------------------------------------------------------------------------------

**Initialization errors:**

>>The error below was fixed by saying false for initializing using data file. We use analytical and so no path is provide for the data file – fix in pisces namelist.
 
 ![title](PISCESinitalizationwrongunits.png?raw=true)
 
>>ie:  ln_ndepo    =  .false.   ! boolean for atmospheric deposition of N .
**Choose false for all options like this.

**Frequency:**  

>>I was having error in output of grid_T frequency. 
 _Solution:_ In namelist n,n_fsbc    = 5 change to 1.


JET configuration: 
-----------------------------------------------------------------------------------------------------
The following errors are specific to the JET Configuration. 

**Analytical forcing error - units:**

>> Make sure you are using the correct units! Must be carbon moles.


**Iron  issues**  

>>Our dissolved iron was being depleted significantly at depth even when transport was turned off. 
> Sovled by inclusion of NB restoring for iron
>More information on restoring of iron, turning off all sources of iron in pisces - please contact author.

 
**Carbon cycle issue - output was empty**
 This was a bottom boundary condition problem - routine p4zsed.F90. A division by zero ; I've added an epsilon value to avoid this.


**CHL banded in pattern**
The bug was because of gphit - we use kilometres for the jet configuration.
But in the p4zprod.F90 you require gphit to compute the day length which you require latitude in degrees. Also again in p4zrem.F90
![title](latdegreestokilometerpisces.png?raw=true)

