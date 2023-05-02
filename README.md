Download Link: https://assignmentchef.com/product/solved-cop4600-project-0-my-first-kernel-mod
<br>
You will add a kernel boot log message to Reptilian. You will then take a screenshot of the terminal displaying the added boot message with your name/UFID and a personal message visible and create a short video to demonstrate your code. You’ll submit the project via Canvas.

<h1>Structure</h1>

The project is broken into four main parts:




<ul>

 <li>Modify the kernel to print your name, UFID, and a personal message to the default boot (and rebuild).</li>

 <li>Take a screenshot displaying your name and UFID in the debug boot message</li>

 <li>Create a unified patch file</li>

</ul>




The system must print “<strong>##### FirstName LastName (UFID: 0000-0000) My Personal Message #####</strong>” using the log system with one new line above and below (while booting with the default configuration) just before the message “<strong>Detecting Reptilian system partition</strong>”. The personal message can be <u>appropriate</u> message you like (see example screenshots). It can be added in source near the call to the <strong>rcu_end_inkernel_boot()</strong> function, which wraps up the kernel’s boot tasks and hands off execution to the system initialization routines.




For extra credit (+4%), students may modify the GRUB menu to add “<strong>(FirstName LastName)</strong>” next to the default “<strong>Reptilian 20.08-A9.0-r2</strong>” option; see the <em>Example Screenshots</em> section below for an example of what the modified menu should look like. This will not be included in the patch; just take a screenshot and talk about what you did in the report and screencast. Note that <u>the GRUB utilities cannot be used</u> for this – just a text editor.

<h1>Log Levels</h1>

Many systems use level-based log systems. The Linux kernel has eight (8) levels that are used for log messages. Anything less severe than the KERN_ERR log level will only show up on the screen in verbose or debug mode.

<h1>Testing</h1>

You should test your code by starting your VM after rebuilding. Make sure it displays your message while booting in default mode (<strong><em>not</em></strong> verbose or debug). You should also apply your patch to a “clean” VM to make sure it works.