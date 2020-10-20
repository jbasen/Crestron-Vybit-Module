# Crestron-Vybit-Module
Licensing

The Prowl notifications module, PushOver notifications module, and 
Vybit notifications module all provide the ability for a Crestron 
program to send push notifications to a homeowner's smart phone 
and/or tablet.   With these modules you can, for example:

1.	Send a notification to a smart phone when the burglar alarm is tripped.  
2.	Send a notification to a smart phone when the temperature in the 
    house gets too cold and there is risk of a pipe freezing.

There are minor differences in functionality between the three modules 
that may make one a better fit for a specific client than the others.

The modules are all written in Simpl# and each has an example program 
demonstrating its use as well as detailed help files.

This family of modules is released as shareware.  As a developer the modules 
are free for use on your own personal Crestron system.  Dealers are also 
invited to use them in their showrooms.  However, if you decide to use any, 
or all of them, on customer systems where you, or the dealer/csp you work for
will profit from them than I ask for a single payment of $100.  

What you get is 

1) My thanks
2) Permission to use Prowl module, PushOver module, and Vybit module on as 
   many client projects as you want
3) A copy of the Simpl# source code for each module (only a binary executable 
   is included with each example program)
4) Good Karma

You can contact me at jay.m.basen@gmail.com to arrange for payment.

Thanks

Jay Basen

_________________________________________________________


This module works with Vybit pushes notifications with a unique sound 
that allows you to identify the notification without having to to your 
smart phone or tablet.  

This module consists of the core S# module Vybit.clz and a Simpl+ wrapper 
Vybit v1.0.usp/Vybit v1.0.ush. The usp and ush files should be placed in 
your Crestron Usrsplus directory.  The INCLUDEPATH statement in the 
Vybit.usp file must be modified to point to the directory where you plan 
on placing the Vybit.clz file.  There have been problems reported when 
this file is simply placed in the Crestron Usrsplus directory.

An example program, Vybit Module Demo.smw is provided to further show how 
the module can be used.  

Inputs
    Init              - Pulse to initialize communications
    Send              - Pulse to send notification to Vybit app after the 
                        API_Trigger_Key$,
                      - Notification$, and Log$ string inputs have been set.
    API_Trigger_Key$  - Identifier from the Vybit trigger url in the app that 
                      - identifies a unique Vybit notification
    Notification$     - Text to be included with the notification or "" if no text
                      - is needed
    Log$              - Text to be included in the Vybit app log of notifications or ""
                      - if no text is needed

Outputs
    None
		
Paramteters
    Debug_Msg_Output - Where to Send Debug Messages - None, Console, Error Log, or Both
