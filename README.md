This is for documenting the lumerical tricks and learnings

Update the lumerical structure paremeter
There are three ways to update the lumerical structure
1. "Deleteall"; recreate structure for example "addrect" (in the for loop)
   pro: a. simple; b. for large modification of structure
   con: long codes, reading unfriendly; 
   example code:
   https://github.com/QingjunGoforit/lumerical/blob/aae78a64d8f27551279104ff2536f480d6f6f42c/fiber_modeling_qingjun/fiber_modeling_Qingjun.lsf
3. Set structure group, and set user properties, use "myscript" to create geometry with the user properties, later update the user properties
   pro: easy to share the parameter between different sturctures, once update the property, all the sturcture with the same property will be updated
   con: the "myscript" need to change quote mark to a reading-unfriendly way
   example code:
   https://github.com/QingjunGoforit/lumerical/blob/aae78a64d8f27551279104ff2536f480d6f6f42c/CWM%20tolerance%20analysis.lsf
4. call the existing structure use setnamed("structure_name", "property", value);
   pro and con: between method 1 and 2; reading friendly, need to select all the structures and update them one by one
   example code:
   https://github.com/QingjunGoforit/lumerical/blob/aae78a64d8f27551279104ff2536f480d6f6f42c/CWM%20tolerance%20analysis.lsf
