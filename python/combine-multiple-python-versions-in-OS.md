TIL how to make multiple python installations in one OS without conflicts
-------------------------------------------------------------------------

The trick is to not add a static environment variable for a specific django versions, instead use virtualenv so it is confined for that specific versions, the side effects of putting something in your global environment is new installations of python may not work, i encountered this today, and the error is pointing to the environmental variable that points to a specific python installation. 
