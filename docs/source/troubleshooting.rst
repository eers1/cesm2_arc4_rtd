Troubleshooting
===================================

If a run fails, the first place to check is in your run submission outputs, run.*.o* and run.*.e*, within ``$HOME/cesm_prep/<case_name>``. In particular, the .e file (for error output) may give some indication and it might point you to the cesm log files in ``/nobackup/<username>/cesm_sims/<case_name>/run/`` for more information. Additionally, in the same directory there are log files for each of the coupled models (atm, lnd, etc) where you can check for errors.

.. note::
   
   If you are using short term archiving (``DOUT_S=True``), these logs files will be located at ``/nobackup/<username>/cesm_sims/archive/<case_name>/logs/``. 


For more information on the job from the batch system, you can use ``qacct -j <job_id>`` at any time, or ``qstat -j <job_id>`` while the job is queueing or runnning. 
