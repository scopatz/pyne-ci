pyne-ci
=======

Continuous Integration scripts for PyNE core using Batlab

Post PR nightlies restart process
=================================

 - login to batlab with info google drive doc
 - enter the following commands
 ```sh
 cd pyne-ci
 git pull origin master
 ```
 - Determine the current recurring run # using
 ```sh
 nmi_list_recurring_runs
 ```
 - Then remove the associate Recurrence ID ex:
 ```sh
 nmi_rm 913202.0
 ```
 - Finally restart nightlies 
 ```sh
  nmi_submit pyne.nightly.run-spec 
 ```
