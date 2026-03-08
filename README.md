The Philosophy of System Administration

Although the specifics of being a system administrator may change from platform to platform, there are
underlying themes that do not. These themes make up the philosophy of system administration.
The themes are:
Automate everything
Document everything
Communicate as much as possible
Know your resources
Know your users
Know your business
Security cannot be an afterthought
Plan ahead
Expect the unexpected
The following sections explore each theme in more deta

1.1. Automate Everything
Most system administrators are outnumbered -- either by their users, their systems, or both. In many
cases, automation is the only way to keep up. In general, anything done more than once should be
examined as a possible candidate for automation.
Here are some commonly automated tasks:
Free disk space checking and reporting
Backups
System performance data collection
User account maintenance (creation, deletion, etc.)
Business-specific functions (pushing new data to a Web server, running monthly/quarterly/yearly reports,
etc.)
This list is by no means complete; the functions automated by system administrators are only limited by
an administrator's willingness to write the necessary scripts. In this case, being lazy (and making the
computer do more of the mundane work) is actually a good thing.
Automation also gives users the extra benefit of greater predictability and consistency of service.

1.2. Document Everything
If given the choice between installing a brand-new server and writing a procedural document on
performing system backups, the average system administrator would install the new server every time.
While this is not at all unusual, you must document what you do. Many system administrators put off
doing the necessary documentation for a variety of reasons:
"I will get around to it later."
Unfortunately, this is usually not true. Even if a system administrator is not kidding themselves, the nature
of the job is such that everyday tasks are usually too chaotic to "do it later." Even worse, the longer it is
put off, the more that is forgotten, leading to a much less detailed (and therefore, less useful) document.
"Why write it up? I will remember it."
Unless you are one of those rare individuals with a photographic memory, no, you will not remember it.
Or worse, you will remember only half of it, not realizing that you are missing the whole story. This leads
to wasted time either trying to relearn what you had forgotten or fixing what you had broken due to your
incomplete understanding of the situation.
"If I keep it in my head, they will not fire me -- I will have job security!"
While this may work for a while, invariably it leads to less -- not more -- job security. Think for a moment
about what may happen during an emergency. You may not be available; your documentation may save
the day by letting someone else resolve the problem in your absence. And never forget that emergencies

tend to be times when upper management pays close attention. In such cases, it is better to have your
documentation be part of the solution than it is for your absence to be part of the problem.
In addition, if you are part of a small but growing organization, eventually there will be a need for another
system administrator. How can this person learn to back you up if everything is in your head? Worst yet,
not documenting may make you so indispensable that you might not be able to advance your career. You
could end up working for the very person that was hired to assist you.
Hopefully you are now sold on the benefits of system documentation. That brings us to the next question:
What should you document? Here is a partial list:
Policies
Policies are written to formalize and clarify the relationship you have with your user community. They
make it clear to your users how their requests for resources and/or assistance are handled. The nature,
style, and method of disseminating policies to your a community varies from organization to organization.
Procedures
Procedures are any step-by-step sequence of actions that must be taken to accomplish a certain task.
Procedures to be documented can include backup procedures, user account management procedures,
problem reporting procedures, and so on. Like automation, if a procedure is followed more than once, it is
a good idea to document it.
Changes
A large part of a system administrator's career revolves around making changes -- configuring systems for
maximum performance, tweaking scripts, modifying configuration files, and so on. All of these changes
should be documented in some fashion. Otherwise, you could find yourself being completely confused
about a change you made several months earlier.
Some organizations use more complex methods for keeping track of changes, but in many cases a simple
revision history at the start of the file being changed is all that is necessary. At a minimum, each entry in
the revision history should contain:
The name or initials of the person making the change
The date the change was made
The reason the change was made
This results in concise, yet useful entries:
ECB, 12-June-2002 -- Updated entry for new Accounting printer (to support the replacement printer's
ability to print duplex)

1.3. Communicate as Much as Possible

When it comes to your users, you can never communicate too much. Be aware that small system
changes you might think are practically unnoticeable could very well completely confuse the
administrative assistant in Human Resources.
The method by which you communicate with your users can vary according to your organization.
Some organizations use email; others, an internal website. Still others may rely on Usenet news or
IRC. A sheet of paper tacked to a bulletin board in the breakroom may even suffice at some places.
In any case, use whatever method(s) that work well at your organization.
In general, it is best to follow this paraphrased approach used in writing newspaper stories:
Tell your users what you are going to do
Tell your users what you are doing
Tell your users what you have done
The following sections look at these steps in more depth.

1.3.1. Tell Your Users What You Are Going to Do

Make sure you give your users sufficient warning before you do anything. The actual amount of
warning necessary varies according to the type of change (upgrading an operating system demands
more lead time than changing the default color of the system login screen), as well as the nature of
your user community (more technically adept users may be able to handle changes more readily
than users with minimal technical skills.)

At a minimum, you should describe:
The nature of the change
When it will take place
Why it is happening
Approximately how long it should take
The impact (if any) that the users can expect due to the change
Contact information should they have any questions or concerns
Here is a hypothetical situation. The Finance department has been experiencing problems with
their database server being very slow at times. You are going to bring the server down, upgrade the
CPU module to a faster model, and reboot. Once this is done, you will move the database itself to
faster, RAID-based storage. Here is one possible announcement for this situation:
System Downtime Scheduled for Friday Night
Starting this Friday at 6pm (midnight for our associates in Berlin), all financial applications will
be unavailable for a period of approximately four hours.
During this time, changes to both the hardware and software on the Finance database server will
be performed. These changes should greatly reduce the time required to run the Accounts Payable
and Accounts Receivable applications, and the weekly Balance Sheet report.
Other than the change in runtime, most people should notice no other change. However, those of
you that have written your own SQL queries should be aware that the layout of some indices will
change. This is documented on the company intranet website, on the Finance page.
Should you have any questions, comments, or concerns, please contact System Administration at
extension 4321.
A few points are worth noting:
Effectively communicate the start and duration of any downtime that might be involved in the
change.
Make sure you give the time of the change in such a way that it is useful to all users, no matter
where they may be located.
Use terms that your users understand. The people impacted by this work do not care that the new
CPU module is a 2GHz unit with twice as much L2 cache, or that the database is being placed on a
RAID 5 logical volume

1.3.2. Tell Your Users What You Are Doing

This step is primarily a last-minute warning of the impending change; as such, it should be a brief repeat
of the first message, though with the impending nature of the change made more apparent ("The system
upgrade will take place TONIGHT."). This is also a good place to publicly answer any questions you may
have received as a result of the first message.
Continuing our hypothetical example, here is one possible last-minute warning:
System Downtime Scheduled for Tonight
Reminder: The system downtime announced this past Monday will take place as scheduled tonight at 6pm
(midnight for the Berlin office). You can find the original announcement on the company intranet website,
on the System Administration page.
Several people have asked whether they should stop working early tonight to make sure their work is
backed up prior to the downtime. This will not be necessary, as the work being done tonight will not
impact any work done on your personal workstations.
Remember, those of you that have written your own SQL queries should be aware that the layout of some
indices will change. This is documented on the company intranet website, on the Finance page.
Your users have been alerted; now you are ready to actually do the work.
1.3.3. Tell Your Users What You Have Done
After you have finished making the changes, you must tell your users what you have done. Again, this
should be a summary of the previous messages (invariably someone will not have read them.)[1]
However, there is one important addition you must make. It is vital that you give your users the current
status. Did the upgrade not go as smoothly as planned? Was the new storage server only able to serve the
systems in Engineering, and not in Finance? These types of issues must be addressed here.

Of course, if the current status differs from what you communicated previously, you should make this
point clear and describe what will be done (if anything) to arrive at the final solution.
In our hypothetical situation, the downtime had some problems. The new CPU module did not work; a
call to the system's manufacturer revealed that a special version of the module is required for in-the-field
upgrades. On the plus side, the migration of the database to the RAID volume went well (even though it
took a bit longer than planned due to the problems with the CPU module.
Here is one possible announcement:
System Downtime Complete
The system downtime scheduled for Friday night (refer to the System Administration page on the
company intranet website) has been completed. Unfortunately, hardware issues prevented one of the tasks
from being completed. Due to this, the remaining tasks took longer than the originally-scheduled four
hours. Instead, all systems were back in production by midnight (6am Saturday for the Berlin office).
Because of the remaining hardware issues, performance of the AP, AR, and the Balance Sheet report will
be slightly improved, but not to the extent originally planned. A second downtime will be announced and
scheduled as soon as the issues that prevented completion of the task have been resolved.
Please note that the downtime did change some database indices; people that have written their own SQL
queries should consult the Finance page on the company intranet website.
Please contact System Administration at extension 4321 with any questions.
With this kind of information, your users will have sufficient background knowledge to continue their
work, and to understand how the changes impact them.

1.4. Know Your Resources

System administration is mostly a matter of balancing available resources against the people and
programs that use those resources. Therefore, your career as a system administrator will be a short and
stress-filled one unless you fully understand the resources you have at your disposal.
Some of the resources are ones that seem pretty obvious:
System resources, such as available processing power, memory, and disk space
Network bandwidth
Available money in the IT budget
But some may not be so obvious:
The services of operations personnel, other system administrators, or even an administrative assistant
Time (often of critical importance when the time involves things such as the amount of time during which
system backups may take place)
Knowledge (whether it is stored in books, system documentation, or the brain of a person that has worked
at the company for the past twenty years)
It is important to note is that it is highly valuable to take a complete inventory of those resources available
to you and to keep it current -- a lack of "situational awareness" when it comes to available resources can
often be worse than no awareness at all.
1.5. Know Your Users
Although some people bristle at the term "users" (perhaps due to some system administrators' use of the
term in a derogatory manner), it is used here with no such connotation implied. Users are those people
that use the systems and resources for which you are responsible -- no more, and no less. As such, they are
central to your ability to successfully administer your systems; without understanding your users, how can
you understand the system resources they require?
For example, consider a bank teller. A bank teller uses a strictly-defined set of applications and requires
little in the way of system resources. A software engineer, on the other hand, may use many different
applications and always welcomes more system resources (for faster build times). Two entirely different
users with two entirely different needs.
Make sure you learn as much about your users as you can.
1.6. Know Your Business
Whether you work for a large, multinational corporation or a small community college, you must still
understand the nature of the business environment in which you work. This can be boiled down to one
question:

What is the purpose of the systems you administer?

The key point here is to understand your systems' purpose in a more global sense:
Applications that must be run within certain time frames, such as at the end of a month, quarter, or year
The times during which system maintenance may be done
New technologies that could be used to resolve long-standing business problems
By taking into account your organization's business, you will find that your day-to-day decisions will be
better for your users, and for you.

1.7. Security Cannot be an Afterthought

No matter what you might think about the environment in which your systems are running, you cannot
take security for granted. Even standalone systems not connected to the Internet may be at risk (although
obviously the risks will be different from a system that has connections to the outside world).
Therefore, it is extremely important to consider the security implications of everything you do. The
following list illustrates the different kinds of issues you should consider:
The nature of possible threats to each of the systems under your care
The location, type, and value of the data on those systems
The type and frequency of authorized access to the systems
While you are thinking about security, do not make the mistake of assuming that possible intruders will
only attack your systems from outside of your company. Many times the perpetrator is someone within the
company. So the next time you walk around the office, look at the people around you and ask yourself this
question:
What would happen if that person were to attempt to subvert our security?

1.7.1. The Risks of Social Engineering

While most system administrators' first reactions when they think about security is to concentrate on the
technological aspects, it is important to maintain perspective. Quite often, security breaches do not have
their origins in technology, but in human nature.
People interested in breaching security often use human nature to entirely bypass technological access
controls. This is known as social engineering. Here is an example:
The second shift operator receives an outside phone call. The caller claims to be your organization's CFO
(the CFO's name and background information was obtained from your organization's website, on the
"Management Team" page).
The caller claims to be calling from some place halfway around the world (maybe this part of the story is
a complete fabrication, or perhaps your organization's website has a recent press release that makes
mention of the CFO attending a tradeshow).
The caller tells a tale of woe; his laptop was stolen at the airport, and he is with an important customer and
needs access to the corporate intranet to check on the customer's account status. Would the operator be so
kind as to give him the necessary access information?
Do you know what would your operator do? Unless your operator has guidance (in the form of policies
and procedures), you very likely do not know for sure.
Like traffic lights, the goal of policies and procedures is to provide unambiguous guidance as to what is
and is not appropriate behavior. However, just as with traffic lights, policies and procedures only work if
everyone follows them. And there is the crux of the problem -- it is unlikely that everyone will adhere to
your policies and procedures. In fact, depending on the nature of your organization, it is possible that you
do not even have sufficient authority to define policies, much less enforce them. What then?
Unfortunately, there are no easy answers. User education can help; do everything you can to help make
your user community aware of security and social engineering. Give lunchtime presentations about
security. Post pointers to security-related news articles on your organization's mailing lists. Make yourself
available as a sounding board for users' questions about things that do not seem quite right.
In short, get the message out to your users any way you can.

1.8. Plan Ahead

System administrators that took all this advice to heart and did their best to follow it would be fantastic
system administrators -- for a day. Eventually, the environment will change, and one day our fantastic
administrator would be caught flat-footed. The reason? Our fantastic administrator failed to plan ahead.
Certainly no one can predict the future with 100% accuracy. However, with a bit of awareness it is easy to
read the signs of many changes:
An offhand mention of a new project gearing up during that boring weekly staff meeting is a sure sign that
you will likely need to support new users in the near future
Talk of an impending acquisition means that you may end up being responsible for new (and possibly
incompatible) systems in one or more remote locations
Being able to read these signs (and to respond effectively to them) makes life easier for you and your
users.

1.9. Expect the Unexpected

While the phrase "expect the unexpected" is trite, it reflects an underlying truth that all system
administrators must understand:
There will be times when you are caught off-guard.
After becoming comfortable with this uncomfortable fact of life, what can a concerned system
administrator do? The answer lies in flexibility; by performing your job in such a way as to give you (and
your users) the most options possible. Take, for example, the issue of disk space. Given that never having
sufficient disk space seems to be as much a physical law as the law of gravity, it is reasonable to assume
that at some point you will be confronted with a desperate need for additional disk space right now.
What would a system administrator who expects the unexpected do in this case? Perhaps it is possible to
keep a few disk drives sitting on the shelf as spares in case of hardware problems[2]. A spare of this type
could be quickly deployed[3] on a temporary basis to address the short-term need for disk space, giving
time to more permanently resolve the issue (by following the standard procedure for procuring additional
disk drives, for example).
By trying to anticipate problems before they occur, you will be in a position to respond more quickly and
effectively than if you let yourself be surprised.
[2] And of course a system administrator that expects the unexpected would naturally use RAID (or
related technologies) to lessen the impact of a critical disk drive failing during production.
[3] Again, system administrators that think ahead configure their systems to make it as easy as possible to
quickly add a new disk drive to the system.
PREVIOUS

What a Linux administrator must know by head?

I think there are a few skills that are pretty important.
You must be able to configure the network using just cli tools like ifconfig, route, and ip.

A few times a client has called saying their a Linux box had failed. I had them boot a livecd. But the
server was on a network without DHCP (it was the DHCP). Once the system was booted I need to walk
them through starting the network and SSH so I could remotely connect and help them diagnose and fix
what was broken.
You may be at a point where you cannot access the Internet, and you will need to know how to get online.
I think you should know how do a full backup of the system using tar, rsync, or dd. If you don't know how
to do a backup and restore things you almost certainly should not touching systems. You do need to also
actually make sure backups are made before making system changes.
I think you should know how to access the filesystems from a livecd on your servers. This means you
should know how to activate LVM, and Software RAID based drives, access partition information, and
mount the file-systems.
If your server is unbootable, you may need to access the file-system and fix something. It will be pretty
painful trying to figure out how to actually mount things in an emergency. Be prepared ahead of time.
You should be familiar enough with the boot process to be able to change things at boot. Most systems use
GRUB, but you may run into LILO.
Importantly, know how boot into different run-levels such as single-user.
I think you should have at least a working knowledge of how to do some basic captures with tcpdump and
be able to read the results. All the nice GUI features in Wireshark are nice, but if something is broken you
may not actually be able to access Wireshark.
There are a large number of networking problems that I was able to quickly identify and solve just by
running tcpdump.

1.10. Red Hat Enterprise Linux-Specific Information

This section describes information related to the philosophy of system administration that is specific to
Red Hat Enterprise Linux.

1.10.1. Automation

Automation of frequently-performed tasks under Red Hat Enterprise Linux requires knowledge of several
different types of technologies. First are the commands that control the timing of command or script
execution. The cron and at commands are most commonly used in these roles.
Incorporating an easy-to-understand yet powerfully flexible time specification system, cron can schedule
the execution of commands or scripts for recurring intervals ranging in length from minutes to months.
The crontab command is used to manipulate the files controlling the cron daemon that actually schedules
each cron job for execution.
The at command (and the closely-related command batch) are more appropriate for scheduling the
execution of one-time scripts or commands. These commands implement a rudimentary batch subsystem
consisting of multiple queues with varying scheduling priorities. The priorities are known as niceness
levels (due to the name of the command -- nice). Both at and batch are perfect for tasks that must start at a
given time but are not time-critical in terms of finishing.
Next are the various scripting languages. These are the "programming languages" that the average system
administrator uses to automate manual operations. There are many scripting languages (and each system
administrator tends to have a personal favorite), but the following are currently the most common:
The bash command shell
The perl scripting language
The python scripting language
Over and above the obvious differences between these languages, the biggest difference is in the way in
which these languages interact with other utility programs on a Red Hat Enterprise Linux system. Scripts
written with the bash shell tend to make more extensive use of the many small utility programs (for
example, to perform character string manipulation), while perl scripts perform more of these types of
operations using features built into the language itself. A script written using python can fully exploit the
language's object-oriented capabilities, making complex scripts more easily extensible.
This means that, in order to truly master shell scripting, you must be familiar with the many utility
programs (such as grep and sed) that are part of Red Hat Enterprise Linux. Learning perl (and python), on
the other hand, tends to be a more "self-contained" process. However, many perl language constructs are

based on the syntax of various traditional UNIX utility programs, and as such are familiar to those Red
Hat Enterprise Linux system administrators with shell scripting experience.

1.10.2. Documentation and Communication

In the areas of documentation and communication, there is little that is specific to Red Hat Enterprise

Linux. Since documentation and communication can consist of anything from adding comments to a text-
based configuration file to updating a webpage or sending an email, a system administrator using Red Hat
Enterprise Linux must have access to text editors, HTML editors, and mail clients.
Here is a small sample of the many text editors available under Red Hat Enterprise Linux:
The gedit text editor
The Emacs text editor
The Vim text editor
The gedit text editor is a strictly graphical application (in other words, it requires an active X Window
System environment), while vim and Emacs are primarily text-based in nature.
The subject of the best text editor has sparked debate for nearly as long as computers have existed and
will continue to do so. Therefore, the best approach is to try each editor for yourself, and use what works
best for you.
For HTML editors, system administrators can use the Composer function of the Mozilla Web browser. Of
course, some system administrators prefer to hand-code their HTML, making a regular text editor a
perfectly acceptable tool as well.
As far as email is concerned, Red Hat Enterprise Linux includes the Evolution graphical email client, the
Mozilla email client (which is also graphical), and mutt, which is text-based. As with text editors, the
choice of an email client tends to be a personal one; therefore, the best approach is to try each client for
yourself, and use what works best for you.
1.10.3. Security
As stated earlier in this chapter, security cannot be an afterthought, and security under Red Hat Enterprise
Linux is more than skin-deep. Authentication and access controls are deeply-integrated into the operating
system and are based on designs gleaned from long experience in the UNIX community.
For authentication, Red Hat Enterprise Linux uses PAM -- Pluggable Authentication Modules. PAM

makes it possible to fine-tune user authentication via the configuration of shared libraries that all PAM-
aware applications use, all without requiring any changes to the applications themselves.

Access control under Red Hat Enterprise Linux uses traditional UNIX-style permissions (read, write,
execute) against user, group, and "everyone else" classifications. Like UNIX, Red Hat Enterprise Linux
also makes use of setuid and setgid bits to temporarily confer expanded access rights to processes running
a particular program, based on the ownership of the program file. Of course, this makes it critical that any
program to be run with setuid or setgid privileges must be carefully audited to ensure that no exploitable
vulnerabilities exist.
Red Hat Enterprise Linux also includes support for access control lists. An access control list (ACL) is a
construct that allows extremely fine-grained control over what users or groups may access a file or
directory. For example, a file's permissions may restrict all access by anyone other than the file's owner,
yet the file's ACL can be configured to allow only user bob to write and group finance to read the file.
Another aspect of security is being able to keep track of system activity. Red Hat Enterprise Linux makes
extensive use of logging, both at a kernel and an application level. Logging is controlled by the system
logging daemon syslogd, which can log system information locally (normally to files in the /var/log/
directory) or to a remote system (which acts as a dedicated log server for multiple computers.)
Intrusion detection sytems (IDS) are powerful tools for any Red Hat Enterprise Linux system
administrator. An IDS makes it possible for system administrators to determine whether unauthorized
changes were made to one or more systems. The overall design of the operating system itself includes
IDS-like functionality.
Because Red Hat Enterprise Linux is installed using the RPM Package Manager (RPM), it is possible to
use RPM to verify whether any changes have been made to the packages comprising the operating
system. However, because RPM is primarily a package management tool, its abilities as an IDS are
somewhat limited. Even so, it can be a good first step toward monitoring a Red Hat Enterprise Linux
system for unauthorized modifications.

1.11.2. Useful Websites

http://www.kernel.org/pub/linux/libs/pam/ -- The Linux-PAM project homepage.
http://www.usenix.org/ -- The USENIX homepage. A professional organization dedicated to bringing
together computer professionals of all types and fostering improved communication and innovation.
http://www.sage.org/ -- The System Administrators Guild homepage. A USENIX special technical group
that is a good resource for all system administrators responsible for Linux (or Linux-like) operating
systems.
http://www.python.org/ -- The Python Language Website. An excellent site for learning more about
Python.
http://www.perl.org/ -- The Perl Mongers Website. A good place to start learning about Perl and
connecting with the Perl community.
http://www.rpm.org/ -- The RPM Package Manager homepage. The most comprehensive website for
learning about RPM.
