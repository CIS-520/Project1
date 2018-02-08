Originally, I thought that I had to make a new file called alarm-mega.ck that would be 
a copy of alarm-multiple.ck (with a 70 as an argument on one of the lines). 
I edited the other files that had references to alarm-multiple
and added references to alarm-mega. Yet, the project would always fail when I tried to make it. 
I went to Chandra's office hours for some help with this, and he suggested making a C file.
The C file was similar to the alarm-negative.c file, with a function that would loop 70 times, 
have a sleep_timer(1) command, and a print statement. This worked fine. But on further inspection, 
I realized that the alarm-wait file had a function for alarm-multiple, and that I could make a similar
function for alarm-mega. I still left the references to alarm-mega (and test_alarm_mega) in the other files that also had 
references to alarm-multiple. The files changed specifically with this added reference were tests.c, Make.tests. I originally
had also made this change to tests.h as well, since it includes a reference to alarm-multiple, but I suppose that this 
reference got lost in the transition from the C approach. Since my program ran without the reference in the tests.h, I am
assumming that this last reference isn't needed. 
