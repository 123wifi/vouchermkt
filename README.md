# vouchermkt
Standalone application to create and manage vouchers for mikrotik user-manager  


I'm just finishing the standalone application to create Hotspot users.
I've developed it with Livecode (revolution), 'cause the learning curve is good 
and offers several advantages:

*Community edition freely usable (a paid version also exists if you need it)
*With only one source code it can generate binaries for:

Windows
Linux (x86,x86_64, ARM)
OSX
Android
iOS

*Graphical interface ( buttons, text fields, grids, windows...)
*High level language, near to english natural speaking
*Ability to use external functions througth .dll, .libs...


What does actually do ?

The application can connect to a mikrotik router with ssh and create and ask for hotspot users througth 
user-manager. All user management is done with the hotspot/user-manager logic. 
This application intends to be a very simple DGI ("Dumb Graphical Interface", yes! I've invented it!) 
to be used by non technical staff, only needing to push a button to create a voucher.

The application is protected by initial login/password, validated against an internal
user created in the mikrotik. The ssh commands are executed using the login/password initial credentials.

The application creates random user/password (vouchers) -only numeric chars by now-, 
verifies that the random user doesn't exists yet (to avoid conflicts) and creates 
the user inside mikrotik assigning the desired profile (the profiles must be created before).

Prints a voucher.

The application gives the ability to search the sessions activity of existing users.

The internal code is a shame (I've developed at same time I was learning the programming language).
The next developing effort will be focused in clean and optimization code.
