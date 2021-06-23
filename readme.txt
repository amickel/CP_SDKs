Application Name
================
Description_interactive


Application Version
===================
0.1


NCOS Devices Supported
======================
ALL


External Requirements
=====================


Application Purpose
===================
This program allows the user interact with the local API by using the
description field as the input command and posting the output of the command
back into the description field. If a status command is passed the Cradlepoint
will re-run the command every 5 seconds until a new command is entered. Thanks
to @nathanwiens for the port status contribution, which will post unicode
symbols representing each port's status to the description field. Due to field
character length limitations only the first 256 characters of the result will
be put into the description.

 Example description field good input and expected output:
     input:
         .put('/config/system/gps/enabled', False)
     expected output:
         {'success': True, 'data': False}
 Example description field bad input and expected output:
     input:
         .put('/config/system/enabled', False)
     expected output:
         {'success': False, 'data': {'exception': 'key', 'key': 'enabled'}}


Expected Output
===============
Description updated

