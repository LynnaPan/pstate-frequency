# pstate-frequency

For a long time, there was only one main CPU frequency scaling driver for Linux  
called acpi-cpufreq. The code was old and many people felt like the commonly used  
ondemand governor was not cutting it with modern hardware. Intel stepped up to  
create a new CPU driver called intel_pstate which promised more robust control  
over CPU P-States and better dynamic scaling.

And when it was introduced there were no programs built to really take advantage  
of its new interface (currently housed in /sys/devices/system/cpu/intel_pstate).  
cpupower existed for earlier acpi-cpufreq machines, but no program existed to  
make it convenient to use intel_pstate.

So I built one.  
Kind of.

pstate-frequency is a simple program. Its job is to allow users to conveniently  
and quickly read and change the values used by the intel_pstate driver. It allows  
users to set maximum and minimum frequency ranges, and control the likelyhood of  
the CPU to enter Turbo Boost frequencies.

It's not perfect.

Due to bugs in the new intel_pstate driver, frequency ranges may not always be  
respected. The driver may not idle at the proper frequencies all the time.  
Various bugs can occur.

And that's okay.

pstate-frequency works to deliver convenience, it helps the user configure the 
intel_pstate driver to run as they would like it to. It is a simple program.  
It has a simple task and a simple goal.  Written in simple shell script, it depends only on the  
GNU coreutils and the users ability to read and comprehend the various options  
available.

Follow pyamsoft around the Web for updates and announcements about the  
newest applications!

Like what I do?

Send me an email at: pyam.soft@gmail.com  
Or find me online at: http://pyamsoft.blogspot.com/