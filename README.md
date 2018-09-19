# pre-execute

This is a teraterm macro that executes the command described in preformatted text.  
Execute the procedure described by markdown (or textile) as it is.  
You can also get logs at the same time.  
This software is released under the MIT License, see LICENSE file.

# How to use

1. Please copy the following file and describe the settings such as prompt.  
auto-run.template.ttl  
~~~
(Omitted)
prompt="pi@raspberrypi:.*\$"
(Omitted)
include "core\pre-execute.ttl"
exit
~~~
In this example, the file copied is your-auto-run.ttl.

2. Select the your-auto-run.ttl in Teraterm.  
~~~
Teraterm
    -> Control
        -> Macro
            -> your-auto-run.ttl
~~~

3. Then you are prompted to select markdown or textile, please specify an arbitrary file.  
Samples are prepared in the scenario directory.

# Format to be executed
## Preformated text(backquote * 3)

~~~
```
command1
command2
command3
```
~~~

## Preformated text(textile)
~~~
<pre>
command1
command2
command3
</pre>
~~~

## Inline teraterm macro
~~~
<!--ttl
teraterm-command1
teraterm-command2
teraterm-command3
-->
~~~
The following can not be used.
~~~
<!--ttl teraterm command1(can not use) -->
~~~
