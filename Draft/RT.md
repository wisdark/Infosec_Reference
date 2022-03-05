# Red Teaming/Adversary (Emu/)Simulation/Explicitly Pen testing stuff

------------------------------------------------------------------------------------------------------------------------------
## Table of Contents
- Stuff is sorted into various categories, use the following top-level ToCs for quick access to the appropriate ToC
- [General Stuff](#general)
	- [101](#101)
	- [Courses](#gcourses)
	- [General Informative Information](#gii)
	- [Generally Relevant/Useful Information](#grui)
	- [Red Team Experiencs](#rte)
	- [Papers](#gpapers)
	- [Other](#rother)
- [Adversary Emu/Simu ; Building(and growing) a Red Team ; Organizing a Red Team Engagement](#first)
- [C2s & Infrastructure](#c2ss)
- [Simulation Tools](#simtools)
	- [Articles/Blogposts/Writeups](#sta)
	- [Talks/Presentations/Videos](#stpv)
	- [Adversary Simulation Tools](#sast)
- [Implants & Payload Development](#implants)
- [Advanced Persistent Threat Actors & Campaigns](#aptdata)
	- [Campaigns](#aptcamp)
- [Tactics/Strategies/Methodologies](#tacticsandstats)
	- [Lessons Learned](#vll)
	- [Tactics](#ttactics)
	- [Strategies](#tstrats)
	- [Methodologies](#tmethods)
	- [Skills Improvement](#vskill)
- [Penetration Testing](#pentest)
	- [Culture](#culture)
	- [Workflows](#penworkflows)
	- [Enagement Types](#pentypes)
- [PenTesting X](#penx)
	- [AIX](#aix)
	- [Embedded](#embedded)
	- [Faxes, Printers, Other](#faxesprint)
	- [MainFrames](#main)
	- [SCADA/PLCs](#scada)
	- [Virtual Appliances](#va)
------------------------------------------------------------------------------------------------------------------------


------------------------------------------------------------------------------------------------------------------------
### Adversary Emu/Simu ; Building(and growing) a Red Team ; Organizing a Red Team Engagement<a name="first"></a>
- [Adversary Simulation &Or Emulation](#advsim)
	- [Articles/Blogposts/Writeups](#advart)
	- [Talks/Presentations/Videos](#advvid)
	- [Simulation Plans](#advplans)
	- [Tools](#advtools)
- [Building(and Growing) a (Red) Team](#dreamteam)
	- [101](#team101)
	- [Articles/Blogposts/Writeups](#teamart)
	- [Talks/Presentations/Videos](#teamtalks)
- [Organizing a Red Team Engagement](#engagered)
	- [Frameworks & Methodologies](#methods)
	- [Facilitating a Red Team Engagement](#farte)
	- [Metrics & models](#gmm)
	- [Purple Teaming](#purple)
------------------------------------------------------------------------------------------------------------------------


------------------------------------------------------------------------------------------------------------------------
### C2s & Infrastructure<a name="c2ss"></a>
- [Command, Control, Communicate (or just CnC, or C3)](#c2s)
	- [General stuff](#c2gs)
	- [C2 Development](#c2d)
	- [C2 Frameworks](#c2-frames)
	- [Communication Channel Example PoCs](#c2cc)
	- [Papers about C2s](#c2papers)
- [Infrastructure](#infra)
	- [101](#i101)
	- [Articles/Blogposts/Writeups](#iarticles)
	- [HW/SW for Remote Testing](#remote-testing)
	- [Logging & Monitoring](#ilm)
	- [Web Server](#iws)
	- [Automation Tooling](#iat)
- [Cobalt Strike](#cobaltstrike)
	- [101](#cs101)
	- [Agressor Scripts](#csas)
	- [Beacon](#csbeacon)
	- [C2](#csc2)
	- [Documentation](#csdoc)
- [Empire](#empire)
	- [Articles](#articles)
	- [Customizing](#ecustom)
	- [Manual](#edoc)
	- [Modules & Additions/Extensions](#emods)
	- [Modules & Additions/Extensions](#emods)
	- 
- [Domains and Domain Related Things](#domains) 
	- [General](#dg)
	- [Domain Fronting](#df)
	- [Tools](#dt)
	- [Domain reputation](#dr)
- [Egress & Exfiltration](#egress)
	- 
- [External Attack Surface](#external)
------------------------------------------------------------------------------------------------------------------------


------------------------------------------------------------------------------------------------------------------------
### Implants & Payload Development<a name="implants"></a>
- [Start of this Section](#implantdev)
- [Creation & Development](#pcd)
- [Anti-Tricks](#anti-tricks)
	- [Anti-Dbg](#anti-dbg)
	- [Anti-UnPackers](#anti-packer)
	- [Anti-RE](#anti-re)
	- [Anti-Sandbox](#anti-sandbox)
	- [Bring-Your-Own ...](#byoc)
	- [Crypters](#crypter)
	- [Meta/Poly-Morphism](#metapoly)
	- [Obfuscation](#obfuscation)
	- [Packers](#packers)
- [Evasion](#evasion)
- [Network Communications](#netcomms) - FIX
	- [Communication Channel Examples/Samples/PoCs](#c2commsamples)
	- [Protocols](#protocols)
		- [DNS](#dns1)
		- [DNS-over-HTTPS(DoH)](#doh1)
		- [HTTP](http1)
		- [HTTP2](http2)
		- [HTTP3](#http3)
		- [QUIC](#quic)
	- [Tricks](#tricks1)
- [Obfuscation Techniques](#obfuscation1)
	- []()
	- []()
- [Meta/Poly/Oligo-Morphism](#metapoly)
- [Packers](#packers)
- [Publishing](#ipub)
- [Updates](#updates)
- [Language Specific](#langspec)
	- [AutoIT](#autoitlang)
	- [Basic](#basiclang)
	- [C](#clang)
	- [C++](#cppp)
	- [CSharp](#csharppay)
	- [CSharp _Other_ stuff](#csharpother)
	- [Go](#gopay)
	- [Haskell](#haskell)
	- [Janet](#janet)
	- [Java](#java)
	- [.NET](#.net)
	- [Nim](#nim)
	- [PowerShell](#powershell)
	- [Python](#python)
	- [Rust](#rust)
- [Linux Specific](#linspec)
- [macOS Specific](#macspec)
- [Windows Specific](#winspec)
- [Delivery & Staging](#pds)
- [Access Methods/Tools](#access)
- [Physical Implants](#pimplant)
	- [HW Related/Physical Devices](#hw)
	- [Dropboxes](#dropboxes)
	- [Physical Implants](#implants)
	- []()
------------------------------------------------------------------------------------------------------------------------------



----------------------------------------------------------------------------------------------------------------
### <a name="general"></a>General
* **101**<a name="101"></a>
	* [Red Team - Wikipedia](https://en.m.wikipedia.org/wiki/Red_team)
	* [Common Ground Part 1: Red Team History & Overview](https://www.sixdub.net/?p=705)
	* [Target Analysis - Wikipedia](https://en.wikipedia.org/wiki/Target_analysis)
	* [Center of Gravity Analysis - Dale C. Eikmeier](http://www.au.af.mil/au/awc/awcgate/milreview/eikmeier.pdf)
		* Center of Gravity: A system's source of power to act.
	* [A Tradecraft Primer: Structured Analytic Techniques for Improving Intelligence Analysis - USGov 2009](https://www.cia.gov/library/center-for-the-study-of-intelligence/csi-publications/books-and-monographs/Tradecraft%20Primer-apr09.pdf)
	* [The Black Team](http://www.penzba.co.uk/GreybeardStories/TheBlackTeam.html)
	* [IBM Black Team](http://www.t3.org/tangledwebs/07/tw0706.html)
	* [RedTeaming from Zero to One – Part 1 - Rashid Feroze](https://payatu.com/redteaming-from-zero-to-one-part-1)
		* [Part 2](https://payatu.com/redteaming-zero-one-part-2/)
* **Courses**<a name="gcourses"></a>
	* [Advanced Threat Tactics – Course and Notes - CobaltStrike](https://blog.cobaltstrike.com/2015/09/30/advanced-threat-tactics-course-and-notes/)
	* [Red v Blue Workshop - WOPR Summit - Taylor, Dan, Phil](https://github.com/ahhh/presentations/blob/master/Red%20V%20Blue%20Workshop.pdf)
* **General Informative Information**<a name="gii"></a>
	* **Articles/Blogposts/Writeups**
		* [Offensive Tool Design and the Weaponization Dilemma - Matt Graeber(2015)](http://www.exploit-monday.com/2015/12/offensive-tool-design-and-weaponization.html)
		* [Fools of Golden Gate](https://blog.silentsignal.eu/2017/05/08/fools-of-golden-gate/)
			* How major vulnerabilities/large amounts of publicly vulnerable systems can exist without public recognition for long periods of time. (i.e. CVEs(10.0) exist, but no mapping in nessus/metasploit/etc)
		* [Red Teaming and the Adversarial Mindset: Have a Plan, Backup Plan and Escape Plan - ITS](https://www.itstactical.com/digicom/security/red-teaming-and-the-adversarial-mindset-have-a-plan-backup-plan-and-escape-plan/)
		* [Raphael’s Magic Quadrant - Mudge](https://blog.cobaltstrike.com/2015/08/03/raphaels-magic-quadrant/)
		* [RAT - Repurposing Adversarial Tradecraft - killswitch_GUI](https://speakerdeck.com/killswitch_gui/rat-repurposing-adversarial-tradecraft)
		* [Penetration Testing considered Harmful Today](http://blog.thinkst.com/p/penetration-testing-considered-harmful.html)
		* [Red Team Gut Check - Tim MalcomVetter](https://medium.com/@malcomvetter/red-team-gut-check-10b5976ffd19)
		* [Internal Red Teams and Insider Knowledge - Tim MalcomVetter](https://medium.com/@malcomvetter/internal-red-teams-and-insider-knowledge-8324555aaf40)
		* [Red Teaming: From the Military to Corporate Information Security Teams - 4n7m4n](https://medium.com/@antman1P_30185/red-teaming-from-the-military-to-corporate-information-security-teams-408c040bd87e)
		* [What I’ve Learned in Over a Decade of “Red Teaming” - Dominic Chell](https://medium.com/@dmchell/what-ive-learned-in-over-a-decade-of-red-teaming-5c0b685c67a2)
		* [The Future of Adversaries is Software Development - Tim Malcomvetter(2019)](https://medium.com/@malcomvetter/the-future-of-adversaries-is-software-development-f599c3da2a9f)		
		* [Low Hanging Fruit Often Abused By Red Teams - Cedric Owens(2018)](https://medium.com/red-teaming-with-a-blue-team-mentaility/low-hanging-fruit-often-abused-by-red-teams-b9a66026d89e)
		* [Google Calendar Event Injection with MailSniper](https://www.blackhillsinfosec.com/google-calendar-event-injection-mailsniper/)	
		* [RedTips](https://github.com/vysecurity/RedTips)
			* Red Team Tips as posted by @vysecurity on Twitter
		* [On Better Red Teaming - Action Dan(2019)](https://lockboxx.blogspot.com/2019/12/on-better-red-teaming.html)			
		* [3 Principles of Red Teaming - Action Dan(2020)](https://lockboxx.blogspot.com/2020/01/3-principles-of-red-teaming.html)
		* [Thoughts on the recent Red Team debate - Jonas Bauters(2020)](https://blog.nviso.eu/2020/01/17/thoughts-on-the-recent-red-team-debate/)
			* [The Problems With Today's Red Teaming - Florian Roth(2019)](https://cyb3rops.medium.com/the-problems-with-todays-red-teaming-7b8ed1e735c9)
			* [What I’ve Learned in Over a Decade of “Red Teaming” - Dominic Chell(2019)](https://medium.com/@dmchell/what-ive-learned-in-over-a-decade-of-red-teaming-5c0b685c67a2)
	* **Talks/Presentations/Videos**
		* [Why I Love Offensive Work, Why I don't Love Offensive Work - Halvar Flake(OffensiveCon20)](https://www.youtube.com/watch?v=8QRnOpjmneo)
		* [Red Team Apocalypse - Beau Bullock and Derek Banks(BSides Tampa2018)](https://www.irongeek.com/i.php?page=videos/bsidestampa2018/courtroom02-red-team-apocalypse-beau-bullock-and-derek-banks)
			* Abstract: TABLETOP SCENARIO: Your organization regularly patches, uses application whitelisting, has NextGen-NG firewalls/IDS's, and has the latest Cyber-APT-Trapping-Blinky-Box. You were just made aware that your entire customer database was found being sold on the dark web. Go. Putting too much trust in security products alone can be the downfall of an organization. In the 2015 BSides Tampa talk ""Pentest Apocalypse"" Beau discussed 10 different pentesting techniques that allow attackers to easily compromise an organization. These techniques still work for many organizations but occasionally more advanced tactics and techniques are required. This talk will continue where ""Pentest Apocalypse"" left off and demonstrate a number of red team techniques that organizations need to be aware of in order to prevent a ""Red Team Apocalypse"" as described in the tabletop scenario above."
		* [Prowling: Better Penetration Testing - J Wolfgang Goerlich(Converge2018)](https://www.irongeek.com/i.php?page=videos/converge2018/converge-2018-207-prowling-better-penetration-testing-j-wolfgang-goerlich)
			* "But we passed our penetration test," the person handling the security breach groaned. "How come they missed this?" Since the late 1960s, penetration testing has been about two things: demonstrating that the system can be broken into and finding some vulnerabilities. But, by now? We all know systems can be broken into. The shock and surprise are gone. And we all know there are vulnerabilities. Scores of vulnerabilities. Too many vulnerabilities. In fact, arguably today,s penetration testing doesn,t even identify a fraction of the vulnerabilities. This session will review the state of testing strategies and present predictions on where penetration testing should go in the future
		* [Backdooring With Metadata - Backdooring With Metadata - Itzik Kotler(Converge2018)](https://www.irongeek.com/i.php?page=videos/converge2018/converge-2018-203-backdooring-with-metadata-itzik-kotler)
			* Not all binaries were created equal, some are small, some are big, and some can be abused to gain arbitrary code execution. In this talk, I,ll demo how tens of popular, already-installed binaries in popular OS,s such as Linux, FreeBSD, Oracle Solaris, macOS etc. can be turned into backdoors with just one command-line. The icing on the cake? That one command-line won,t change the content or size of binaries, it will only change the metadata. Come see how you can save disk space and bandwidth in your next red team / penetration testing engagement.
		* [Skills For A Red-Teamer - Brent White, Tim Roberts(Nolacon2018)](https://www.irongeek.com/i.php?page=videos/nolacon2018/nolacon-2018-104-skills-for-a-red-teamer-brent-white-tim-roberts)
			* Want to incorporate hybrid security assessments into your testing methodology? What does going above and beyond look like for these types of assessments? How do you provide the best value with the resources and scope provided? What do some of these toolkits encompass? If you‚Äôre interested in what skills are needed for a Red-Teamer, or taking your red teaming assessments to the next level, here‚Äôs the basic info to get you started. We‚Äôll discuss items of importance, methodology, gear, stories and even some tactics used to help give you an edge.
		* [Offensive Cartography - Trenton Ivey(ShowMeCon2018)](https://www.irongeek.com/i.php?page=videos/showmecon2018/showmecon-2018-track-1-05-offensive-cartography-trenton-ivey)
			* Understanding the operational environment is an important part of any offensive operation. This can be a daunting task during Computer Network Exploitation (CNE) and Computer Network Attack (CNA) operations because the target environment is often complex, abstract, and constantly changing. However, by consuming the output of common offensive tools and storing information in a normalized, graph-based database, it is possible to create a detailed map of the target environment that both humans and automated tools can efficiently leverage. This talk will discuss the challenges and benefits of mapping the operational environment, and will provide examples of how both offensive and defensive teams can leverage the resulting maps to increase their chances of success.
		* [The Art of Cyberwar: A Foundation and Framework for the Development of TTPs - Kevin L Johnson(ShowMeCon20119)](https://www.irongeek.com/i.php?page=videos/showmecon2019/showmecon-2019-03-the-art-of-cyberwar-a-foundation-and-framework-for-the-development-of-ttps-kevin-l-johnson)
			* Cyberspace is a warfighting domain, on par with other warfighting domains: Land, Sea, Air, and Space. It is a force multiplier, securing and enhancing the effectiveness of other domains and their missions. It is also the world's newest warfighting asset that demands attention; defensive and offensive as well as tactical and strategic. When I took on this endeavor, many have often asked, how can I cover such a broad and enigmatic topic? Particularly, when so many still argue over the definition of cyber, how, where and when it should be applied? Who should be in charge of it and when command and control is delegated. Someone(s) has made this more complex than it needs to be. The realization of cyber and its proper application has been long overdue for the laying of plans. Cyberwar is an integral part of war, Sun Tzu having already laid the groundwork.Sun Tzu said: 1. The art of war is of vital importance to the state.2. It is a matter of life and death, a road either to safety or ruin.There is much to be said about the correlation between the Art of War and the Art of Cyberwar; however, that being said this not a replacement for the Art of War nor is it an evolution. It is simply, like its namesake, a framework and foundation; empirical guidance on what is important and why. The Art of Cyberwar starts with the 'Tenets of Cyberwar'. And, comparable to Sun Tzu, "The General that harkens to my counsel and acts upon it, will conquer: let such a one be retained in command! The General that hearkens not to my counsel nor acts upon it will suffer defeat: let such a one be dismissed." The Tenets of Cyberwar are: Reduce the Threat Surface (Reduce/Eliminate Access, TRU Encryption: 'in-Transit, at-Rest, in-Use', Defense-in-Depth, Deny by Default/Allow by Exception), Cyber Terrain, Defensive Cyber Operations (DCO), Offensive Cyber Operations (OCO), Threat Actors, Legal-Ease, Cyber Partners and Emerging Technologies. It is these key tenets that help highlight the importance of cyber in war, in its element, cyberspace. Cyberspace is a key tenet of kinetic success - on and off the battlefield. Cyberwar targeting and attack does not exist in a battlefield vacuum! In Cyberwar, all cyber services (Financial, Medical, Alert Systems/First Responders: Fire, Police, Ambulance, Industrial, SCADA, Transportation, Communication Networks, Supply Chains, etc.) are all impacted. In addition, to the military aspect!An attack by a threat actor/adversary does not and will not limit itself to battlefield targets; at one time, separation between battlefield and the actual nation state was dependent on where the actual battle was fought with the location of the battlefield taking the biggest negative impact. However, it is no longer the situation. Anyone, anywhere, with the right capabilities, resources and skill sets can impact any country without co-location to the country or battlefield. The Art of Cyberwar requires a change in how countries prosecute their wars, how they plan and prepare, and how they determine and define war. The world is already at war. Some countries know it; others simply don't or don't want to believe it and getting up to speed is the true challenge. It is a mission impossible. But, unlike the old TV series and recent movies, every country, company and infrastructure must start with the basics the best offense is a good defense. In cyberspace, they who attack without the benefit of good defenses is mutually assuring their destruction.
	* **Resources**
		* [Red Team Infrastructure Wiki](https://github.com/bluscreenofjeff/Red-Team-Infrastructure-Wiki)
			* Wiki to collect Red Team infrastructure hardening resources
			* Accompanying Presentation: [Doomsday Preppers: Fortifying Your Red Team Infrastructure](https://speakerdeck.com/rvrsh3ll/doomsday-preppers-fortifying-your-red-team-infrastructure)
		* [Planning a Red Team exercise](https://github.com/magoo/redteam-plan)
		* [Red Teaming Quick Reference Sheet - Sandia Labs(USGov)](https://idart.sandia.gov/_assets/documents/2017-09-13_RT4PM_QRS-Paper-Size.pdf)
			* This quick reference sheet is a component of Sandia'sRed Teaming for Program Managers class.
		* [IDART Quick Reference Sheet - Sandia Labs(USGov)](https://idart.sandia.gov/_assets/documents/2017-09-13_IDART_QRS-Paper-Size.pdf)
* **Generally Relevant/Useful Information**<a name="grui"></a>
	* [The ‘Laws’ of Red Teaming - RedTeam Journal](https://redteamjournal.com/red-teaming-laws/)
		* Red teaming is governed by informal and wholly unscientific “laws” based largely on human nature. These laws are driven by paradox and, in many cases, a healthy dose of humor. We state some from a general perspective, some from the perspective of the customer or sponsor, and some from the perspective of the red team. Enjoy. We add to these as the mood strikes. (For an alternative list of rules, try the one at redteams.net.)
	* [Beyond Red Teaming Cards - ](https://www.reciprocalstrategies.com/resources/brt_cards/)
		* The Beyond Red Teaming (BRT) cards extend the Red Team Journal Red Teaming “Laws” and cards. The purpose of the BRT cards is to help security professionals consider and assess their own frames and narratives.
	* [Goodbye OODA Loop](http://armedforcesjournal.com/goodbye-ooda-loop/)
	* [Some Comments and Thoughts on Tradecraft](https://www.darkoperator.com/blog/2017/11/20/some-comments-and-thoughts-on-tradecraft)
	* [Terrorists and Technological Innovation - Daveed Gartenstein-Ross, Colin P. Clarke, Matt Shear](https://www.lawfareblog.com/terrorists-and-technological-innovation)
	* ["If we win, we lose" - Malcom Vetter(BlueHat v18)](https://www.youtube.com/watch?v=ifCeaYShRSU)
		* [Slides](https://www.slideshare.net/MSbluehat/if-we-win-we-lose-using-healthy-competition-to-measure-and-improve-security-programs)
		* In this talk, we’ll dig into the dichotomy of the Red vs. Blue competition, cut through the unhealthy competitive noise, highlight what healthy competition looks like, and let that naturally lead us towards program measurement and team comparison. Somebody has to come out on top and somebody on bottom—how can we know which is which, and how can we move more organizations into the top category while maintaining the momentum to move the best InfoSec programs higher still? Maybe an Ancient Greek from 2,500 years ago can help us do that … with some (sanitized) Red Team, post-campaign insights about what good and bad security really looks like, and some sprinkled in recommendations for how Microsoft products can help them get there. It’s half-time, you’re behind but it’s close, our coach has a plan, and you’re now motivated to improve detection and response. It’s time to win, not lose!
	* [The Duality of Attackers - Or Why Bad Guys are a Good Thing™ - carnal0wnage(2020)](https://carnal0wnage.attackresearch.com/2020/04/the-duality-of-attackers-or-why-bad.html)
	* [Red Team Tips - Jean-François Maes](https://redteamer.tips/red-team-tips/)
	* [Operators, EDR Sensors, and OODA Loops - @Jackson_T(2021)](https://jackson-t.ca/ooda-loops.html)
	* [Operational Mental Models - @Jackon_T](https://jackson-t.ca/operational-mental-models.html)
* **Red Team Experiences**<a name="rte"></a>
	- **Articles/Blogposts/Writeups**
		* [Red Teaming Tips - Vincent Yiu](https://threatintel.eu/2017/06/03/red-teaming-tips-by-vincent-yiu/)
		* [Red Team Tips as posted by @vysecurity on Twitter](https://github.com/vysec/RedTips)
		* [Red Teams - Facebook Experiences Writeup - Ryan McGeehan](https://medium.com/starting-up-security/red-teams-6faa8d95f602)
		* [Reflections from a Red Team Leader - Susan Craig](http://usacac.army.mil/CAC2/MilitaryReview/Archives/English/MilitaryReview_20070430_art011.pdf)
		* [Red Teaming: Using Cutting-Edge Threat Simulation to Harden the Microsoft Enterprise Cloud](https://azure.microsoft.com/en-us/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/)
		* [10 Red Teaming Lessons Learned over 20 Years](https://redteamjournal.com/2015/10/10-red-teaming-lessons-learned-over-20-years/)
		* [Red team versus blue team: How to run an effective simulation - CSOonline](https://www.csoonline.com/article/2122440/disaster-recovery/emergency-preparedness-red-team-versus-blue-team-how-to-run-an-effective-simulation.html)
		* [Red Teaming for Pacific Rim CCDC 2017](https://bluescreenofjeff.com/2017-05-02-red-teaming-for-pacific-rim-ccdc-2017/)
		* [How I Prepared to Red Team at PRCCDC 2015](https://bluescreenofjeff.com/2015-04-15-how-i-prepared-to-red-team-at-prccdc-2015/)
		* [Red Teaming for Pacific Rim CCDC 2016](https://bluescreenofjeff.com/2016-05-24-pacific-rim-ccdc_2016/)
		* [Defenders, Bring Your 'A' Game](https://winterspite.com/security/defenders-bring-your-a-game/)
		* [Responsible Red Teams - Tim MaclomVetter](https://medium.com/@malcomvetter/responsible-red-teams-1c6209fd43cc)
			* [Response by John Strand](https://medium.com/@john_43488/there-was-a-very-well-thought-out-article-on-responsible-red-teaming-by-tim-malcomvetter-7131faa17047)
		* [RedTeaming from Zero to One – Part 1 - payatu.com](https://payatu.com/redteaming-from-zero-to-one-part-1/)
		* [RedTeaming from Zero to One – Part 2 - payatu.com](https://payatu.com/redteaming-zero-one-part-2/)
		* [Red Team Tales 0x01: From MSSQL to RCE - Pablo Martinez](https://www.tarlogic.com/en/blog/red-team-tales-0x01/)
			* In a Red Team operation, a perimeter asset vulnerable to SQL Injection was identified. Through this vulnerability it was possible to execute commands on the server, requiring an unusual tactic to achieve the exfiltration of the output of the commands. In this article we will explain the approach that was followed to successfully compromise this first perimeter element that was later used to pivot the internal network.
		* [There is a shell in your lunch-box - Rotimi Akinyele](https://hakin9.org/shell-lunch-box-rotimi-akinyele/)
		* [Old Skool Red Team - DiabloHorn](https://diablohorn.com/2019/12/28/old-skool-red-team/)
		* [Black Team War Stories: Which company are you a contractor with? - Mark Frost(2019)](https://www.nccgroup.com/uk/about-us/newsroom-and-events/blogs/2019/july/black-team-war-stories-which-company-are-you-a-contractor-with/)
		* [Finding Weaknesses Before the Attackers Do - Alyssa Rahman, Curtis Antolik(2019)](https://www.mandiant.com/resources/finding-weaknesses-attackers-do)
		* [ Anatomy of a Red-Team exercise – Chapter 1 - CyberForce Offensive Security Team(2021)](https://ictexpertsluxembourg.lu/technical-corner/anatomy-of-a-red-team-exercise-chapter-1/)
			* [Part 2](https://ictexpertsluxembourg.lu/technical-corner/anatomy-of-a-red-team-exercise-chapter-2/)
		* [How I hacked into a Telecom Network — Part 1 (Getting the RCE) - Harpreet Singh(2020)](https://medium.com/bugbountywriteup/how-i-hacked-into-a-telecom-network-part-1-getting-the-rce-167c2bb320e6)
			* [How I hacked into a Telecom Network — Part 2 (Playing with Tunnels: TCP Tunneling)](https://medium.com/bugbountywriteup/how-i-hacked-into-a-telecom-network-part-2-playing-with-tunnels-tcp-tunneling-b4cef2837938)
			* [How I hacked into a Telecom Network — Part 3 (Playing with Tunnels: Stealthy SSH & Dynamic Tunnels)](https://medium.com/bugbountywriteup/how-i-hacked-into-a-telecom-network-part-3-playing-with-tunnels-stealthy-ssh-dynamic-tunnels-5ac26557d0eb)
			* [How I hacked into a Telecom Network — Part 4 (Getting Access to CDRs, SS7 applications & VLRs)](https://medium.com/bugbountywriteup/how-i-hacked-into-a-telecom-network-part-4-getting-access-to-cdrs-ss7-applications-vlrs-9a8cf95e2648)
	* **External to Internal**
		* **Articles/Blogposts/Writeups**
			* [From OSINT to Internal: Gaining Domain Admin from Outside the Perimeter - Esteban Rodriguez](https://www.coalfire.com/The-Coalfire-Blog/Sept-2018/From-OSINT-to-Internal-Gaining-Domain-Admin)
			* [From OSINT to Internal – Gaining Access from outside the perimeter - n00py](https://www.n00py.io/2017/03/from-osint-to-internal-gaining-access-from-the-outside-the-perimeter/)
		* **Tools that I couldn't decide where else to put**
			* [intrigue-core](https://github.com/intrigueio/intrigue-core)
				* Intrigue-core is a framework for external attack surface discovery and automated OSINT.
			* [DeviceDetector.NET](https://github.com/totpero/DeviceDetector.NET)
				* The Universal Device Detection library will parse any User Agent and detect the browser, operating system, device used (desktop, tablet, mobile, tv, cars, console, etc.), brand and model.
* **Papers**<a name="gpapers"></a>
	* [Red teaming - A Short Introduction (1.0) June 2009 - Mark Mateski](https://redteamjournal.com/papers/A%20Short%20Introduction%20to%20Red%20Teaming%20(1dot0).pdf)
	* [Red Teaming Guide - UK Ministry of Defense](https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/142533/20130301_red_teaming_ed2.pdf)
	* [Red Team Handbook(2012) - University of Foreign Military And Cultural studies](http://www.au.af.mil/au/awc/awcgate/army/ufmcs_red_team_handbook_apr2012.pdf)
	* [Red Teaming of Advanced Information Assurance Concepts - Bradley Wood, Ruth Duggan](http://cs.uccs.edu/~gsc/pub/master/sjelinek/doc/research/red.pdf)
	* [A Guide To Red Teaming - NATO](http://www.act.nato.int/images/stories/events/2011/cde/rr_ukdcdc.pdf)
	* [Modeling and Simulation of Red Teaming - Part 1: Why Red Team M&S? - Michael J Skroch](https://redteamjournal.com/wp-content/uploads/2009/12/msrt0.3-2nov2009-sand2009-7215J.pdf)
	* [Moving Forward with Computational Red Teaming - Scott Wheeler - Australian DoD](http://www.dtic.mil/dtic/tr/fulltext/u2/a569437.pdf)
	* [Cyber Red Teaming  Organisational, technical and legal implications in a military context - NATO](https://ccdcoe.org/sites/default/files/multimedia/pdf/Cyber_Red_Team.pdf)
	* [Traditions In Military-Strategic Thought In Germany And The Problem Of Deterrence - 1989 - Detlef Bald](http://www.mgfa.de/html/einsatzunterstuetzung/downloads/ap018englisch.pdf?PHPSESSID=931748af0e86616800373655acaf2902)
	* [Force Protection and Suicide Bombers: The Necessity for Two Types of Canadian Military Red Teams](http://www.journal.forces.gc.ca/vol12/no4/page35-eng.asp)
	* [The Applied Critical Thinking Handbook(2015) - University of Foreign Military And Cultural studies](http://usacac.army.mil/sites/default/files/documents/ufmcs/The_Applied_Critical_Thinking_Handbook_v7.0.pdf)
	* [Preparing for the War of the Future in the Wake of Defeat: The Evolution of German Strategic Thought, 1919 - 1935 - Mark Shannon](https://www.ciaonet.org/attachments/25573/uploads)
	* [Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains](https://www.lockheedmartin.com/content/dam/lockheed/data/corporate/documents/LM-White-Paper-Intel-Driven-Defense.pdf)		
	* [Ananalysis of the Metasploit Framework relative to the Penetration Testing Execution Standard(PTES) guidance(2011) - Brandon Perry](http://www.nothink.org/metasploit/documentation/metasploit_msf_analysis_ptes.pdf)
	* [Microsoft Cloud Red Teaming(2016) - gallery.technet](https://gallery.technet.microsoft.com/Cloud-Red-Teaming-b837392e)
		* This whitepaper discusses Microsoft’s strategy and execution of Red Teaming and live site penetration testing against Microsoft managed cloud infrastructure, services and applications. You will learn how Microsoft simulates real-world breaches, conducts continuous security monitoring and practices security incident response to validate and improve the security of Microsoft Azure and Office 365. In addition, you will gain visibility into procedures that customers should consider when deploying and managing cloud-based assets in a secure manner.
	* [Five Ways I got Caught before Lunch - RastaMouse(Mystikcon 2021)](https://www.youtube.com/watch?v=qIbrozlf2wM)
	* [An Introduction to Red Team Assessments | Payatu | Hrushikesh Kakade(2021)](https://www.youtube.com/watch?v=D0VlGr6KVeM)
	* [Guide to Red Team Operations - Yashika Dir(2019)](https://www.hackingarticles.in/guide-to-red-team-operations/)
	* [A Hands-On Introduction to Mandiant's Approach to OT Red Teaming - Mark Heekin, Daniel Kapellmann Zafra, Nathan Brubaker, Ken Proska, Rob Caldwell(2020)](https://www.mandiant.com/resources/hands-on-introduction-to-mandiant-approach-to-ot-red-teaming)
	* [Exploiting UN-attended Web Servers To Get Domain Admin – Red Teaming - wesecureapp(2019)](https://wesecureapp.com/blog/exploiting-un-attended-web-servers-to-get-domain-admin-red-teaming/)
	* [A Red Team Operation Leveraging a zero-day vulnerability in Zoom - Laurent Deloseieres(2021)](https://medium.com/manomano-tech/a-red-team-operation-leveraging-a-zero-day-vulnerability-in-zoom-80f57fb0822e)
* **Other**<a name="gother"></a>
	* [The Definition of a Green Team: A proposed definition for Green Team, and how it differs from a Red Team - Daniel Messler](https://danielmiessler.com/blog/the-definition-green-team-how-different-red-team/)
* **Misc**
	* [Red_Team](https://github.com/BankSecurity/Red_Team)
		* Some scripts useful for red team activities
	* [Penetration-Testing-Tools - mgeeky](https://github.com/mgeeky/Penetration-Testing-Tools)
		*  A collection of more than a 140+ tools, scripts, cheatsheets and other loots that I have developed over years for Penetration Testing and IT Security audits purposes. Most of them came handy at least once during my real-world engagements. 
	* [PenTesting-Scripts - killswitch-GUI](https://github.com/killswitch-GUI/PenTesting-Scripts)
	* [Red Teaming/Adversary Simulation Toolkit - infosecn1nja](https://github.com/infosecn1nja/Red-Teaming-Toolkit)
	* [Red Team Powershell Scripts - Mr-Un1k0d3r](https://github.com/Mr-Un1k0d3r/RedTeamPowershellScripts)
------------------------------------------------------------------------------------------------------------------------------







































------------------------------------------------------------------------------------------------------------------------------
### <a name="advsim"></a>Adversary Simulation &Or Emulation
* **101**
	* [Emulation, Simulation, & False Flags - Tim Malcomvetter(2020)](https://malcomvetter.medium.com/emulation-simulation-false-flags-b8f660734482)
	* [What’s in a name? Thoughts on Red Team nomenclature - John Bauters(2020)](https://blog.nviso.eu/2020/01/23/thoughts-on-red-team-nomenclature/)
* **Articles/Blogposts/Writeups**<a name="advart"></a>
	* [Persistence Testing / Detection Testing / Purple Teaming - Action Dan(2016)](https://lockboxx.blogspot.com/2016/05/persistence-testing-detection-testing.html)
	* [APT Emulation Theory - Action Dan(2019)](https://lockboxx.blogspot.com/2019/08/apt-emulation-theory.html)
	* [Scenario Based Blog Post - Part 1 - Sneakidia(2020)](https://sneakidia.blogspot.com/2020/11/scenario-based-blog-part-1.html)
		* [Part 2](https://sneakidia.blogspot.com/2021/01/scenario-based-blog-post-part-2.html)
	* [Emulation, Simulation, & False Flags - Tim Malcomvetter(2020)](https://medium.com/@malcomvetter/emulation-simulation-false-flags-b8f660734482)
	* [Mimicking evil - David Hunt(2021)](https://feed.prelude.org/p/mimicking-evil)
	* [The Rise of Adversary Emulation - Jonas Bauters(2018)](https://blog.nviso.eu/2018/09/18/the-rise-of-adversary-emulation/)
	* [Using Research to Gain Attack Intelligence - Stephen Marchewitz, Carlos Perez, Christopher Paschen(2020)](https://www.trustedsec.com/events/using-research-to-gain-attack-intelligence/)
* **Talks/Presentations/Videos**<a name="advvid"></a>
	* [How to Start a Cyber War: Lessons from Brussels - Chris Kubecka(BSides Charm 2019)](http://www.irongeek.com/i.php?page=videos/bsidescharm2019/1-06-how-to-start-a-cyber-war-lessons-from-brussels-chris-kubecka)
		* A sanitized peek behind the diplomatic curtain, revealing challenges, decisions & tools at their disposal. The Vanguard cyber warfare exercises in Brussels involving EU & NATO member states. Nation-states leveraging software, hardware and human vulnerabilities into digital warfare, with devastating consequences. Embassy threats, leaked Intel agency tools, hacking back & mass casualties.
	* [Embrace the Red: Enhancing detection capabilities with adversary simulation - Mauricio Velazco(BSidesCharm 2019)](https://www.irongeek.com/i.php?page=videos/bsidescharm2019/1-01-embrace-the-red-enhancing-detection-capabilities-with-adversary-simulation-mauricio-velazco)
		* Executing adversary simulations in properly monitored environments allows defenders to test and enhance their detection capabilities. Unfortunately, red & purple team engagements cannot be executed too often. This talk will describe the benefits of blue team led simulations by dissecting common red team techniques, show how they can be detected and release a new tool to simulate them.
	* [Adversary Emulation and Red Team Exercises - Jorge Orchilles(2020)](https://www.youtube.com/watch?v=LOv7D384CiI)
		* [Slides](https://www.slideshare.net/jorgeorchilles/adversary-emulation-and-red-team-exercises-educause/)
	* [When Worlds Collide: OSS Hunting & Adversarial Simulation | BHIS & Friends(2020)](https://www.youtube.com/watch?v=P2v-fq3JxDg)
		* The group will discuss Roberto Rodriguez (@Cyb3rWard0g) and Nate Guagenti’s (@neu5ron) development and maintenance of the HELK project while focusing on the ongoing development of Mordor, Datasets, and Azure Resource Manager templates. Joining the world-class hunters is Marcello Salvati (Byt3bl33d3r), developer of CrackMapExec and SILENTTRINITY to continue the discussion of OSS adversarial simulation. John Strand will add commentary on the history of adversarial simulation, hunting, and where the industry may be headed.
	* [Cuddling the Cozy Bear, Emulating APT29 - Jorge OrchillesCyber Junegle DEF CON Red Team Village2020)](https://www.youtube.com/watch?v=Fa4GHF_OVVc&list=PLruly0ngXhPGvyl-gOp4d_TvIiedloX1l&index=10)
		* In this talk, we will learn about APT29 “Cozy Bear”, how they operate and what their objectives are. We will create an adversary emulation plan using C2 Matrix to pick the best command and control framework that covers the most TTPs. We will spend at least half the talk live demoing the attack with various tools that emulate the adversary behaviors and TTPs.
	* [Attacking Below the Surface - Adversary Emulation - Rod Soto & Jose Hernandez](https://www.youtube.com/watch?v=YEnL8QfFlJI&list=PLruly0ngXhPGvyl-gOp4d_TvIiedloX1l&index=25)
		* Using Splunk Attack Range for simulation testing.
	* [Open Source Adversary Simulation Toolset Review - Ryan Voloch(BSides Pittsburg(2019)](https://www.youtube.com/watch?v=Sm0-YVa5po8)
		* Goals of Presentation are to help the audience: Understand the practical benefits of using Adversary Simulation Toolsets such as gap/maturity assessment, threat hunt validation, and operations testing.; Compare and contrast 4 free Adversary Simulation Toolsets to help select which one(s) are best: Caldera, Metta, Endgame RTA, Atomic Red Team; Be encouraged to use and participate in community development of these free toolsets.
	* [Emulating the Adversary in Post-Exploitation - Jake Williams(SANS HackFest&Ranges Summit2020)](https://www.youtube.com/watch?v=VctxgiEoDUU&list=PLdVJWiil7RxoW8rBeKc0flY8bRuD3M68L&index=5)
		* We all know that non-technical personnel (e.g. managers and executives) struggle to understand the impacts detailed in technical pentest/red team reports. But the same people have no trouble understanding the impact of a data breach. What's the difference? Well, in most red team reports, we focus on system compromise and getting domain admin rather than emulating the adversary and demonstrating what can be done with a compromise. Real attackers aren't interested in complicated exploitation techniques, they just want to get the data that pays the bills. In this talk, we'll discuss how attackers discover relevant data to target so you can more closely emulate your adversary and maximize the value of your next penetration test.
	* [Tradecraft Development in Adversary Simulations - Fatih Ozavci(Defcon29 Adversary Village)](https://www.youtube.com/watch?v=KJsVVEn4fFw)
	* [Look at me, I'm the Adversary now: Intro to Adversary Emulation & Its Place in Security Operations - Samuel Kimmons(2021)](https://www.youtube.com/watch?v=vnr0kijaK60)
		* "Adversary Emulation is quickly becoming a hot topic in information security, and there is a good reason for it. Security analysts, threat hunters, and incident responders are constantly facing an onslaught of old and new threats. How can defenders properly prepare for the ever-changing threat landscape, improve their skill set, and improve the security posture of their organization? In this presentation I'll answer those questions by covering: The various forms of Adversary Emulation, where/how it fits into Security Operations, Threat Intelligence, the benefits of using it as a Blue Team training tool, and how to get started!"
* **Simulation Plans**<a name="advplans"></a>
	* [Unit42 Playbook Viewer](https://pan-unit42.github.io/playbook_viewer/)
	* [Introducing the Adversary Playbook: First up, OilRig - Ryan Olson](https://unit42.paloaltonetworks.com/unit42-introducing-the-adversary-playbook-first-up-oilrig/)
	* [TA505+ Adversary Simulation Resources](https://github.com/fozavci/ta505plus)
		* TA505+ Adversary Simulation
	* [Adversary Emulation Library](https://github.com/center-for-threat-informed-defense/adversary_emulation_library)
		* In collaboration with Center Participants, the Center for Threat-Informed Defense (Center) is building a library of adversary emulation plans to allow organizations to evaluate their defensive capabilities against the real-world threats they face. Emulation plans are an essential component in testing current defenses for organizations that are looking to prioritize their defenses around actual adversary behavior. Focusing our energies on developing a set of common emulation plans that are available to all means that organizations can use their limited time and resources to focus on understanding how their defenses actually fare against real-world threats.
	* [SMUC -- Simplified MITRE Use Cases](https://github.com/karemfaisal/SMUC)
		* This Repo will contains MITRE att&ck use cases and some other attacks.
	* [community-threats](https://github.com/scythe-io/community-threats)
		* The GitHub of Adversary Emulation Plans in JSON. Share SCYTHE threats with the community. #ThreatThursday adversary emulation plans are shared here.
	* [public-threats](https://github.com/Manticore-Platform/public-threats)
		* Manticore's Public Threats Repository
	* [attack-arsenal](https://github.com/mitre-attack/attack-arsenal)
		* A collection of red team and adversary emulation resources developed and released by MITRE. 
* **Tools**<a name="advtools"></a>
	* [Manticore Adversary Emulation Client Tool](https://github.com/Manticore-Platform/manticore-cli)
		* Manticore Adversary Emulation Cli
	* [Emulate.GO](https://github.com/Haydz/Emulate.GO)
		* A tool to abstract away the complexity of executing command line indicators in adversary emulation.
	* [Operator](https://github.com/preludeorg/operator-support)
		* Operator: an autonomous red team command-and-control platform to make security testing more accessible.
	* [PetaQ](https://github.com/fozavci/petaqc2)
		* PetaQ is a malware which is being developed in .NET Core/Framework to use websockets as Command & Control (C2) channels. It's designed to provide a Proof of Concept (PoC) websocket malware to the adversary simulation exercises (Red & Purple Team exercises).
------------------------------------------------------------------------------------------------------------------------------





































-----------------------------------------------------------------------------------------------------------------------------
### <a name="aptdata"></a> Advanced Persistent Threat Actors & Campaigns
* **101**
	* [APTnotes](https://github.com/aptnotes/data)
		* APTnotes is a repository of publicly-available papers and blogs (sorted by year) related to malicious campaigns/activity/software that have been associated with vendor-defined APT (Advanced Persistent Threat) groups and/or tool-sets.
	* [APT Groups and Operations](https://docs.google.com/spreadsheets/d/1H9_xaxQHpWaa4O_Son4Gx0YOIzlcBWMsdvePFX68EKU/edit?usp=sharing)
* **Articles/Blogposts/Writeups**
* **Talks/Presentations/Videos**
	* [From Hacking Team to Hacked Team to…? - Filip Kafla(NorthSec2018)](https://www.youtube.com/watch?v=wkkBcspGLUg)
		* Hacking Team came into the spotlight of the security industry following its damaging data breach in July 2015. The leaked data revealed several 0-day exploits being used and sold to governments, and confirmed Hacking Team’s suspected business with oppressive regimes. But what happened to Hacking Team after one of the most famous hacks of recent years?  Hacking Team’s flagship product, the Remote Control System (RCS), was detected in the wild in the beginning of 2018 in fourteen countries, including those contributing to previous criticism of the company’s practices. We will present the evidence that convinced us that the new post-hack Hacking Team samples can be traced back to a single group – not just any group – but Hacking Team’s developers themselves.  Furthermore, we intend to share previously undisclosed insights into Hacking Team’s post-leak operations, including the targeting of diplomats in Africa, uncover digital certificates used to sign the malware, and share details of the distribution vectors used to target the victims. We will compare the functionality of the post-leak samples to that in the leaked source code. To help other security researchers we’ll provide tips on how to efficiently extract details from these newer VMProtect-packed RCS samples. Finally, we will show how Hacking Team sets up companies and purchases certificates for them.
* **Specific Campaigns/Groups/Operations**<a name="aptcamp"></a>
	* **Articles/Blogposts/Writeups**
	* **Talks/Presentations/Videos**
	* **Equation Group**
		* **Talks/Presentations/Videos**
			* [DanderSpritz: How the Equation Group's 2013 tools pwn in 2018 - Francisco Donoso(THOTCON9)](https://speakerdeck.com/francisck/thotcon-9-danderspritz-how-the-equation-groups-2013-tools-pwn-in-2018)
			* [Killsuit the equation group's swiss army knife for persistence - Francisco J Donoso, Randori(BlueHatv18)](https://www.youtube.com/watch?v=R5mgAsd2VBM)
				* [Slides](https://www.slideshare.net/MSbluehat/bluehat-v18-killsuit-the-equation-groups-swiss-army-knife-for-persistence-evasion-and-data-exfil)
------------------------------------------------------------------------------------------------------------------------------






























	
	
	
	
	
	


-----------------------------------------------------------------------------------------------------------------------------
### Building a (Red) Team<a name="dreamteam"></a>
* **101**<a name="team101"></a>
	* [The Four Phases of Offensive Security Teams - Mubix(2020)](https://malicious.link/post/2020/four-phases-of-offsec/)
* **Non-Red Team Team Building**
	* I'm of the opinion that teams are built from mutual understanding and trust. I believe that the following exercises help foster and expose these to the participating groups in a non-forced, optional manner that does not feel 'artificial'. Shoutout to Sean F. for his advice. Thanks again for that. :D
	* **Articles**
		* [Build Your Creative Confidence: The Wallet Exercise - Tom Kelley(2019)](https://www.ideo.com/blog/build-your-creative-confidence-the-wallet-exercise)
		* [Stuck in a rut? An exercise on how to be an out-of-the-box thinker - Jason Zook](https://thenextweb.com/entrepreneur/2014/06/05/stuck-rut-exercise-box-thinker/)
		* [How to run a Design Thinking workshop : Design A Wallet Challenge - Valerie Gan(2019)](https://uxplanet.org/design-thinking-is-for-everyone-design-a-wallet-challenge-80422329e83d?gi=3e2787b82253)
		* [Design Thinking 101: Design the Ideal Wallet - teachingentrepreneurship.org(2019)](https://www.teachingentrepreneurship.org/design-thinking-101/)
		* [Design Thinking: The Ideal Wallet [Online Version] - teachingentrepreneurship.org(2021)](https://www.teachingentrepreneurship.org/design-thinking/)
		* [Wallet Exercise in different Languages - Stanford.edu](https://dschool.stanford.edu/resources/the-gift-giving-project)
		* [Learn How to Use the Best Ideation Methods: Worst Possible Idea - by Rikke Friis Dam, Teo Yu Siang](https://www.interaction-design.org/literature/article/learn-how-to-use-the-best-ideation-methods-worst-possible-idea)
		* [Bad Idea Brainstorm - Korey Kostek(2017)](https://medium.com/@koreykostek/bad-idea-brainstorm-46f6f6d72e36)
		* [3 Creative Exercises to Kickstart a Killer Ideation Session - Tommy Campbell(2016)](https://medium.com/@tommycampbell/3-creative-exercises-to-kickstart-a-killer-ideation-session-7c5b3fb57b6e)
* **Articles/Blogposts/Writeups**<a name="teamart"></a>
	* [So You Want a Red Team: The Primer - Jerry Odegaard(2019)](https://whiteoaksecurity.com/blog/2019/6/27/so-you-want-a-red-team-the-primer)
	* [Adversary Mindset and Kobayashi Maru Exericse - P. Boonyakarn](https://pandora.sh/posts/adversary-mindset-and-kobayashi-maru-exericse/)
	* [Embracing the Kobayashi Maru:  Why You Should Teach Your Students to Cheat - Gregory Conti and James Caroland](http://www.rumint.org/gregconti/publications/KobayashiMaru_PrePub.pdf?fbclid=IwAR0SSUwpxCwxw25bHyL4GfXpRPCr6fcneJGigjMpfx3S4iFdhIa26-eiqLc)
		* This article describes our experiences in helping students develop an adversary mindset byadopting the Kobayashi Maru training exercise employed in the fictional Star Trek universe.  Inthe Kobayashi Maru exercise, Starfleet cadets were faced with a no-win scenario -- attempt torescue the crew of a disabled civilian vessel, and be destroyed in the effort, or avoidconfrontation and leave the disabled ship and its crew to be captured or destroyed.  Famously,Captain Kirk won the scenario by, and this is important, stepping outside the game and alteringits rules to his benefit.  By deciding to cheat and altering the programming of the ArtificialIntelligence driving the exercise, he won the contest. Lest there be any misunderstanding, our purpose with this article is not to encourage or teachstudents to cheat in general, but to learn to think creatively when considering adversarybehavior.
	* [How to Create an Internal/Corporate Red Team - Tim MalcomVetter(20202)](https://malcomvetter.medium.com/how-to-create-an-internal-corporate-red-team-1023027ea1e3)
	* [Zero to Hero – Building a Red Team - Robert Neel & David Thompson](http://penconsultants.com/blog/presentation-zero-to-hero-building-a-red-team/)
	* [Some Lessons Learned from Building Red Agents in the RAND Strategy Assessment System (RSAS) - Paul K Davis(1989)](https://www.rand.org/content/dam/rand/pubs/notes/2007/N3003.pdf)
		* This Note contains the text of an oral presentation delivered to the third "Thinking Red in War Games" workshop held at the National Defense University in June 1988. The work underlying the presentation was accomplished in the RAND Strategy Assesment Center (RSAC), which the author directs.
* **Talks/Presentations/Videos**<a name="teamtalks"></a>
	* [Red white and blue. Making sense of Red Teaming for good. - Ian Amit(Derbycon2014)](https://www.irongeek.com/i.php?page=videos/derbycon4/t209-red-white-and-blue-making-sense-of-red-teaming-for-good-ian-amit)
		* Say red team one more time. I dare you. I double dare you. The term red team has been recently more abused than cyber. And it’s making us all hurt in ways we need dolls to point where the bad man touched us. Time to get back to business: In this talk we’ll get down and dirty on how a company can actually see a benefit from red teaming. Beyond the red team having fun and bragging rights. Actual ROI. Dirty business speak... We’ll explore some recent examples of implementing red team engagements along with good ol’e blue work, cutting the fat in the security practice of companies, and getting actionable work done.
	* [Spy Vs. Spy: How to Use Breakable Dependencies to Your Advantage - Stacey Banks, Anne Henmi(Derbycon2015)](https://www.irongeek.com/i.php?page=videos/derbycon5/stable35-spy-vs-spy-how-to-use-breakable-dependencies-to-your-advantage-stacey-banks-anne-henmi)
		* When a dependency comes along can you break it? Break it good? The reliance on third-party applications can unleash a dependency hell upon your network. How well do you trust the integrity of third party integrations that affect your code, your systems, and any COTS/GOTS you purchase? We will take a look at vulnerabilities that have been exploited and how they broke the perceived security of the network. Looking at the flaws in the trust chain we can see where the weaknesses are introduced and begin to devise ways to exploit them. When you're leveraging third party applications, and everyone is, you have to ask yourself `‰ÛÏDo I feel lucky?‰Û. Well, do ya, punk?`
	* [Embrace the Bogeyman: Tactical Fear Mongering for Those Who Penetrate - FuzzyNop(Derbycon2016)](https://www.irongeek.com/i.php?page=videos/derbycon6/114-embrace-the-bogeyman-tactical-fear-mongering-for-those-who-penetrate-fuzzynop)
		* When it comes to cyber penetration, evolving threat landscapes mandate advanced persistent tac. ha ha, just kidding. Look, let's be real, as an internal red team things can get really weird. A day job carrying out a company?s most apocalyptic self-destructive fantasies presents a strange duality of helping and hurting. General public and corporate fear of 'hackers' has been both a blessing and a curse. You might say it?s a gray area, but is it really that simple? In this talk i'll share the ups, downs, and lessons learned during my adventures as the corporate bogeyman.
	* [The Art of War, Attacking the Organization and Raising the Defense - Jeremy Mio, David Lauer, Mike Woolard(Derbycon2016)](https://www.irongeek.com/i.php?page=videos/derbycon6/408-the-art-of-war-attacking-the-organization-and-raising-the-defense-jeremy-mio-david-lauer-mike-woolard)
		* The most effective way into an organization, cute cat pictures and free tickets to DerbyCon... the easiest and quickest way into an organization, attacking the weakest link, humans. There are many campaigns in the wild conveying "Cyber Security" being a shared responsibility across the organization, but how can we expect that when we do not prepare our fellow employees? We need to properly prepare our employees, managers, technical folk, and even the Executives for the security battle ground. Militaries do not train their generals, sergeants, and ground soldiers with the same material and techniques, and neither should we for security awareness training. Join us and an old friend, Sun Tzu, to prepare the war and battles we are facing from all sides of our organization.
	* [Planning Effective Red Team Exercises - Sean T Malone - BSidesSF2016](https://www.youtube.com/watch?v=cD-jKBfSKP4)
		* An effective red team exercise is substantially different from a penetration test, and it should be chartered differently as well. The scenario, objective, scope, and rules of engagement all need to be positioned correctly at the beginning in order to most closely simulate a real adversary and provide maximum value to the client.In this presentation, we'll review best practices in each of these areas, distilled from conducting dozens of successful red team exercises - along with some war stories highlighting why each element matters. Those in offensive security will gain an understanding of how to manage the client's expectations for this process, and how to guide them towards an engagement that provides a realistic measurement of their ability to prevent, detect, and respond to real attacks. Those in enterprise security will gain a deeper understanding of this style of assessment, and how to work with a red team to drive real improvement in their security programs.
	* [Building A Successful Internal Adversarial Simulation Team - C. Gates & C. Nickerson - BruCON 0x08(2016)](https://www.youtube.com/watch?v=Q5Fu6AvXi_A&list=PLtb1FJdVWjUfCe1Vcj67PG5Px8u1VY3YD&index=1)
	* [Some Teams Are Red, Others Are Blue, But Purple Ones Are the Best Value Prajakta Jagda(SHELLCON 2017)](https://www.youtube.com/watch?v=115w1Z9MMA4&list=PL7D3STHEa66R0nWbixrTo3O7haiMmA71T&index=6)
		* How does one build an enterprise red team from scratch? That was the question I faced a year ago when I accepted the lead red team engineer role at Palo Alto Networks. The most apparent lesson for me has been that red teaming as an internal enterprise function draws an interpretation that is quite different from the one generally accepted by the industry. Over the last year, I have had to set aside everything I thought I knew about red teaming and build an approach that offered the value proposition an enterprise is looking for from such a function. In the first part of this session, I want to touch upon the lessons I have learned during my journey to build a red team program. I want to share my thoughts on the philosophy and approach that is most likely to benefit an enterprise program like this. While this might seem very academic, this has governed every single tactical piece the team has had to implement to make the program a success. Not only has the team composition and interactions been heavily governed by the approach, we have also built custom tools and frameworks to operationalize it. The success we have seen so far is what has prompted me to share highlights of the program with a wider audience. Hopefully, I can help someone else struggling with the same question I faced above. The story, however, doesn’t end there, because building a red team program was only half the battle. I’m sure at least some of the attendees have read (with or without scoffing) about the purple teaming movement. While, in theory, it absolutely should resonate with any enterprise security engineer, putting it in practice is a different matter. The second part of the session will focus on approaches and mechanisms to adopt purple teaming. By the end of this session, the audience should expect to walk away with concrete ideas on approaches to implementing enterprise red team and purple team programs.
	* [Let's Create A Redteam Mission - Alex Kouzmine - BlackAlps 2018](https://www.youtube.com/watch?v=-kK8K-UVhWY)
	* [Red Teaming gaps and musings - Samuel Sayan(Derbycon2018)](https://www.irongeek.com/i.php?page=videos/derbycon8/stable-00-red-teaming-gaps-and-musings-samuel-sayen)
		* Red Teaming is currently the closest most companies get to adversary emulation. While Red Teaming can do a good job pointing out security gaps, blind spots, and human weaknesses within an organization, there are also limitations. Engagement SOW’s, timelines, and laws impose limitations which can unwittingly push a Red Team engagement far from adversary emulation. Some thoughts on the current status quo, and ways to mix it up.
	* [Red vs Blue and why We are doing it wrong - Chris Roberts(BSides Chattanooga 2018)](https://www.irongeek.com/i.php?page=videos/bsideschattanooga2018/100-red-vs-blue-and-why-we-are-doing-it-wrong-chris-roberts)
		* Leave your 0days, leave your latest hacks behind AND bring your playbook for the blue team. We have more hacks and more works, trojans and attack vectors than we know what to do with, therefore what DO we actually do with them, THAT IS the question on the "tech behind" track'this is not about how you attach it is ALL about how you defend. What happens when the midden hits the fan, how and where and why do you react, how do you even know that you have been hacked? As security we have failed our very charges, we continue to allow them to be attacked and we fail at defense, therefore bring your BEST technical minds and apply them to how we better protect those that rely upon us.
	* [Building and Leading Corporate Red Teams - Dale Pearson(x33fcon 2018)](https://www.youtube.com/watch?v=2kWMIffjNXI)
		* Red Teaming often means different things to different people, so in this talk Dale shares with you what he believes to be Red Teaming in the Corporate world, what to be the foundational elements of establishing the support and buy in to put together an effective adversarial emulation capability, and how to lead it to success and evolve the capability over time.
	* [Blue Blood Injection: Transitioning Red to Purple - Lsly Ayyy(Derbycon2018)](https://www.irongeek.com/i.php?page=videos/derbycon8/stable-35-blue-blood-injection-transitioning-red-to-purple-lsly-ayyy)
		* Moving from a large company with a retinue of pentesters, to a start-up with far fewer resources, can be a strain. It may be just you. While you're performing services, your new company may also need you to be flexible -- move to supporting some IR or blue team-related functionality. You won't be able to do both sides of a purple team, but you can help things meet for your clients. This talk will have my story, as well as some ideas when having to reach across a spectrum of needs with limited (or no) defense-focused personnel.
	* [Why your red team shouldn't be snowflakes - Isaiah Sarju(ShowMeCon2019)](https://www.irongeek.com/i.php?page=videos/showmecon2019/showmecon-2019-15-why-your-red-team-shouldnt-be-snowflakes-isaiah-sarju)
		* Red teaming requires the use of specialized tools. However, this should not exclude operators from using the same technology, adhering to the same procedures, and following the same policies as their colleagues throughout the organization. Some argue that this will prevent operators from executing on their duties. The contrary is true. With a few exceptions in place and thoughtful architecture considerations, treating red teamers as regular employees will improve their testing and reduce the risk that red teamers bring to organizations.
	* [Five phases of IRTOF: Kickstarting your organization's Red Team Operations programme - Abhijith B R(BSides Delhi 2020)](https://www.youtube.com/watch?v=AThBgIE3cEI)
		* [Slides](https://tacticaladversary.io/slides/Internal-Red-Team-BSides-Delhi-2020-Abhijith-b-r.pdf)
		* This talk is about building a practical internal #redteam​. This is not an easy task. For organizations, it is essential to have an internal offensive team to continuously perform adversarial simulation to strengthen the security posture and enhance blue team capabilities. Many variables needs to be taken care of before going forward with such an initiative. Most important thing would be assessing the progress and maturity of the red team building process. Explains various steps to create an internal offensive team/red team from scratch and increasing the capabilities gradually on different phases. This talk introduces a proven way of building internal offensive teams, Internal Red Team Operations Framework. (IRTOF)
	* [How To Build A High-Performing Red Team - Tom Porter & Patrick Fussell(WWHF 2020 Virtual)](https://www.youtube.com/watch?v=fSLxkDQiVsc)
		* What are the habits of a highly successful red team? How much do TTPs or a team’s talent level contribute to their overall effectiveness? This talk will examine the actions that separate high-performing red teams from the competition. The speakers will share practical red team methods developed through their careers as offensive security consultants, along with insights from leaders in the infosec industry. They’ll connect observations from recent publications on the topic with the lessons learned from their previous careers on other high-performing, high-stress teams -- one as a Marine and the other as a professional baseball player.  This talk will highlight how effective teams are architected, the challenges of remote work, engagement planning and execution, practical tips for effective communication, and the importance of team cohesion when pursuing a mission. Attendees will walk away with action items they can take back to their organizations and start implementing immediately.
* **Increasing the Size/Maturity Of**
	* **Talks/Presentations/Videos**
		* [Illusion of Control: Capability Maturity Models and Red Teaming - Johann Rehberger(2020)](https://embracethered.com/blog/posts/2020/capability-maturity-model-test-red-teaming/)
		https://www.tmmi.org/tmmi-model/
		* [Guerrilla Red Team: Decentralize the Adversary - Christopher Cottrell(RedTeamVillage)](https://www.youtube.com/watch?v=bgvKQF0oNoA&feature=share)
			* "Guerrilla Red Team is a methodology by which a company can grow security IQ, technical expertise, and security brainpower, resulting in an internal mesh network of trusted decentralized ethical hackers. The program requires minimal capital investment from the hosting red team. It achieves its primary goals through weekly group mentorship hosted during a four-hour block, once per week, during the workday. It forms a peer network in which guerrilla operators share ideas and techniques, and ultimately grow technically and professionally as a unit. Members of the program come from various technical disciplines, but not necessarily security-focused verticals. The cohort of five to six members follows a nine-week syllabus that takes them from someone with minimal red team experience to autonomous operations. Guerrilla Operators will have a regular cadence of operations, which will require deconfliction from the parent red team to only ensure there are no safety concerns with the proposed target. Expected outcomes for the nine-week cohort are as follows: Guerrilla operators are armed with the skills to continue their red team learning, as well as a support network for challenging tasks The parent red team has an expanded network of internal, trusted, ethical hackers. This strengthens idea generation for campaigns, and enables communication through the use of a shared and common technical language. Over time, the Guerrilla Red Team provides a steady flow of trained homegrown red team operators or security analysts The company itself benefits by having security-focused mindsets placed throughout technical disciplines, resulting in staff that are poised to ward off attacks by thinking like an attacker, functioning similarly to security-focused Site Reliability Engineers (SRE) Provides the company with verification that their security program and infrastructure are as robust as they say it is through the use of decentralized, independent low-tier actors attacking the network: an Offsec ChaosMonkey Provides the guerrilla operators real world, hands on experience in a career field that is hard to break into outside of the Federal pipeline "
----------------------------------------------------------------------------------------------------------------










----------------------------------------------------------------------------------------------------------------
### <a name="engagered"></a>Organizing a Red Team Engagement
* **Facilitating a Red Team Engagement**<a name="farte"></a>
	* **Defining Rules of Engagement**
		* [Sanremo Handbook on Rules of Engagement - iihl.org](http://iihl.org/sanremo-handbook-rules-engagement/)
			* The Sanremo Handbook on the Rules of Engagement (RoE), published in November 2009, represents the only work of this type which sets out to explain in a practical way the complex procedures and methodology governing the development and implementation of Rules of Engagement. It has been translated into the 6 official languages of the United Nations as well as Bosnian, Hungarian and Thai.
	* **Articles/Blogposts/Writeups**
		* [Cyber Exercise  Playbook - MITRE](https://www.mitre.org/sites/default/files/publications/pr_14-3929-cyber-exercise-playbook.pdf)
		* [Planning a Red Team exercise](https://github.com/magoo/redteam-plan)
		* [So You Want to Run a Red Team Operation](https://medium.com/@prsecurity_/how-to-build-an-internal-red-team-7957ec644695)
		* [Red Team Development and Operations: A Practical Guide](https://redteam.guide)
			* [Supporting Documents](https://redteam.guide/docs/)
		* [Red Team Tradecraft and TTP Guidance - Threatexpress](http://threatexpress.com/redteaming/redteamplanning/tradecraft/)
		* [High Value Adversary Emulations via In Person Purple Team Exercises - Jorge Orchilles(2020)](https://www.youtube.com/watch?v=Ard7c-79X84)
			* [Slides](https://www.slideshare.net/jorgeorchilles/purple-team-work-it-out-organizing-effective-adversary-emulation-exercises)
		* [Purple Team - Work it out: Organizing Effective Adversary Emulation Exercises - Jorge Orchilles(2020)](https://www.slideshare.net/jorgeorchilles/purple-team-work-it-out-organizing-effective-adversary-emulation-exercises)
		* [How to Build a Red Teaming Attack Scenario | Part 1 - Bypass Security Controls - Barış Akkaya & Süleyman Özarslan(2020)](https://www.picussecurity.com/resource/blog/how-to-build-a-red-teaming-attack-scenario-part-1)
			* [Part 2](https://www.picussecurity.com/resource/blog/how-to-build-a-red-teaming-attack-scenario-part-2)
	* **Talks/Presentations/Videos**
		* [Planning & Executing A Red Team Engagement - Tim Wright(OISF2018)](https://www.irongeek.com/i.php?page=videos/oisf2018/oisf-2018-05-planning-executing-a-red-team-engagement-tim-wright)
* **Methodologies & Frameworks**<a name="advmethods"></a>
	* **Methodologies**
		* [A Hands-On Introduction to Mandiant's Approach to OT Red Teaming - Mark Heekin, Daniel Kapellmann Zafra, Nathan Brubaker, Ken Proska, Rob Caldwell(2020)](https://www.fireeye.com/blog/threat-research/2020/08/hands-on-introduction-to-mandiant-approach-to-ot-red-teaming.html)
		* [A Journey Into a Red Team - Charles Hamilton(2018)](https://ringzer0team.com/d/A-Journey-Into-a-RedTeam-2018.pdf)
		* [Red Team Methodology A Naked Look Jason Lang(Derbycon2019)](https://www.youtube.com/watch?v=kf829-tm0VM)
			* [Slides](https://www.slideshare.net/JasonLang1/red-team-methodology-a-naked-look-169879355)
	* **Frameworks**
		* [TIBER-EU Framework - How to implement the European framework for Threat Intelligence-based Ethical Red Teaming](https://www.ecb.europa.eu/pub/pdf/other/ecb.tiber_eu_framework.en.pdf)
		* [TIBER - NL Guide - How to conduct the TIBER-NL test](https://www.dnb.nl/binaries/TIBER-NL%20Guide%20Second%20Test%20Round%20final_tcm46-365448.pdf)
		* [TIBER-EU Framework: Services Procurement Guide(European Central Bank)](https://www.ecb.europa.eu/pub/pdf/other/ecb.1808tiber_eu_framework.en.pdf)
		* [CREST Penetration Testing Procurement Guide v1.0](https://www.crest-approved.org/wp-content/uploads/PenTest-Procurement-Guide.pdf)
		* [CBEST Intelligence-Led Testing: CBEST Implementation Guide v2.0 - Bank of England](https://www.bankofengland.co.uk/-/media/boe/files/financial-stability/financial-sector-continuity/cbest-implementation-guide)
		* [Purple Team Exercise Framework - Scythe](https://github.com/scythe-io/purple-team-exercise-framework)
		* [Cyber Operational Resilience Intelligence-led Exercises (CORIE) - Council of Financial Regulators(2020)](https://www.cfr.gov.au/publications/policy-statements-and-other-reports/2020/corie-pilot-program-guideline/pdf/corie-framework-guideline.pdf)
			* [Article](https://www.cfr.gov.au/news/2020/mr-20-06.html)
			* "CORIE is a pilot program of exercises aiming to assess a financial institution’s cyber resilience. These exercises use intelligence gathered on adversaries, to simulate their modes of operation. Threat intelligence-led exercises aim to assess the overall maturity of a financial institution’s cyber defence and response capability"
* **Improving**
	* **Talks/Presentations/Videos**
		* [Red Team Engagement Guide: How an Organization Should React - Jason Lang(2019)](https://www.trustedsec.com/blog/red-team-engagement-guide-how-an-organization-should-react/)
		* [OPSEC Obsessed - Jake Kamieniak(x33fcon2020)](https://www.youtube.com/watch?v=KdgUec9pU9U&list=PL7ZDZo2Xu330gMHAoeGvH9QkCJMC-qgeK&index=18)
			* Red Teams can be obsessed with OPSEC because it enables us to deliver impactful results. However, when operational security becomes unchecked secrecy, it can confuse or even offend our peers. A security organization that trusts and understands each other will perform better. If you have ever been asked “Why can’t you just tell me your TTPs?” this talk will help you explain the whats, whys, and whens of OPSEC and help you evaluate when to let others in on your closely guarded secrets. Instead of discussing tips and tricks to hack better, this talk aims to shed light on an area of Red Teaming that walks the line between strategy and the Red to Blue relationship. How does OPSEC enable Red Teams to deliver a more useful assessment? There are Common questions that Red Teams deflect answering, citing OPSEC. This talk will challenge your response to these questions, asking where OPSEC is helping or hurting your specific security mission, and help you justify and explain your decisions. Learn from the real triumphs and pitfalls of GE's Red Team’s experience to improve your own OPSEC strategy.
* **Metrics & Models**<a name="gmm"></a>
	* **Reference**
		* [A Red Team Maturity Model - redteams.fyi](https://redteams.fyi/)
			* A model to reference when gauging Red Team maturity, as well as set goals and provide guidance when building internal Red Teams.
	* **Articles/Blogposts/Writeups**
		* [Measuring a red team or penetration test. - Ryan McGeehan(2018)](https://medium.com/starting-up-security/measuring-a-red-team-or-penetration-test-44ea373e5089)
		* [Helpful Red Team Operation Metrics - Cedric Owens(2020)](https://medium.com/red-teaming-with-a-blue-team-mentaility/helpful-red-team-operation-metrics-fabe5e74c4ac)
		* [Gamifying Security with Red Team Scores - wunderwuzzi(2021)](https://embracethered.com/blog/posts/2021/gamifying-red-team-security-score/)
- **Purple Teaming**<a name="purple"></a>
	- **Articles/Blogposts/Writeups**
		* [Enterprise Purple Teaming](https://github.com/ch33r10/EnterprisePurpleTeaming)
			* Collection of resources
		* [Atomic Purple Team Framework and LifeCycle](https://github.com/DefensiveOrigins/AtomicPurpleTeam)
			* The Atomic Purple Team Framework and Lifecycle is a business/organizational concept designed to assist organizations in building, deploying, maintaining, and justying Attack-Detect-Defend Information Security Exercises.		
		* [Copy pasting the copy-paste adversary for ̶l̶u̶l̶z̶ science. - Bitst0rm(2020)](https://medium.com/@b1tst0rm/copy-pasting-the-copy-paste-adversary-for-%CC%B6l%CC%B6u%CC%B6l%CC%B6z%CC%B6-science-7e3efecb389d)
		* [Welcome to the Emulating like a champ: Emulating the latest Buer Loader Workshop! - ](https://jfmaes-1.gitbook.io/emulate-like-a-champ-emulating-the-latest-buer-cam/)
		* [Attack automation with Metasploit tasks - Dawid Golak(2020)](https://medium.com/@dawid.golak/attack-automation-with-metasploit-tasks-c389a4c2e3a6)
		* [An introduction to Purple Teaming - Bridewell Consulting(2020)](https://www.bridewellconsulting.com/an-introduction-to-purple-teaming)
		* [Purple Maturity Model - Tim Schulz(2021)](https://raw.githubusercontent.com/tim-scythe/conference-materials/master/SANS-PurpleTeamSummit-2021/Purple%20Maturity%20Model.pdf)
		* [Purple is the new red - David Hunt(2021)](https://feed.prelude.org/p/purple-is-the-new-red)
		* [Is This Thing On? How to make sure your antivirus is working without any malware - Michael Allen(2021)](https://www.blackhillsinfosec.com/is-this-thing-on/)
		* [Scythe Threat Thursday Blogposts](https://www.scythe.io/threatthursday)
	- **Papers**
		* [The Unified Kill Chain: Designing a Unified Kill Chain for analyzing, comparing and defending against cyber attacks - Mr. drs. Paul Pols(2017)](https://www.csacademy.nl/images/scripties/2018/Paul-Pols---The-Unified-Kill-Chain.pdf)
			* "In this thesis,a Unified Kill Chain(UKC)modelis developedthat focuses on the tactics that form the consecutive phases of cyber attacks(Table 1). Ahybrid research approach is used to develop the UKC,combiningdesign science with qualitative research methods. The UKC is first developed through literature study, extendingthe CKC by uniting improvements that were previously proposed by other authors withthe tactics of MITRE’s ATT&CK™model. The UKC is subsequently iteratively evaluatedand improved through case studies of attacksby Fox-IT’s Red Team and APT28(alias Fancy Bear). The resulting UKC is a meta model that supports the development of end-to-end attack specific kill chains and actor specific kill chains, that can subsequently be analyzed, compared and defended against."
	- **Talks/Presentations/Videos**
		* [Purple Team: Exposed - Mary Sawyer(ShellCon2018)](https://www.youtube.com/watch?v=Mkh5cSnunrI&list=PL7D3STHEa66TbZwq9w3S2qWzoJeNo3YYN&index=15)
			* Are you looking to rapidly improve your security posture or train a new member of your security organization? Are you a Blue Team member looking to cross train with Red Team or vice versa? Purple Teaming could be the answer to your problems. You may have already heard about Purple Teaming through a spare think piece online, casual mentions or even rage tweets, but few know what makes a Purple Team. In this talk I will cover how to build your own Purple Team function from the ground up using applied gap analysis, creating meaningful test cases, modifying tools, cross-training possibilities, and automation frameworks. We'll walk through the methodology together so you leave with the tools and experience you need to do it yourself. If implemented, this can give you a better knowledge of your security baseline, improvements in defenses, opportunities for internal training and mentorship, and an increased dialogue between Red and Blue.
		* [ATAT: How to take on the entire rebellion with 2-3 stormtroopers - ll3nigmall(ShowMeCon2018)](https://www.irongeek.com/i.php?page=videos/showmecon2018/showmecon-2018-track-3-02-atat-how-to-take-on-the-entire-rebellion-with-2-3-stormtroopers-ll3nigmall)
			* This talk is about the Attack Team Automation Tool (ATAT). ll3nigmall wrote this tool to create repeatability and increase efficiency in large scale penetration tests. Are you feeling Vader's impending choke hold when large scopes are handed down with numerous targets and a large number of duplicate exploits to be handled across several disparate targets? Do you receive incomplete vulnerability reports from Qua..I mean, your vulnerability scanners that require you to identify which port each target has the identified service running on? Does your team have to accomplish high volume and high value repeatable penetration tests with industry standard tools at a fraction of the time it would normally take? If the answer to any of these questions is yes, maybe, or just a defeated; then it is time to fire up your brand new ATAT and charge those shield generators like Greedo in a speedo! Yeah, I'm not really sure what that last line was supposed to mean either. Just git clone ATAT. You'll see what I mean! :)
		* [A Practical Approach to Purple Teaming - Matt Thelen(ShowMeCon 2019)](https://www.irongeek.com/i.php?page=videos/showmecon2019/showmecon-2019-00-a-practical-approach-to-purple-teaming-matt-thelen)
			* To get the most out of your red and blue teams and to improve detection and response capabilities, give them a common goal; ensuring a company's controls are effective and working as intended, AKA Purple Teaming. I will cover the benefits of this approach. I will walk you through some of the early challenges we faced and how we overcame these. How we leveraged the MITRE ATT&CK Framework to establish a common language and approach as well as how we measured success through each engagement.
		* [Executing Purple Team Exercises - Madhav Bhatt(2019)](https://desi-jarvis.medium.com/executing-purple-team-exercises-8629ab9e4a4d)
		* [Sharpen your Simulation Game Part 1 - Introduction - Mauricio Velazco(2020)](https://medium.com/threat-hunters-forge/sharpen-your-simulation-game-part-1-introduction-85d785cda32c)
		* [Structured Purple Team Exercises - Action Dan(2020)](https://lockboxx.blogspot.com/2020/09/structured-purple-team-exercises.html)
		* [Purple Team Candidates for Modern Tech Environments - Cedric Owens(2020)](https://medium.com/red-teaming-with-a-blue-team-mentaility/purple-team-candidates-for-modern-tech-environments-69a78a125d38)
			* This post aims to discuss some decent purple team exercise inputs based on common red team techniques/attack paths along with defensive considerations in modern tech environments. This post is not all encompassing, but looks at some of the most likely attack paths along with some things blue teams can do to help posture for these attack paths (this may be proactive purple team exercise scenarios, hunting, table top exercises, etc.).
		* [Purple Team Exercise Tools - Jorge Orchilles(2020)](https://medium.com/@jorgeorchilles/purple-team-exercise-tools-a85187ce341)
		* [Threat-based Purple Teaming with ATT&CK - Chris and Cody from MITRE(x33fcon 2018)](https://www.youtube.com/watch?v=OYEP-YAKIn0)
			* The days of the IOC are over, and now defenders need to detect the behaviors of an adversary. The best way to do this is for red and blue to operate together in a purple team with many quicker engagements. By leveraging threat intelligence and the common language of ATT&CK, red teams can behave like very specific adversaries while providing a breadth of technique implementations. A successful purple team occurs when red helps blue find gaps in sensing, helps create analytics, and can perform many different implementations of the same behaviors. To share this process and jumpstart others, MITRE is releasing initial ATT&CK emulation plans for APT3 and APT29, complete with adversary MO and a ‘cheat sheet’ of potential commands for red teams.
		* [Exercise Your SOC: How to run an effective SOC response simulation - Brian Andrzejewski(BSidesCharm 2018)](https://www.irongeek.com/i.php?page=videos/bsidescharm2018/track-2-08-exercise-your-soc-how-to-run-an-effective-soc-response-simulation-brian-andrzejewski)
			* Security Operation Centers (SOCs) are the front line for incident detection, response, and escalation for organizations. Few security teams evaluate their SOC's tools, techniques and procedures (TTPs) are working the way they are suppose to for expected SOC response. This talk will cover how Blue and Red teams can build and execute live fire security incidents to target your SOC's TTP abilities to detect, respond, and escalate. Techniques will be discussed in how to develop basic SOC exercise scenarios, determine expected outcomes, measure actual results, and report lessons learned to improve your SOC's ability for TTP execution.
		* [Going Purple: Measurably improving your security posture with Purple Team engagements - Ben0xA(2019)](https://www.trustedsec.com/events/webinar-going-purple-measurably-improving-your-security-posture-with-purple-team-engagements/)
		* [Operationalizing the MITRE ATT&CK Framework - Robert Olson(BSides Cleveland2019)](https://www.irongeek.com/i.php?page=videos/bsidescleveland2019/bsides-cleveland-b-01-operationalizing-the-mitre-attck-framework-robert-olson)
			* The MITRE ATT&CK framework is all the rage these days. Many are looking at this as a research framework that can help standardize many aspects of information security, particularly with respect to offensive methodology. This talk will look at the MITRE ATT&CK framework from a different angle aby examining how the information MITRE has organized can improve penetration testing and, based on preliminary results, defensive posture. I will provide an overview of the ATT&CK framework, discuss the techniques that are useful for penetration testing, and present a case study of homebrew malware written to be aligned with the ATT&CK Framework. The talk will conclude with a discussion of using existing tools aligned with MITRE's ATT&CK Framework for detection and automating analysis of log data generated by those tools. It is important to note that this talk as supported by a significant amount of student work through both undergraduate and graduate capstone projects.
		* [Quickstart Guide to MITRE ATT&CK - Do’s and Don'ts - Adam Mashincho(HackFest Summit 2020)](https://www.youtube.com/watch?v=1tv9hGdzEUA&list=PLdVJWiil7RxoW8rBeKc0flY8bRuD3M68L&index=11&t=0s)
			* Given the increasing awareness and use of the MITRE ATT&CK Matrix as a common language between Red Teams, Blue Teams, and executives, a growing number of organizations are utilizing the framework in inappropriate ways. This talk will provide the audience with a very fast yet very practical overview of ATT&CK, as well as how it is being utilized well and not so well in the industry. From periodic tables to minesweeper, and from CALDERA to Atomic Red Team, we will go over a list of the do’s and don’ts to get the most value from the ATT&CK matrix.
		* [Adversarial Threat Modeling](https://github.com/ssnkhan/adversarial-threat-modelling)
			* Supporting material for my presentation "Adversarial Threat Modelling — A Practical Approach to Purple Teaming in the Enterprise"
		* [ATT&CK Like an Adversary for Defense Hardening - Steve Motts & Christian Kopacsi(Converge2018)](https://www.irongeek.com/i.php?page=videos/converge2018/converge-2018-107-attck-like-an-adversary-for-defense-hardening-steve-motts-christian-kopacsi)
			* Introduction to the MITRE ATT&CK framework, and integration of open-source tools to increase cyber defenses and ensure your Blue Team can detect post-compromise techniques.
		* [Threat-based Purple Teaming with ATT&CK by Chris and Cody from MITRE - x33fcon2018](https://www.youtube.com/watch?v=OYEP-YAKIn0)
			* The days of the IOC are over, and now defenders need to detect the behaviors of an adversary. The best way to do this is for red and blue to operate together in a purple team with many quicker engagements. By leveraging threat intelligence and the common language of ATT&CK, red teams can behave like very specific adversaries while providing a breadth of technique implementations. A successful purple team occurs when red helps blue find gaps in sensing, helps create analytics, and can perform many different implementations of the same behaviors. To share this process and jumpstart others, MITRE is releasing initial ATT&CK emulation plans for APT3 and APT29, complete with adversary MO and a ‘cheat sheet’ of potential commands for red teams.
		* [Adversarial Emulation - Bryson Bort BSidesAugusta2019)](https://www.youtube.com/watch?v=TbX7T6WmrMo&list=PLEJJRQNh3v_PF6cecq0ES2w25JtoG631g&index=21)
		* [Embrace the Red Enhancing detection capabilities with adversary simulation - Mauricio Velazco(BSides Charm2019)](https://www.youtube.com/watch?v=8JFP1wj37Vk)
		* [Automating User Interaction With Sheepl: Soup To Nuts - Matt Lorentzen(44con2019)](https://www.youtube.com/watch?v=ZErvmrP4UCg)
		* [Baselining Behavior Tradecraft through Simulations - Dave Kennedy(WWHF2019)](https://www.youtube.com/watch?v=s19na5Iob6A&list=PLXF21PFPPXTNXEgkUEBbRgvraxWP3c4Hr&index=11)
			* With the adoption of endpoint detection and response tools as well as a higher focus on behavior detection within organizations, when simulating an adversary it's important to understand the systems you are targeting. This talk will focus on the next evolution of red teaming and how defeating defenders will take more work and effort. This is a good thing! It's also proof that working together (red and blue) collectively, we can make our security programs more robust in defending against attacks. This talk will dive into actual simulations where defenders have caught us as well as ways that we have circumvented even some of the best detection programs out there today. Let's dive into baselining behavior and refining our tradecraft to evade detection and how we can use that to make blue better.
		* [SANS Purple Team Summit 2021](https://www.youtube.com/playlist?list=PLdVJWiil7Rxqut7ZVcrzitjorCPcJ-N9I)
		* [Purple Maturity Model - Timothy Schulz(2021)](https://www.youtube.com/watch?v=OAIugoIvpmw)
			* This talk will present an approach to maturing a new purple team from scratch, allowing anyone to chart the path for an internal capability. We will use a multi-level approach to identify the skill sets, people, and processes needed to build a strong purple team. Audiences can expect to walk away with an understanding of where their organization sits in the Purple Maturity Model, and what skills their current blue and red teams can leverage to strengthen the organization’s purple capabilities.
		* [SCYTHE Purple Team Workshop with Tim Schulz Slides](https://www.slideshare.net/jorgeorchilles/scythe-purple-team-workshop-with-tim-schulz)
		* [Becoming a Yogi on Mac ATT&CK with OceanLotus Postures - Cat Self & Adam Pennington(OBTSv4.0/2021)](https://www.youtube.com/watch?v=N_xBbDDycHo)
			* Maybe you've heard about this MITRE ATT&CK® thing, but it’s just for Windows, right? ATT&CK's free knowledge base of adversary behaviors focuses on the real-world tactics, techniques, and procedures seen in actual intrusions, and has quietly covered Macs since 2017. Macs are a unique security space, and we’ll explore what’s unique about ATT&CK for macOS, and the work we’re doing to improve it in 2021. Using OceanLotus's macOS activity as a use case, we’ll walk through how organizations can use ATT&CK as a focal point to improve their threat intelligence, detection analytics, adversary emulation and defensive planning.
		* [Threat Focused Purple Team Exercises (non Active Directory Edition) - Cedric Owens(2021)](https://www.youtube.com/watch?v=DK9ZonIuD0k)
			* This talk will focus on some examples of threat-focused purple team exercises that red and blue teams can collaborate on with the goal of proactively building detections and response procedures for these attack paths. In particular, this talk will focus on useful purple team exercise ideas for modern tech environments that have very few Windows hosts and large numbers of macOS, linux, and cloud hosts. There is a lot more content available that focuses on Windows, so this talk aims to help provide offensive and defensive practitioners with some useful ideas and approaches for the types of environments that exist at most tech companies. By the end of this talk I hope you will be armed with practical ideas for purple team exercises that you can start executing.
		* [Purple Team War Stories - Pepijn Vissers(2021)](https://www.youtube.com/watch?v=6AlZz8shw9c)
		* [Exploitation with Reverse Shell and Infection with PowerShell using VBS - Filipi PIres(HacktivityCon RTV2021)](https://www.youtube.com/watch?v=73f6Jei3W8M)
			* The purpose of this presentation, it was to execute several efficiency and detection tests in our lab environment protected with an endpoint solution, provided by CrowdStrike, this presentation brings the result of the defensive security analysis with an offensive mindset using reverse shell techniques to gain the access inside the victim's machine and after that performing a Malware in VBS to infected the victim machine through use some scripts in PowerShell to call this malware, in our environment bypassing some components and engines, such as: Malware Protection - Associated IOC (Command entered in script), Suspicious Processes, File System Access, Suspicious Processes, Suspicious Scripts and Commands, Intelligence-Sourced Threats, among others..The purpose of this presentation, it was to execute several efficiency and detection tests in our lab environment protected with an endpoint solution, provided by CrowdStrike, this presentation brings the result of the defensive security analysis with an offensive mindset using reverse shell techniques to gain the access inside the victim's machine and after that performing a Malware in VBS to infected the victim machine through use some scripts in PowerShell to call this malware, in our environment bypassing some components and engines, such as: Malware Protection - Associated IOC (Command entered in script), Suspicious Processes, File System Access, Suspicious Processes, Suspicious Scripts and Commands, Intelligence-Sourced Threats, among others..
	* **Tools**
		* [C2 Cradle](https://github.com/cedowens/C2_Cradle)
			* The C2 Cradle is a tool to easily download, install, and start command & control servers (I added C2s that have macOS compatible C2 payloads/clients) as docker containers. The operator is presented with a list of options to choose from and the C2 Cradle will take it from there and download, install, and start the C2 server in a container.
		* [APT Simulator](https://github.com/NextronSystems/APTSimulator)
			* APT Simulator is a Windows Batch script that uses a set of tools and output files to make a system look as if it was compromised. In contrast to other adversary simulation tools, APT Simulator is designed to make the application as simple as possible. You don't need to run a web server, database or any agents on set of virtual machines. Just download the prepared archive, extract and run the contained Batch file as Administrator. Running APT Simulator takes less than a minute of your time.
		* [Fransom](https://github.com/fraktalcyber/Fransom)
			* Fraktal's Ransomware Emulator
		* [RAASNet](https://github.com/leonv024/RAASNet)
			* "This project was made to demonstrate how easy ransomware are easy to make and how it work. The script works on Windows, Linux and MacOS. It is recommended to compile payload.py to EXE format to make it more portable."
		* [Infection Monkey](https://github.com/guardicore/monkey)
			* The Infection Monkey is an open source security tool for testing a data center's resiliency to perimeter breaches and internal server infection. The Monkey uses various methods to self propagate across a data center and reports success to a centralized Monkey Island server.
		* [Network Flight Simulator](https://github.com/alphasoc/flightsim)
			* flightsim is a lightweight utility used to generate malicious network traffic and help security teams to evaluate security controls and network visibility. The tool performs tests to simulate DNS tunneling, DGA traffic, requests to known active C2 destinations, and other suspicious traffic patterns.
		* [Invoke-Apex](https://github.com/secmode/Invoke-Apex)
			* A PowerShell-based toolkit and framework consisting of a collection of techniques and tradecraft for use in red team, post-exploitation, adversary simulation, or other offensive security tasks.
		* [MalwLess Simulation Tool](https://github.com/n0dec/MalwLess)
			* MalwLess is an open source tool that allows you to simulate system compromise or attack behaviours without running processes or PoCs. The tool is designed to test Blue Team detections and SIEM correlation rules. It provides a framework based on rules that anyone can write, so when a new technique or attack comes out you can write your own rules and share it a with the community.
		* [Atomic Operator](https://github.com/swimlane/atomic-operator)
			* This python package is used to execute Atomic Red Team tests (Atomics) across multiple operating system environments.
		* [AutoWin](https://github.com/Reduati/AutoWin)
			* Autowin is a framework that helps organizations simulate custom attack scenarios in order to improve detection and response capabilities.
		* [Villainous](https://github.com/ObstreperousMadcap/villainius)
			* A benign application used to demonstrate an EDR detection.
		* [Swift-Attack](https://github.com/cedowens/Swift-Attack)
			* Unit tests for blue teams to aid with building detections for some common macOS post exploitation methods. I have included some post exploitation examples using both command line history and on disk binaries (which should be easier for detection) as well as post exploitation examples using API calls only (which will be more difficult for detection). The post exploitation examples included here are not all encompassing. Instead these are just some common examples that I thought would be useful to conduct unit tests around. I plan to continue to add to this project over time with additional unit tests.
		* [ATTPwn](https://github.com/Telefonica/ATTPwn)
			* ATTPwn is a computer security tool designed to emulate adversaries. The tool aims to bring emulation of a real threat into closer contact with implementations based on the techniques and tactics from the MITRE ATT&CK framework. The goal is to simulate how a threat works in an intrusion scenario, where the threat has been successfully deployed. It is focused on Microsoft Windows systems through the use of the Powershell command line. This enables the different techniques based on MITRE ATT&CK to be applied. ATTPwn is designed to allow the emulation of adversaries as for a Red Team exercise and to verify the effectiveness and efficiency of the organization's controls in the face of a real threat.
	- **Ransomware Simulation Tooling**<a name="ransomtools"></a>
		* [Phirautee](https://github.com/Viralmaniar/Phirautee)
			* A proof of concept crypto virus to spread user awareness about attacks and implications of ransomwares. Phirautee is written purely using PowerShell and does not require any third-party libraries. This tool steals the information, holds an organisation’s data to hostage for payments or permanently encrypts/deletes the organisation data.
		* [Racketeer Project - Ransomware simulation toolkit](https://github.com/dsnezhkov/racketeer)
			* The goal of this project is to provide a way for teams to simulate and test detection of common ransomware operation, in a controlled manner, against a set of company assets and network endpoints.
		* [Ransomulator](https://github.com/zeronetworks/BloodHound-Tools/tree/main/Ransomulator)
			* Ransomulator is a ransom simulator for BloodHound database. It can be used to measure a network resilience for ransomare infections, and identify "weak links" in the network.
		* [Angie-Ransomware](https://github.com/youyong123/Angie-Ransomware)
		* [Sansomware](https://github.com/sannemaasakkers/Sansomware)
			* Sansomware is a small project built for demo purposes. Want to show your friends, colleagues or employees what ransomware looks like and how it works to improve awareness? You can use Sansomware to run on your local machine without really encrypting your files.
		* [RansomwareSimulator](https://github.com/d4rkm0de/RansomwareSimulator)
			* Multithreaded Powershell script to emulate the "blast radius" of a ransomware infection. Does not actually encrypt anything! Uses passive checks to test write priv to discovered files and reports on them.
		* [my-Little-Ransomware](https://github.com/aaaddress1/my-Little-Ransomware)
		* [Ransomware Simulator](https://github.com/nccgroup/ransomware-simulator)
			* NCC Group Ransomware Simulator
		* [RAASNet](https://github.com/leonv024/RAASNet)
			* Open-Source Ransomware As A Service for Linux, MacOS and Windows
		* [Jasmin The Ransomware](https://github.com/codesiddhant/Jasmin-Ransomware)
			* Jasmin Ransomware is an advanced red team tool (WannaCry Clone) used for simulating real ransomware attacks. Jasmin helps security researchers to overcome the risk of external attacks.
----------------------------------------------------------------------------------------------------------------












------------------------------------------------------------------------------------------------------------------------------
### <a name="c2s"></a>Command, Control, Communicate (or just CnC, or C3)
* **General Stuff**<a name="c2gs"></a>
	* **Articles/Blogposts/Writeups**
		* [The C2 Matrix](https://www.thec2matrix.com)
		* [Reviving MuddyC3 Used by MuddyWater (IRAN) APT - Ahmed Khlief(2020)](https://shells.systems/reviving-leaked-muddyc3-used-by-muddywater-apt/)
		* [The origin of command and control traffic - DTM(2019)](https://dtm.uk/the-origin-of-command-and-control-traffic/)
	* **Talks/Presentations/Videos**
		* [Adversary Emulation and the C2 Matrix - Jorge Orchilles(2020)](https://www.youtube.com/watch?v=PDkn_v7gomU)
		* [Abusing "Accepted Risk" With 3rd Party C2 - HackMiamiCon5](https://www.slideshare.net/sixdub/abusing-accepted-risk-with-3rd-party-c2-hackmiamicon5)
		* [Evading C2 Detection with Asymmetry - Brandon Arvanaghi and Andrew Johnston(BSidesPhiladelphia 2017)](https://www.irongeek.com/i.php?page=videos/bsidesphilly2017/bsidesphilly-cg05-evading-c2-detection-with-asymmetry-by-brandon-arvanaghi-and-andrew-johnston)
			* Detecting callouts to command-and-control (C2) servers used to be straightforward, but attackers in your network have found ways to communicate with the outside world even under the heaviest of scrutiny. In this talk, we discuss ways to use popular websites as means of getting commands and exfiltrating information. We examine the applications of asymmetric communication, from Internet-accessible computers to embedded devices to air-gapped systems. Finally, we give some suggestions to defenders, and discuss how to detect and mitigate risks that enable asymmetric malware.
* **C2 Development**<a name="c2d"></a>
	* See [Implant & Payload Development](#implantdev)
	* **Articles/Blogposts/Writeups**
		* [How to Build a 404 page not found C2](https://www.blackhillsinfosec.com/?p=5134)
		* [InternetExplorer.Application for C2 - leoloobeek(2017)](https://adapt-and-attack.com/2017/12/)
		* [My Journey Writing A Post Exploitation Tool for macOS - Cedric Owens(2019)](https://medium.com/red-teaming-with-a-blue-team-mentaility/my-journey-writing-a-post-exploitation-tool-for-macos-d8293d51244f)
		* [Command and Control via TCP Handshake - thesw4rm(2019)](https://thesw4rm.gitlab.io/nfqueue_c2/2019/09/15/Command-and-Control-via-TCP-Handshake/)
		* [Building a Basic C2 - 0xRick](https://0xrick.github.io/misc/c2/)	
			* [Code](https://github.com/0xRick/c2)
		* [Creating A Simple C2 Server Using aiohttp - Cedric Owens(2019)](https://medium.com/red-teaming-with-a-blue-team-mentality/creating-a-simple-c2-server-using-aiohttp-62ea79640a87)
		* [Introduction to Callidus - 3xpl01tc0d3r(2020)](https://3xpl01tc0d3r.blogspot.com/2020/03/introduction-to-callidus.html)
		c2-pentest-pentesting-redteam-infosec/
	* **Talks/Presentations/Videos**
		* [C3CM: Defeating the Command - Control - and Communications of Digital Assailants](http://www.irongeek.com/i.php?page=videos/derbycon4/t206-c3cm-defeating-the-command-control-and-communications-of-digital-assailants-russ-mcree)
			* C3CM: the acronym for command- control- and communi - cations countermeasures. Ripe for use in the information security realm, C3CM takes us past C2 analysis and to the next level. Initially, C3CM was most often intended to wreck the command and control of enemy air defense networks, a very specific military mission. We-ll apply that mindset in the context of combating bots and other evil. Our version of C3CM therefore is to identify, interrupt, and counter the command, control, and communications capabilities of our digital assailants. The three phases of C3CM will utilize: Nfsight with Nfdump, Nfsen, and fprobe to conduct our identification phase, Bro with Logstash and Kibana for the interruption phase, and ADHD for the counter phase. Converge these on one useful platform and you too might have a chance deter those who would do you harm. We-ll discuss each of these three phases (identify, interrupt, and counter) with tooling and tactics, complete with demonstrations and methodology attendees can put to use in their environments. Based on the three part ISSA Journal Toolsmith series: http://holisticinfosec.blogspot.com/search?q=c3cm&max-results=20&by-date=true
		* [Flying a False Flag: Advanced C2, Trust Conflicts, and Domain Takeover - Nick Landers(BHUSA2019)](https://www.youtube.com/watch?v=2BEwqbCbQuM&feature=youtu.be)
			* This talk will discuss the methodology, selection process, and challenges of modern C2. It will cover the details of recent HTTP/S advancements and tooling for new cloud service primitives such as SQS, AppSpot, S3, and CloudFront. We will demonstrate how trust can be abused for stealthy C2 techniques via internal mail servers, defensive platforms, and trusted domains. We will also cover the various options for domain takeover, and release tooling for exploiting domain takeover scenarios in Amazon Web Services (AWS), Azure, and Google Cloud Platform (GCP).
			* [Code](https://github.com/monoxgas/FlyingAFalseFlag)
		* [Building Fully Functional C2 With Azure - Chris Truncer & Matt Grandy(WWHF2020 Virtual)](https://www.youtube.com/watch?v=hpiOv7RhvE8)
			* Building out command and control has seen multiple iterations over the years. The original build-out that most attackers utilized involved obtaining access to a server (via compromise or purchase) to use for C2 in addition to leveraging a domain to direct all traffic to an endpoint they control. Attackers, and the offensive security community, have expanded their arsenal and have started to use cloud services via domain fronting to hide their C2 traffic within legitimate web services. However, defenders have been also been developing their own techniques to detect these techniques.
	- **Commmunications**
		* [Using Windows Schannel for Covert Communication - odzhan(2017)](https://modexp.wordpress.com/2017/07/10/schannel-covert/)
		* [Using WebSockets and IE/Edge for C2 communications - arno0x0x(2017)](https://arno0x0x.wordpress.com/2017/11/10/using-websockets-and-ie-edge-for-c2-communications/)
		* [Overt Command & Control: The Art of Blending In - William Knowles, Dave Hartley(BlueHat v18)](https://www.youtube.com/watch?v=2O-KKLlsDgM)
			* This talk discusses the recent advancements in defensive technologies and the realities of their abilities to profile the legitimate and detect and alert on the illegitimate when it comes to malware C2 channels. This talk will draw on MWR's expertise of conducting countless Red Team / Adversarial Simulations and Attack Detection capability assessments across the breadth of critical infrastructure sectors. The following topics will be discussed: 1. What are the general trends in the capabilities of defensive centric tooling for the detection and prevention of C2 channels? In particular, where are the gaps that we are regularly able to leverage to remain undetected? ; 2. What currently exists with respect to offensive tooling for operating both "traditional" and "esoteric" C2? The focus will fall on what we have found to practically work rather than what is simply available.; 3. How is the landscape changing for attackers looking to operate C2 channels, and for defenders in looking to prevent them? In particular, we will provide our thoughts on answering the question: where do we go from here?
		* [SSHazam: Hide Your C2 Inside of SSH - Carrie Roberts(2019)](https://www.blackhillsinfosec.com/sshazam-hide-your-c2-inside-of-ssh/)
		* [Using and detecting C2 printer pivoting - Alfie Champion, James Coote(2020)](https://labs.f-secure.com/blog/print-c2/)
		* [Leveraging Microsoft Teams to persist and cover up Cobalt Strike traffic - Pablo Ambite(2021)](https://www.blackarrow.net/leveraging-microsoft-teams-to-persist-and-cover-up-cobalt-strike-traffic/)
		* [Azure Application Proxy C2 - Adam Chester(2021)](https://www.trustedsec.com/blog/azure-application-proxy-c2/)
		* [BadOutlook for C2 - Ali S. Ahmad(2021)](https://www.optiv.com/insights/source-zero/blog/badoutlook-c2)
		* [AWS GuardDuty: Post-DNS Era Covert Channel For C&C - Sze Siong Teo(HITB2021 AMS)](https://www.youtube.com/watch?v=liQjug4uFQI)
			* In this talk, we will look at how malware can maintain a covert communication channel to an external APT without getting detected by popular NIDS like Snort and Zeek. This can be done by monitoring the OS connection table and selectively pick the hosts of any known cloud services that are in use instead of hardwiring a specific cloud service. In addition, hostnames used by the apt/yum repository in a system are also inspected for CDN usage as attackers can host their covert channel behind the same CDN service to evade NIDS detection. This method guarantees the outbound connection will always work and continuously keep the traffic outside the radar of NIDS.  Later, we will move on to the cloud environment and demonstrate a more robust C&C and data exfiltration channel by using an attacker-owned S3 bucket to evade AWS GuardDuty detection. This is a blind spot that can be used to stay undetected from GuardDuty due to the different way how it sees IAM authenticated requests versus S3 pre-signed URL requests. Besides, we will also explore other AWS services that can be misused as the covert channel for C&C and data exfiltration without getting detected by GuardDuty in this talk.  Finally, we will discuss some of the mitigation methods to render these backdoor network channels unusable and common mistakes to avoid when using a public cloud like AWS.
	* **Tools**
		* [Callback Catcher](https://bitbucket.org/gavinanders/callback-catcher/src/master/)
			* Callback Catcher is a multi-socket control tool designed to aid in pentest activities. It has a simple web application with an backend API that allows the user control what TCP and UDP sockets should be opened on the server. It records any and all data send to the exposed sockets and logs it to a database which can be easily accessed via it's backend API. Itís kind of intended to be like the love child of Burp Collaborator and Responder. Alternatively think of it like a low/medium interactive honeypot. Its been coded on top of the Django REST framework, which offers a number of benefits , primarily being able to create your own client scripts and tools and quickly searching and filtering of data. Opening of sockets is built on top of Python's ServerSocket library. Upon spinning up a socket a user is given the option to assign a handler to the socket, which is affectively user defined code that overwrites the handler function within the SocketServer.TCPServer and SocketServer.UDPServer classes. This code tells the socket how to handle the incoming data and what to respond with. Each connection to the socket is recorded to a database.
		* [CheckPlease](https://github.com/Arvanaghi/CheckPlease)
			* Implant-Security modules written in PowerShell, Python, Go, Ruby, C, C#, Perl, and Rust. 
		* [emptynest](https://github.com/empty-nest/emptynest)
			* Emptynest is a plugin based C2 server framework. The goal of this project is not to replace robust tools such as Empire, Metasploit, or Cobalt Strike. Instead, the goal is to create a supporting framework for quickly creating small, purpose built handlers for custom agents. No agent is provided. Users of Emptynest should create their own agents that implement minimal functionality and can be used to evade detection and establish a more robust channel. An example of an agent might support Unhooking, DLL Unloading, and code execution. Due to the simple nature of this project, it is recommended that agents be kept private.
		* [RemoteRecon](https://github.com/xorrior/RemoteRecon)
			* RemoteRecon provides the ability to execute post-exploitation capabilities against a remote host, without having to expose your complete toolkit/agent. Often times as operator's we need to compromise a host, just so we can keylog or screenshot (or some other miniscule task) against a person/host of interest. Why should you have to push over beacon, empire, innuendo, meterpreter, or a custom RAT to the target? This increases the footprint that you have in the target environment, exposes functionality in your agent, and most likely your C2 infrastructure. An alternative would be to deploy a secondary agent to targets of interest and collect intelligence. Then store this data for retrieval at your discretion. If these compromised endpoints are discovered by IR teams, you lose those endpoints and the information you've collected, but nothing more.
		* [Nuages](https://github.com/p3nt4/Nuages)
			* Nuages aims at being a C2 framework in which back end elements are open source, whilst implants and handlers must be developed ad hoc by users. As a result, it does not provide a way to generate implants, but an open source framework to develop and manage compatible implants that can leverage all the back end resources already developed.
			* [Tutorial: Creating a custom full featured implant(Nuages)](https://github.com/p3nt4/Nuages/wiki/Tutorial:-Creating-a-custom-full-featured-implant)
	* **C3**
		* **101**
			* [C3 - Custom Command and Control - FSecure Labs](https://labs.f-secure.com/tools/c3/)
			* [C3](https://github.com/FSecureLABS/C3)
				* C3 (Custom Command and Control) is a tool that allows Red Teams to rapidly develop and utilise esoteric command and control channels (C2). It's a framework that extends other red team tooling, such as the commercial Cobalt Strike (CS) product via ExternalC2, which is supported at release. It allows the Red Team to concern themselves only with the C2 they want to implement; relying on the robustness of C3 and the CS tooling to take care of the rest. This efficiency and reliability enable Red Teams to operate safely in critical client environments (by assuring a professional level of stability and security); whilst allowing for safe experimentation and rapid deployment of customised Tactics, Techniques and Procedures (TTPs). Thus, empowering Red Teams to emulate and simulate an adaptive real-world attacker.
		* **Articles/Blogposts/Writeups**
			* [Making Donuts Explode – Updates to the C3 Framework - Tim Carrington](https://labs.f-secure.com/blog/making-donuts-explode-updates-to-the-c3-framework/)
* **C2 Frameworks**<a name="c2-frames"></a>
	* [The C2 Matrix](https://www.thec2matrix.com/)
	* **ARTi-C2**
		* [Atomic-Red-Team-Intelligence-C2](https://github.com/blackbotinc/Atomic-Red-Team-Intelligence-C2)
			* ARTi-C2 is a modern execution framework built to empower security teams to scale attack scenario execution from single and multi-breach point targets with the intent to produce actionable attack intelligence that improves the effectiveness security products and incident response.
	* **BlackMamba**
		* [BlackMamba](https://github.com/loseys/BlackMamba)
			* BlackMamba is a multi-client C2/post-exploitation framework
	* **Deimos**
		* [DeimosC2](https://github.com/DeimosC2/DeimosC2)
			* DeimosC2 is a Golang command and control framework for post-exploitation.
	* **Covenant**
		* **101**
			* [Entering a Covenant: .NET Command and Control - Ryan Cobb](https://posts.specterops.io/entering-a-covenant-net-command-and-control-e11038bcf462)
			* [Covenant](https://github.com/cobbr/Covenant)
				* Covenant is a .NET command and control framework that aims to highlight the attack surface of .NET, make the use of offensive .NET tradecraft easier, and serve as a collaborative command and control platform for red teamers. Covenant is an ASP.NET Core, cross-platform application that includes a web-based interface that allows for multi-user collaboration.
		* **Articles/Blogposts/Writeups**
			* [Covenant Tasks 101 - RastaMouse](https://rastamouse.me/2019/12/covenant-tasks-101/)
			* [Covenant, Donut, TikiTorch - RastaMouse](https://web.archive.org/web/20200408131145/https://rastamouse.me/2019/08/covenant-donut-tikitorch/)
			* [Red Teaming with Covenant and Donut - NaijaSecForce](https://blog.naijasecforce.com/red-teaming-with-covenant-and-donut/)
			* [Actually Using Covenant C2 and Not Just Installing It! - Ryan Villarreal(2020)](https://bestestredteam.com/2020/02/19/interacting-with-covenant-c2/)
			* [Covenant Task 101 — PPID Spoof Example - Onwukike Chinedu(2020)](https://medium.com/@chinedu.onwukike/covenant-task-101-ppid-spoof-example-c07ecb21007f)
			* [Using Custom Covenant Listener Profiles & Grunt Templates to Elude AV - Rasta Mouse(2020)](https://offensivedefence.co.uk/posts/covenant-profiles-templates/)
		* **Talks/Presentations/Videos**
			* [Operating with Covenant - Ryan Cobb and Justin Bui(SO-CON 2020)](https://www.youtube.com/watch?v=oN_0pPI6TYU&list=PLJK0fZNGiFU-2vFpjnt96j_VSuQVTkAnO&index=20&t=6s)
				* In the age of EDR and threat hunting, red teamers need flexible, robust command and control platforms. Red teamers need the ability to collaborate with teammates, customize implant behavior and command and control traffic, track artifacts, and quickly adapt for defensive technologies. Covenant is a .NET command and control platform that provides these necessary tools to red teamers. Workshop participants will learn basic and advanced usage of Covenant, how to customize their tradecraft within Covenant, and how the platform can help them conduct operations.			
		* **Tooling**
			* [CovenantTasks](https://github.com/py7hagoras/CovenantTasks)
	* **FactionC2**
		* [The Faction C2 Framework](https://www.factionc2.com/articles/rebuilding-a-faction-part-2)
			* Faction is a C2 framework for security professionals, providing an easy way to extend and interact with agents. It focuses on providing an easy, stable, and approachable platform for C2 communications through well documented REST and Socket.IO APIs.
	* **FudgeC2**
		* [FudgeC2](https://github.com/Ziconius/FudgeC2)
			* FudgeC2 is a Powershell command and control platform designed to facilitate team collaboration and campaign timelining. This aims to help clients better understand red team activities by presenting them with more granular detail of adversarial techniques. Built on Python3 with a web frontend, FudgeC2 aims to provide red teamers a simple interface in which to manage active implants across their campaigns.
	* **Grat2**
		* [GRAT2](https://github.com/r3nhat/GRAT2)
			* GRAT2 is a Command and Control (C2) tool written in python3 and the client in .NET 4.5.
	* **goc2**
		* [goc2](https://github.com/grines/goc2)
			* MacOS C2 Framework 
		* [goc2-agent](https://github.com/grines/goc2-agent)
			* Payloads for goc2	
	* **Koadic**
		* [Koadic](https://github.com/zerosum0x0/koadic)
			* Koadic, or COM Command & Control, is a Windows post-exploitation rootkit similar to other penetration testing tools such as Meterpreter and Powershell Empire. The major difference is that Koadic does most of its operations using Windows Script Host (a.k.a. JScript/VBScript), with compatibility in the core to support a default installation of Windows 2000 with no service packs (and potentially even versions of NT4) all the way through Windows 10.
		* [Post Exploitation with KOADIC - Ian Kings](https://www.prismacsi.com/en/post-exploitation-with-koadic/)
	* **MacC2**
		* [MacC2](https://github.com/cedowens/MacC2)
			* MacC2 is a macOS post exploitation tool written in python that uses Objective C calls or python libraries as opposed to command line executions. The client is written in python2, which though deprecated is still being shipped with base Big Sur installs. It is possible down the road that Apple will remove python2 (or python altogether) from base macOS installs but as of Nov 2020 this is not the case. Apple plans to eventually remove scripting runtimes from base macOS installs, but it is unknown when that will happen since Big Sur includes python.
	* **Merlin**
		* [merlin](https://github.com/Ne0nd0g/merlin)
			* Merlin is a cross-platform post-exploitation HTTP/2 Command & Control server and agent written in golang. 
		* [Introducing Merlin — A cross-platform post-exploitation HTTP/2 Command & Control Tool - Russel Van Tuyl(2017)](https://medium.com/@Ne0nd0g/introducing-merlin-645da3c635a)
		* [HTTP/2 Magic with Merlin - Russel Van Tuyl(BSides Knoxville 2018)](https://www.youtube.com/watch?v=tCK1yp5d1E8)
			* HTTP/2 is a protocol that increases efficiency and overcomes shortfalls of the HTTP/1 protocol and is intended to be used only over TLS connections. Because this protocol is relatively new, there is a lack of tools capable of inspecting the protocol to detect or prevent attacks. The protocol’s use of Perfect Forward Secrecy TLS cipher suites further complicates matters by preventing inspecting technologies from capturing the keying material required to decrypt traffic for inspection. This presentation provides an overview of the HTTP/2 protocol along with implications for defenders and attackers alike. Merlin is a cross-platform post-exploitation HTTP/2 Command & Control server and agent written in golang.A new tool will be released to the public that leverages HTTP/2 Command & Control of a host across many platforms to include Linux, Windows, Android, and MacOS.
		* [Inside the Magic – A Merlin Walkthrough – Russel Van Tuyl (SO-CON 2020)](https://www.youtube.com/watch?v=dEPVn5MI0XA&list=PLJK0fZNGiFU-2vFpjnt96j_VSuQVTkAnO&index=5)
			* Web technologies continue to progress and with that brings an abundance of new protocols that aim to increase internet traffic efficiency and security. This introduces new capabilities into web browser which in-turn requires security tools and process to adapt for effective handling, monitoring, or detection. The TCP based HTTP/2 and the UDP based HTTP/3 protocols are two of the newer protocols that are used by major web browsers and could exist on your network. In this talk we'll do a walkthrough of Merlin, a post-exploitation Command and Control (C2) tool written in Go that leverages these protocols for Command and Control (C2) traffic. The presentation will go through an introduction to the HTTP/2 and HTTP/3 protocols along with other unique Merlin capabilities such as the OPAQUE key exchange, encrypted JSON Web Tokens, and dynamic JA3 client hash modification. The talk will conclude with a Power User section walking through Merlin's various menus and ways to avoid detections. Attend this presentation to increase your knowledge and capabilities of these newer version of HTTP.
	* **Mouse**
		* [Mouse](https://github.com/entynetproject/mouse)
			* Mouse Framework is an iOS and macOS post-exploitation framework that gives you a command line session with extra functionality between you and a target machine using only a simple Mouse payload. Mouse gives you the power and convenience of uploading and downloading files, tab completion, taking pictures, location tracking, shell command executio… 
	- **Mythic(Appfell)**

		
		
		

* [Offensive Operations With Mythic – Kyle Avery – PSW #706 - Kyle Avery(2021)](https://securityweekly.com/shows/offensive-operations-with-mythic-kyle-avery-psw-706/)		

		- **101**
			* [Mythic](https://github.com/its-a-feature/Mythic)
				* A cross-platform, post-exploit, red teaming framework built with python3, docker, docker-compose, and a web browser UI. It's designed to provide a collaborative and user friendly interface for operators, managers, and reporting throughout red teaming.
			* [A Change of Mythic Proportions - Cody Thomas(2020)](https://posts.specterops.io/a-change-of-mythic-proportions-21debeb03617)
			* [Mythic Feature Examples - Cody Thomas(2020)](https://www.youtube.com/playlist?list=PLHVFedjbv6sNLB1QqnGJxRBMukPRGYa-H)
			* [Launching Apfell Programmatically - Cedric Owens(2019)](https://medium.com/red-teaming-with-a-blue-team-mentality/launching-apfell-programmatically-c90fe54cad89)
		- **Articles/Blogposts/Writeups**
			* [In-memory Python Modules with the Medusa Mythic Agent - Alfie Champion(2021)](https://ajpc500.github.io/c2/In-memory-Python-Modules-With-The-Medusa-Mythic-Agent/)
			* [Let’s Talk DNS: Designing a DNS Profile for Mythic C2 - Thiago Mayllart(2021)](https://www.hakaioffensivesecurity.com/lets-talk-dns-designing-a-dns-profile-for-mythic-c2/)
			* [Multi-Stage Offensive Operations with Mythic - Kyle Avery(2021)](https://blog.kyleavery.com/posts/multi-stage-mythic/)
				* [Code](https://github.com/kyleavery/Multi-Stage-Mythic)
		- **Talks/Presentations/Videos**
			* [From Zero to Hero: How to Create a Custom Mythic Agent - Cody Thomas and Josiah Massari](https://www.youtube.com/watch?v=xdmdHMjK1KA&list=PLJK0fZNGiFU-2vFpjnt96j_VSuQVTkAnO&index=18)
				* Learn how to create your own Mythic agent from scratch. In this two-hour workshop, we will create a new PowerShell agent that dynamically loads new commands, hooks into a few of Mythic's features, and provides an avenue to load 3rd party tooling. Come prepped with Mythic installed and you will leave with the code for your new Hercules agent.
			* [Sharpening Our Arrows: Training with Apollo – Dwight Hohnstein (SO-CON 2020)](https://www.youtube.com/watch?v=bcRgj1X7WsA&list=PLJK0fZNGiFU-2vFpjnt96j_VSuQVTkAnO&index=12)
				* Apollo is the latest Windows-platform integration into the Mythic command-and-control framework. Apollo is open source, written in C#, and designed with training in mind to help students who take our course offerings better understand how different attack techniques are implemented at a technical level. Learn how to use an extensible and feature-rich Windows agent that leverages the rich functionality of Mythic in this hour-long debrief.
		- **Agents**
			* [Github Repo of 'Official' Agents](https://github.com/MythicAgents)
			* [Apollo](https://github.com/MythicAgents/Apollo)
			* [Atlas](https://github.com/MythicAgents/atlas)
			* [Hermes](https://github.com/MythicAgents/hermes)
			* [Medusa](https://github.com/MythicAgents/Medusa)
			* [Merlin](https://github.com/MythicAgents/merlin)
			* [Venus](https://github.com/MythicAgents/venus)
		- **Payload Wrappers**	
			* [ScareCrow Wrapper](https://github.com/kyleavery/scarecrow_wrapper)
	* **NinjaC2**
		* [Ninja](https://github.com/ahmedkhlief/Ninja)
			* Ninja C2 is an Open source C2 server created by Purple Team to do stealthy computer and Active directoty enumeration without being detected by SIEM and AVs , Ninja still in beta version and when the stable version released it will contains many more stealthy techniques and anti-forensic to create a real challenge for blue team to make sure all the defenses configured correctly and they can detect sophisticated attacks. Ninja use python to server the payload and control the agents . the agents are based on C# and powershell which can bypass leading AVs . Ninja comunicate with the agents in secure channel encrpyted with AES-256 and the key is not hard coded but randomly generated on the campaign start , every agent connect to the C2 get the key and if the C2 restarted a new key will be used by all old agents and the new. Ninja also randomize the callback URLs for every campaign to bypass static detection.
			* [Introducing Ninja C2 : the C2 built for stealth red team Operations - Ahmed Khlief(2020)](https://shells.systems/introducing-ninja-c2-the-c2-built-for-stealth-red-team-operations/)
	* **Octopus**
		* [Octopus](https://github.com/mhaskar/Octopus)
			* Octopus is an open source, pre-operation C2 server based on python which can control an Octopus powershell agent through HTTP/S.
			* [Unveiling Octopus: The pre-operation C2 for Red Teamers - Askar](https://shells.systems/unveiling-octopus-the-pre-operation-c2-for-red-teamers/)
			* [Automate Octopus C2 RedTeam Infrastructure Deployment - Askar(2020)](https://shells.systems/automate-octopus-c2-redteam-infrastructure-deployment/)
	* **PoshC2**
		* [Project Homepage](https://labs.nettitude.com/tools/poshc2/)
		* [Github Code](https://github.com/nettitude/PoshC2)
		* [Documentation](https://poshc2.readthedocs.io/en/latest/)
		* [Introducing FComm – C2 Lateral Movement - Richard Hicks(2021)](https://labs.nettitude.com/blog/introducing-fcomm-c2-lateral-movement/)
	* **sak1to-shell**
		* [sak1to-shell](https://github.com/d4rk007/sak1to-shell)
			* Multi-threaded c2 server and reverse shell client written in pure C. 
	* **Shadow**
		* [shad0w](https://github.com/bats3c/shad0w)
			* SHAD0W is a modular C2 framework designed to successfully operate on mature enviroments. It will use a range of methods to evade EDR and AV while allowing the operator to continue using tooling an tradecraft they are familiar with. Its powered by Python 3.8 and C, using Donut for payload generation. By using Donut along side the process injection capabilities of SHAD0W it gives the operator the ability to execute .NET assemblies, EXEs, DLLs, VBS, JS or XSLs fully inside memory. Dynamically resolved syscalls are heavily used to avoid userland API hooking, anti DLL injection to make it harder for EDR to load code into the beacons and offical microsoft mitigation methods to protect spawn processes.
			* [Blogpost](https://labs.jumpsec.com/2020/06/03/shad0w/)
	* **SharpC2**
		* [SharpC2](https://github.com/SharpC2/SharpC2)
			* .NET C2 Framework Proof of Concept 
		* [SharpC2 - RastaMouse](https://rastamouse.me/blog/sharpc2/)
	* **Silent Trinity**
		* [SILENTTRINITY](https://github.com/byt3bl33d3r/SILENTTRINITY)
			* SILENTTRINITY is modern, asynchronous, multiplayer & multiserver C2/post-exploitation framework powered by Python 3 and .NETs DLR. It's the culmination of an extensive amount of research into using embedded third-party .NET scripting languages to dynamically call .NET API's, a technique the author coined as BYOI (Bring Your Own Interpreter). The aim of this tool and the BYOI concept is to shift the paradigm back to PowerShell style like attacks (as it offers much more flexibility over traditional C# tradecraft) only without using PowerShell in anyway.
		* [Hunting for SILENTTRINITY - Wee-Jing Chung(2019)](https://blog.f-secure.com/hunting-for-silenttrinity/)
			* SILENTTRINITY (byt3bl33d3r, 2018) is a recently released post-exploitation agent powered by IronPython and C#. This blog post will delve into how it works and techniques for detection.
		* [SILENTTRINITY - DarthSidious](https://hunter2.gitbook.io/darthsidious/command-and-control/silenttrinity)
			* Using Kali as a C2 Server
		* [How to Use Silent Trinity - Bresaola 0.3.0dev - H4cklife!!](https://h4cklife.org/posts/how-to-use-silent-trinity/)
	* **Sliver**
		* [Sliver](https://github.com/BishopFox/sliver)
			* Sliver is a general purpose cross-platform implant framework that supports C2 over Mutual-TLS, HTTP(S), and DNS. Implants are dynamically compiled with unique X.509 certificates signed by a per-instance certificate authority generated when you first run the binary. The server, client, and implant all support MacOS, Windows, and Linux (and possibly every Golang compiler target but we've not tested them all).
	* **TrevorC2**
		* [TrevorC2](https://github.com/trustedsec/trevorc2)
			* TrevorC2 is a client/server model for masking command and control through a normally browsable website. Detection becomes much harder as time intervals are different and does not use POST requests for data exfil.
* **Papers**<a name="c2papers"></a>
	* [Command & Control: Understanding, Denying and Detecting - 2014 - Joseph Gardiner, Marco Cova, Shishir Nagaraja](https://arxiv.org/ftp/arxiv/papers/1408/1408.1136.pdf)
* **Cobalt Strike**<a name="cobaltstrike"></a>
	* **101**<a name="cs101"></a>
		- [Cobalt Strike Community Kit](https://github.com/Cobalt-Strike/community_kit)
			* "Community Kit is a central repository of extensions written by the user community to extend the capabilities of Cobalt Strike. The Cobalt Strike team acts as the curator and provides this kit to showcase this fantastic work."
		- **Stuff**
			* [In-memory Evasion (2018) - Raphael Mudge](https://www.youtube.com/playlist?list=PL9HO6M_MU2nc5Q31qd2CwpZ8J4KFMhgnK)
				* In-memory Evasion is a four-part mini course on the cat and mouse game related to memory detections. This course is for red teams that want to update their tradecraft in this area. It’s also for blue teams that want to understand the red perspective on these techniques. Why do they work in some situations? How is it possible to work around these heuristics in other cases?
			* [Red Team Operations with Cobalt Strike (2019) Playlist - Raphael Mudge](https://www.youtube.com/playlist?list=PL9HO6M_MU2nfQ4kHSCzAQMqxQxH47d1no)
			* [CSFM - Cobal Strike Field Manual](https://github.com/001SPARTaN/csfm)
			* Cobalt Strike Field Manual - A quick reference for Windows commands that can be accessed in a beacon console.
			* [Fighting the Toolset - Mudge](https://www.youtube.com/watch?v=RoqVunX_sqA)
				* This talk explores offense design decisions, default workflows, and how to adapt when your advantages are your weaknesses.
		- **Official Blogposts**
			* [Cobalt Strike 01.08.14 – EXE Artifacts: A New Hope - Raphael Mudge(2014)](https://www.cobaltstrike.com/blog/cobalt-strike-01-08-14-exe-artifacts-a-new-hope/)
			* [Talk to your children about Payload Staging - Raphael Mudge(2016)](https://blog.cobaltstrike.com/2016/06/22/talk-to-your-children-about-payload-staging/)
			* [Cobalt Strike 3.5.1 – Important Security Update(2016)](https://blog.cobaltstrike.com/2016/10/03/cobalt-strike-3-5-1-important-security-update/)
			* [Kits, Profiles, and Scripts… Oh my! - Raphael Mudge(2017)](https://blog.cobaltstrike.com/2017/10/03/kits-profiles-and-scripts-oh-my/)
			* [Cobalt Strike’s Process Injection: The Details - Raphael Mudge(2019)](https://www.cobaltstrike.com/blog/cobalt-strikes-process-injection-the-details-cobalt-strike/)
			* [Learn Pipe Fitting for all of your Offense Projects - Raphael Mudge(2021)](https://blog.cobaltstrike.com/2021/02/09/learn-pipe-fitting-for-all-of-your-offense-projects/)
		- **Usage**
			* [Cobalt Strike 101 - @spottheplanet](https://ired.team/offensive-security/red-team-infrastructure/cobalt-strike-101-installation-and-interesting-commands)
			* [Cobalt Strike. Walkthrough for Red Teamers - Neil Lines(2019)](https://www.pentestpartners.com/security-blog/cobalt-strike-walkthrough-for-red-teamers/)
			* [Red Teaming With Cobalt Strike – Not So Obvious Features - Oddvar Moe(2020)](https://www.trustedsec.com/blog/red-teaming-with-cobalt-strike-not-so-obvious-features/)
			* [Cobalt Strike and Tradecraft - Hausec(2021)](https://hausec.com/2021/07/26/cobalt-strike-and-tradecraft/)
			* [SiegeCast "COBALT STRIKE BASICS" with Tim Medin and Joe Vest(2021)](https://www.youtube.com/watch?v=OtM6iegGYAQ)
			* [Cobalt Strike CheatSheet - S1ckB0y1337](https://github.com/S1ckB0y1337/Cobalt-Strike-CheatSheet)
			* [Cobalt Strike Red Team Cheat Sheet - wsummerhill](https://github.com/wsummerhill/CobaltStrike_RedTeam_CheatSheet)
		- **About**
			* [Cobalt Strike PowerShell Execution - mez0(2020)](https://mez0.cc/posts/cobaltstrike-powershell-exec/)
			* [Anatomy of Cobalt Strike’s DLL Stager - Maxime Thiebaut(2021)](https://blog.nviso.eu/2021/04/26/anatomy-of-cobalt-strike-dll-stagers/)
			* [Defining Cobalt Strike Components So You Can BEA-CONfident in Your Analysis - Alyssa Rahman(2021)](https://www.mandiant.com/resources/defining-cobalt-strike-components)
			* [Analyzing Cobalt Strike for Fun and Profit - Etienne Maynier(2021)](https://randhome.io/blog/2020/12/20/analyzing-cobalt-strike-for-fun-and-profit/)
			* [Striking Back at Retired Cobalt Strike: A look at a legacy vulnerability - NCC ExploitDevGroup(2020)](https://research.nccgroup.com/2020/06/15/striking-back-at-retired-cobalt-strike-a-look-at-a-legacy-vulnerability/)
	- **Agressor Scripts**<a name="csas"></a>
		- **101**
			* [Aggressor Script - cs](https://www.cobaltstrike.com/aggressor-script/index.html)
			* [Aggressor 101: Unleashing Cobalt Strike for Fun and Profit](https://medium.com/@001SPARTaN/aggressor-101-unleashing-cobalt-strike-for-fun-and-profit-879bf22cea31)
			* [vscode-language-aggressor](https://github.com/darkoperator/vscode-language-aggressor)
				* Cobalt Strike Aggressor extension for Visual Studio Code. This is a Visual Studio Code (VSC) extension that aims to provide: An implement of the Sleep and Cobalt Strike (CS) Aggressor grammar; and The definition of Cobalt Strike functions' prototype
		- **Articles/Blogposts/Writeups**
			* [Adding Easy GUIs to Aggressor Scripts - Jeff McJunkin(2016)](https://bluescreenofjeff.com/2016-09-07-adding-easy-guis-to-aggressor-scripts/)
			* [Aggressively Efficient with Aggressor - Joseph Kingstone(2021)](https://www.kingstonesecurity.com/blog/efficiency-with-aggressor)
			* [The Return of Aggressor - RastaMouse](https://rastamouse.me/2019/06/the-return-of-aggressor/)
				* I’ve previously blogged about how to combine MSBuild and TikiSpawn to execute a Cobalt Strike agent, circumventing AppLocker and Defender on Windows 10 1903. Inspired by Forty North’s Aggressor implemention I thought it would be fun to knock something similar up to leverage TikiSpawn for lateral movement via MSBuild and WMI, and this will hopefully mark the beginning of more Aggressor for common/popular TikiTorch use cases.
				* [Code](https://github.com/rasta-mouse/TikiTorch/tree/master/Aggressor)
			* [Cobalt Strike Aggressor Scripts-Ception - Amonsec(2020)](https://ntamonsec.blogspot.com/2020/07/cobalt-strike-aggressor-scripts-ception.html)
		- **Collections of**
			* [CS Aggressor Scripts - ramen0x3f](https://github.com/ramen0x3f/AggressorScripts#utilscna)	
			* [aggressor_scripts_collection - invokethreatguy](https://github.com/invokethreatguy/aggressor_scripts_collection)
				* Collection of various Aggressor Scripts for Cobalt Strike from awesome people. Will be sure to update this repo with credit to each person.
			* [Aggressor Scripts - oldb00t](https://github.com/oldb00t/AggressorScripts)
			* [aggressor_scripts_collection - invokethreatguy](https://github.com/invokethreatguy/aggressor_scripts_collection)
				* Collection of various aggressor scripts for Cobalt Strike from awesome people. Will be sure to update this repo with credit to each person.
			* [AggressorScripts - bluescreenofjeff](https://github.com/bluscreenofjeff/AggressorScripts)
				* Aggressor scripts for use with Cobalt Strike 3.0+
			* [Agressor Script - rasta-mouse](https://github.com/rasta-mouse/Aggressor-Script)
				* Collection of Aggressor Scripts for Cobalt Strike
		- **Samples/Tooling**
			* [Aggressor - Get Text Messages For Your Incoming Beacons - FortyNorthSecurity(2016)](https://fortynorthsecurity.com/blog/aggressor-get-text-messages-for-your-incoming-beacons/)
			* [CSSG](https://github.com/RCStep/CSSG)
				* CSSG is an aggressor and python script used to more easily generate and format beacon shellcode; Adds Shellcode - Shellcode Generator to the Cobalt Strike top menu bar
			* [List-GitHubAssembly](https://github.com/mdsecactivebreach/Execute-GithubAssembly-Aggressor/)
				* Fetch a list of avaialble artifacts from the configured GitHub repo.
			* [CobaltPatch](https://github.com/ASkyeye/CobaltPatch)
				* Custom project template for creating useable bytecode blobs that can be placed in the various `transform-x64` and `transform-x86` blocks for post-ex and stage libraries.
			* [CVE-2018-4878](https://github.com/vysec/CVE-2018-4878)
				* Aggressor Script to launch IE driveby for CVE-2018-4878
			* [EventLogMaster](https://github.com/QAX-A-Team/EventLogMaster)
			* [UACBypass Aggressor Script](https://github.com/RhinoSecurityLabs/Aggressor-Scripts/tree/master/UACBypass)
				* This aggressor script adds three UAC bypass techniques to Cobalt Strike's interface + beacon console.
			* [MoveKit](https://github.com/0xthirteen/MoveKit)
				* Movekit is an extension of built in Cobalt Strike lateral movement by leveraging the execute_assembly function with the SharpMove and SharpRDP .NET assemblies. The aggressor script handles payload creation by reading the template files for a specific execution type.
			* [StayKit](https://github.com/0xthirteen/StayKit)
				* StayKit is an extension for Cobalt Strike persistence by leveraging the execute_assembly function with the SharpStay .NET assembly. The aggressor script handles payload creation by reading the template files for a specific execution type.
			* [Cobalt-Clip](https://github.com/DallasFR/Cobalt-Clip)
				* Cobalt-clip is clipboard addons for cobaltstrike to interact with clipboard. With this you can dump, edit and monitor the content of q clipboard.
			* [Quickrundown](https://github.com/icebearfriend/Quickrundown)
				* Quickrundown (QRD) at its core is an overlay for the bps command packaged with Cobalstrike; this overlay incorporates elements from @r3dQu1nn's processcolor.cna aggressor script to provide enhancements. Utilizing QRD will allow an operator to quickly characterize what processes are both known and unknown on a host through the use of colors and notes about the processes displayed. Built into the script are capabilities to add processes, or update processes that already have characterizations assigned to them. This lets the operator do characterization and research with permenance (for the life of their cna file, that is).
			* [cwd-in-beacon-status-bar.cna](https://github.com/mgeeky/cobalt-arsenal/blob/master/cwd-in-beacon-status-bar.cna)
			* [SharpRelay](https://github.com/pkb1s/SharpRelay)
				* On-the-fly packet modification using Windivert as a base.
			* [HelpColor](https://github.com/outflanknl/HelpColor)
				* Agressor script that lists available Cobalt Strike beacon commands and colors them based on their type
			* [mgeekys_arsenal.cna](https://github.com/mgeeky/cobalt-arsenal/tree/master/mgeekys_arsenal)
				* "This is my Cobalt Strike beast aggressor script combining lots of tools, enhancements, aliases and goodies in a single CNA."
	- **Beacon**<a name="csbeacon"></a>
		* **101**
			* [Beacon Command Behavior and OPSEC Considerations - Official Docs](https://hstechdocs.helpsystems.com/manuals/cobaltstrike/current/userguide/content/topics/appendix-a_beacon-opsec-considerations.htm)
		* **Examples of**
			* [SharpBeacon](https://github.com/mai1zhi2/SharpBeacon)
			* [geacon](https://github.com/darkr4y/geacon)
			* [VermillionStrike](https://www.intezer.com/blog/malware-analysis/vermilionstrike-reimplementation-cobaltstrike/)
	- **Beacon Object File**
		- **101**
			* [Beacon Object Files - cs.com](https://www.cobaltstrike.com/help-beacon-object-files)
				* A Beacon Object File (BOF) is a compiled C program, written to a convention that allows it to execute within a Beacon process and use internal Beacon APIs. BOFs are a way to rapidly extend the Beacon agent with new post-exploitation features.
			* [Beacon Object Files - Luser Demo(Raphael Mudge 2020)](https://www.youtube.com/watch?v=gfYswA_Ronw)
		- **Writing**
			* [bof_template](https://github.com/Cobalt-Strike/bof_template)
			* [bof-vs-template](https://github.com/nccgroup/nccfsas/tree/main/Tools/bof-vs-template)
				* This is a template project for building Cobalt Strike BOFs in Visual Studio.
			* [Visual-Studio-BOF-template](https://github.com/securifybv/Visual-Studio-BOF-template)
				* A Visual Studio template used to create Cobalt Strike BOFs
			* [A Developer’s Introduction to Beacon Object Files - Christopher Paschen(2020)](https://www.trustedsec.com/blog/a-developers-introduction-to-beacon-object-files/)
			* [Writing Beacon Object Files: Flexible, Stealthy, and Compatible - CoreLabs Research(2021)](https://www.cobaltstrike.com/blog/writing-beacon-object-files-flexible-stealthy-and-compatible/)
			* [Cobalt Strike BOF Making - hackplanet.io](https://hackplanet.io/aiovg_videos/cobalt-strike-bof-making/)
			* [Writing Beacon Object Files: Flexible, Stealthy, and Compatible - Santiago Pecin(2021)](https://www.coresecurity.com/core-labs/articles/writing-beacon-object-files-flexibie-stealthy-and-compatible)
			* [Process Injection via custom Beacon Object Files Part 1 - Cerbersec(2021)](https://cerbersec.com/2021/08/26/beacon-object-files-part-1.html)
				* [Process Injection via custom Beacon Object Files Part 2](https://cerbersec.com/2021/08/26/beacon-object-files-part-2.html)
			* [Creating the WhereAmI Cobalt Strike BOF - Bobby Cooke(2021)](https://0xboku.com/2021/08/19/Bof-WhereAmI.html)
			* [BOF2shellcode — a tutorial converting a stand-alone BOF loader into shellcode - Gijs Hollestelle(2021)](https://medium.com/falconforce/bof2shellcode-a-tutorial-converting-a-stand-alone-bof-loader-into-shellcode-6369aa518548)
				* [BOF2shellcode](https://github.com/FalconForceTeam/BOF2shellcode)
		- **Using**
			* [Custom DLL injection with Cobalt Strike's Beacon Object Files - Tom Carver(2020)](https://x64sec.sh/custom-dll-injection-with-cobalt-strike/)
			* [Fetching SharpHound data entirely in-memory (no dropped ZIP or JSON files) using BOF.NET and Cobalt Strike - William Knowles(2021)](https://williamknowles.io/fetching-sharphound-data-entirely-in-memory-no-dropped-zip-or-json-files-using-bof-net-and-cobalt-strike/)
			* [Malware Development: Leveraging Beacon Object Files for Remote Process Injection via Thread Hijacking - Connor McGarr(2021)](https://connormcgarr.github.io/thread-hijacking/)
		- **Samples/Tooling**
			- Collections
				* [CS Community Kit](https://cobalt-strike.github.io/community_kit/)
				* [CS-BOFs](https://github.com/pwn1sher/CS-BOFs)
				* [alphaseclab cobalt strike](https://github.com/alphaSeclab/cobalt-strike)
				* [Various BOF collection](https://github.com/crypt0p3g/bof-collection)
				* [BOFs - JamesCooteUK](https://github.com/JamesCooteUK/BOFs)
				* [BOFs - gervild](https://github.com/guervild/BOFs)
				* [cobalt-arsenal](https://github.com/mgeeky/cobalt-arsenal)
				* [cobaltstrike_bofs](https://github.com/m57/cobaltstrike_bofs)
				* [CobaltStrike-BOF](https://github.com/Yaxser/CobaltStrike-BOF)
			- AD
				* [tgtdelegation](https://github.com/connormcgarr/tgtdelegation)
					* tgtdelegation is a Beacon Object File (BOF) to obtain a usable TGT via the "TGT delegation trick" 
				* [ADSearch](https://github.com/tomcarver16/ADSearch)
					* A tool written for cobalt-strike's execute-assembly command that allows for more efficent querying of AD.
			- Building
				* [BOF-Builder](https://github.com/ceramicskate0/BOF-Builder)
					* C# .Net 5.0 project to build BOF (Beacon Object Files) in mass based on them all being in a folder directory struct somewhere.
				* [Beacon Object File (BOF) Creation Helper](https://github.com/dtmsecurity/bof_helper)
			- Compression
				* [Zipper](https://github.com/outflanknl/Zipper)
					* This CobaltStrike tool allows Red teams to compress files and folders from local and UNC paths. This could be useful in situations where large files or folders need to be exfiltrated. After compressing a file or folder a random named zipfile is created within the user temp folder.
			- Credentials
				* [aggrokatz](https://github.com/sec-consult/aggrokatz)
					* Aggrokatz is an aggressor plugin extension for Cobalt Strike which enables pypykatz to interface with the beacons remotely and allows it to parse LSASS dump files and registry hive files to extract credentials and other secrets stored without downloading the file and without uploading any suspicious code to the beacon.
				* [CredBandit](https://github.com/xforcered/CredBandit)
					* Proof of concept Beacon Object File (BOF) that uses static x64 syscalls to perform a complete in memory dump of a process and send that back through your already existing Beacon communication channel
				* [WdToggle](https://github.com/outflanknl/WdToggle)
					* A Beacon Object File (BOF) for Cobalt Strike which uses direct system calls to enable WDigest credential caching.
				* [PPLDump BOF](https://github.com/EspressoCake/PPLDump_BOF)
					* A faithful transposition of the key features/functionality of @itm4n's PPLDump project as a BOF.
				* [NanoDump](https://github.com/helpsystems/nanodump)
					* A flexible tool that creates a minidump of the LSASS process.
					* [Nanodump: A Red Team Approach to Minidumps - Santiago Pecin(2021)](https://www.coresecurity.com/core-labs/articles/nanodump-red-team-approach-minidumps)
				* [CredManBOF](https://github.com/jsecu/CredManBOF)
					* This is an BOF file to use with Cobalt Strike, dumping the credential manager by abusing the SeTrustedCredmanAccess Privilege.
				* [BOF-RegSave](https://github.com/EncodeGroup/BOF-RegSave)
					* Beacon Object File(BOF) for CobaltStrike that will acquire the necessary privileges and dump SAM - SYSTEM - SECURITY registry keys for offline parsing and hash extraction.
			- Discovery
				* [Situational Awareness BOF](https://github.com/trustedsec/CS-Situational-Awareness-BOF)
					* This Repo intends to serve two purposes. First it provides a nice set of basic situational awareness commands implemented in BOF. This allows you to perform some checks on a host before you begin executing commands that may be more invasive. Its larger goal is providing a code example and workflow for others to begin making more BOF files.
				* [AggressiveProxy](https://github.com/EncodeGroup/AggressiveProxy)
					* AggressiveProxy is a combination of a .NET 3.5 binary (LetMeOutSharp) and a Cobalt Strike aggressor script (AggressiveProxy.cna). Once LetMeOutSharp is executed on a workstation, it will try to enumerate all available proxy configurations and try to communicate with the Cobalt Strike server over HTTP(s) using the identified proxy configurations.
				* [EnumCLR.c](https://gist.github.com/G0ldenGunSec/8ca0e853dd5637af2881697f8de6aecc)
					* Cobalt Strike BOF to identify processes with the CLR loaded with a goal of identifying SpawnTo / injection candidates.
				* [DLL Image Resource Version Enumeration BOF](https://github.com/EspressoCake/DLL_Version_Enumeration_BOF)
					* A BOF for enumerating version information for DLLs associated for a Beacon process.
				* [whereami](https://github.com/boku7/whereami)
					* Cobalt Strike Beacon Object File (BOF) that uses handwritten shellcode to return the process Environment strings without touching any DLL's.
				* [Registry-Recon](https://github.com/optiv/Registry-Recon)
					* Cobalt Strike Aggressor Script that Performs System/AV/EDR Recon
				* [Process Protection Level Enumerator BOF](https://github.com/EspressoCake/Process_Protection_Level_BOF)
					* A Syscall-only BOF file intended to grab process protection attributes, limited to a handful that Red Team operators and pentesters would commonly be interested in.
				* [xPipe](https://github.com/xforcered/xPipe)
					* Cobalt Strike BOF to list Windows Pipes & return their Owners & DACL Permissions
				* [HalosGate Processlist Cobalt Strike BOF](https://github.com/boku7/halosgate-ps)
					* Cobalt Strike Beacon Object File (BOF) that uses a custom HalosGate & HellsGate syscaller, written in assembly, to return a list of processes.
			- Evasion
				https://github.com/ajpc500/BOFs/tree/main/ETW
				* [BOF - Trusted Path UAC Bypass](https://github.com/netero1010/TrustedPath-UACBypass-BOF)
					* Cobalt Strike beacon object file implementation for trusted path UAC bypass. The target executable will be called without involving "cmd.exe" by using DCOM object.
				* [UAC-SilentClean](https://github.com/EncodeGroup/UAC-SilentClean)
					* This project implements a DLL planting technique to bypass UAC Always Notify and execute code in a high integrity process.
			- Execution
				* [Weaponizing your favorite Go program for Cobalt Strike - CCob(2020)](https://ethicalchaos.dev/2020/01/26/weaponizing-your-favorite-go-program-for-cobalt-strike/)
					* [Code](https://github.com/CCob/goreflect)
				* [BOF-Adios](https://gitlab.com/nephosec/bof-adios)
				* [Syscalls Shellcode Injection BOF](https://github.com/ajpc500/BOFs/tree/main/SyscallsInject)
				* [InlineWhispers](https://github.com/outflanknl/InlineWhispers)
					* A Proof of Concept for weaponizing SysWhispers for making direct system calls in Cobalt Strike Beacon Object File.
				* [InlineWhispers2](https://github.com/Sh0ckFR/InlineWhispers2)
					* Tool for working with Direct System Calls in Cobalt Strike's Beacon Object Files (BOF) via Syswhispers2
				* [SysWhispers2](https://github.com/FalconForceTeam/SysWhispers2BOF)
					* Script to use SysWhispers2 direct system calls from Cobalt Strike BOFs.
					* [FalconFriday — Direct system calls and Cobalt Strike BOFs — 0xFF14 - Gijs Hollestelle(2021)](https://medium.com/falconforce/falconfriday-direct-system-calls-and-cobalt-strike-bofs-0xff14-741fa8e1bdd6)
				* [spawn](https://github.com/boku7/spawn)
					* Cobalt Strike BOF that spawns a sacrificial process, injects it with shellcode, and executes payload. Built to evade EDR/UserLand hooks by spawning sacrificial process with Arbitrary Code Guard (ACG), BlockDll, and PPID spoofing.
				- DLL-Related
					* [DLL Exports Extraction BOF](https://github.com/EspressoCake/DLL-Exports-Extraction-BOF)
						* DLL Exports Extraction BOF with optional NTFS transactions.
					* [DLL Hijack Search Order BOF](https://github.com/EspressoCake/DLL-Hijack-Search-Order-BOF)
						* DLL Hijack Search Order Enumeration BOF
				- .NET
					* [BOF.NET](https://github.com/CCob/BOF.NET)
						* A .NET Runtime for Cobalt Strike's Beacon Object Files; BOF.NET is a small native BOF object combined with the BOF.NET managed runtime that enables the development of Cobalt Strike BOFs directly in .NET. BOF.NET removes the complexity of native compilation along with the headaches of manually importing native API. Testing BOF.NET assemblies is also generally much easier, since the .NET assemblies can be debugged using a traditional managed debugger.
				 	* [InlineExecute-Assembly](https://github.com/anthemtotheego/InlineExecute-Assembly)
				 		* InlineExecute-Assembly is a proof of concept Beacon Object File (BOF) that allows security professionals to perform in process .NET assembly execution as an alternative to Cobalt Strikes traditional fork and run execute-assembly module 
				 		* [Don’t Be Rude, Stay: Avoiding Fork&Run .NET Execution With InlineExecute-Assembly - Shawn (@anthemtotheego)(2021)](https://securityintelligence.com/posts/net-execution-inlineexecute-assembly/)
				- Process Injection-related
					* [cThreadHijack](https://github.com/connormcgarr/cThreadHijack)
						* Beacon Object File (BOF) for remote process injection via thread hijacking
					* [HOLLOW](https://github.com/boku7/HOLLOW)
						* EarlyBird process hollowing technique (BOF) - Spawns a process in a suspended state, inject shellcode, hijack main thread with APC, and execute shellcode
					* [BOF-DLL-Inject](https://github.com/tomcarver16/BOF-DLL-Inject)
						* Manual Map DLL injection implemented with Cobalt Strike's Beacon Object Files.
			- Hooking
				* [Detect-Hooks](https://github.com/anthemtotheego/Detect-Hooks)
					* Proof of concept Beacon Object File (BOF) that attempts to detect userland hooks in place by AV/EDR
				* [unhook-bof](https://github.com/rsmudge/unhook-bof)
					* This is a Beacon Object File to refresh DLLs and remove their hooks. The code is from Cylance's Universal Unhooking research:
				* [Removing Hooks by Refreshing NTDLL](https://gitlab.com/riccardo.ancarani94/ntdll-refresher-hook-removal-bof)
					* A Beacon Object File used to remove userland hooks from NTDLL. Currently supports only 64 bit (although the change is trivial).
			- Lateral Movement
				* [ServiceMove-BOF](https://github.com/netero1010/ServiceMove-BOF)
					* New lateral movement technique by abusing Windows Perception Simulation Service to achieve DLL hijacking code execution.
				* [CS-BOF](https://github.com/Mr-Un1k0d3r/SCShell/tree/master/CS-BOF)
					* BOF Version os ScShell for Cobalt Strike
			- Persistence
				* [DLL-Hijack-Search-Order-BOF](https://github.com/EspressoCake/DLL-Hijack-Search-Order-BOF)
					* DLL Hijack Search Order Enumeration BOF
			- Privilege Escalation
				* [SpoolSystem](https://github.com/rxwx/spoolsystem)
					* SpoolSystem is a CNA script for Cobalt Strike which uses @itm4n's Print Spooler named pipe impersonation trick to gain SYSTEM privileges without creating any new process or relying on cross-process shellcode injection (if the selfinject method is used).
				* [Toggle_Token_Privileges_BOF](https://github.com/EspressoCake/Toggle_Token_Privileges_BOF)
					* Syscall BOF to arbitrarily add/detract process token privilege rights.
			- Processes
				* [FindObjects-BOF](https://github.com/outflanknl/FindObjects-BOF)
					* A Cobalt Strike Beacon Object File (BOF) project which uses direct system calls to enumerate processes for specific loaded modules or process handles.
				* [cs-rdll-example](https://github.com/rxwx/cs-rdll-ipc-example)
					* Example code for using named pipe output with beacon ReflectiveDLLs
			- Web
				* [Curl-BOF](https://github.com/ajpc500/BOFs/tree/main/Curl)
	* **External C2**<a name="csc2"></a>
		* **Doc**
			* [Cobalt Strike External C2 Paper](https://www.cobaltstrike.com/downloads/externalc2spec.pdf)
			* [Malleable-C2-Profiles Offical Repo](https://github.com/Cobalt-Strike/Malleable-C2-Profiles)
		- **External C2**
			* [Cobalt Strike Malleable C2 Design and Reference Guide](https://github.com/threatexpress/malleable-c2)
				* This project is intended to serve as reference when designing Cobalt Strike Malleable C2 profiles.
			* [ExternalC2.NET](https://github.com/rasta-mouse/ExternalC2.NET)
				* .NET Standard 2.0 libraries which implement Cobalt Strike's External C2 specfication (revision 0.1).
			* [external_c2 framework](https://github.com/RhinoSecurityLabs/external_c2_framework)
				* Python framework for usage with Cobalt Strike's External C2 specification as described in the spec. The primary design goal is to be a very modular implementation of the external c2 spec that provides enough abstraction to easily implement C2 channels for Cobalt Strike. Ideally, all a user would have to do is create a transport module, an encoder module, and populate a configuration file to implement a new channel.
		* **Tools**
			* [External C2 - cs](https://github.com/outflanknl/external_c2)
				* POC for Cobalt Strike external C2
			* [Malleable-C2-Profiles](https://github.com/rsmudge/Malleable-C2-Profiles)
				* Malleable C2 is a domain specific language to redefine indicators in Beacon's communication. This repository is a collection of Malleable C2 profiles that you may use. These profiles work with Cobalt Strike 3.x.
		* **Articles**
			* [Cobalt Strike over external C2 – beacon home in the most obscure ways](https://outflank.nl/blog/2017/09/17/blogpost-cobalt-strike-over-external-c2-beacon-home-in-the-most-obscure-ways/)
			* [OPSEC Considerations for Beacon Commands - CobaltStrike](https://blog.cobaltstrike.com/2017/06/23/opsec-considerations-for-beacon-commands/)
			* [Valid SSL Certificates with SSL Beacon - cs](https://www.cobaltstrike.com/help-malleable-c2#validssl)
			* [Randomized Malleable C2 Profiles Made Easy](https://bluescreenofjeff.com/2017-08-30-randomized-malleable-c2-profiles-made-easy/)
			* [Agentless Post Exploitation](https://blog.cobaltstrike.com/2016/11/03/agentless-post-exploitation/)
			* [“Tasking” Office 365 for Cobalt Strike C2 - William Knowles](https://labs.f-secure.com/archive/tasking-office-365-for-cobalt-strike-c2/)
				* To explore the potential that Cobalt Strike's newly added “External C2” extension offers offensive teams, MWR have developed a customized C2 channel that uses Office 365 as the communications path.  The key objectives of this post are as follows: Demonstration of a Cobalt Strike C2 channel through Office 365 using “tasks” within Outlook.; Insight into some of the challenges of designing a customized Cobalt Strike C2 channel and one way in which they were addressed.
			* [Sleeping with a Mask On (Cobalt Strike) - Adam Svoboda(2021)](https://adamsvoboda.net/sleeping-with-a-mask-on-cobaltstrike/)
			* [Tailoring Cobalt Strike on Target - Adam Chester(2021)](https://www.trustedsec.com/blog/tailoring-cobalt-strike-on-target/)
			* [ExternalC2.NET - RastaMouse(2021)](https://rastamouse.me/externalc2-net/)
	- **Malleable**
		- **101**
			* [Malleable C2 Documenation - cs](https://www.cobaltstrike.com/help-malleable-c2)
			* [Official Public Code Repo](https://github.com/cobalt-strike)
		- **Articles/Blogposts/Writeups**
			* [Understanding Cobalt Strike Profiles - Updated for Cobalt Strike 4.5 - Andy Gill(2021)](https://blog.zsec.uk/cobalt-strike-profiles/)
			* [magic_mz_x86 and magic_mz_x64 - Shantanu Khandelwal](https://www.redteam.cafe/red-team/shellcode-injection/magic_mz_x86-and-magic_mz_x64)
		- **Profiles**
			* [User Defined Reflective DLL Loader - Official Documentation](https://hstechdocs.helpsystems.com/manuals/cobaltstrike/current/userguide/content/topics/malleable-c2-extend_user-defined-rdll.htm?cshid=1054)
			* [Dissecting Cobalt Strike Loader - Lokesh J(2021)](https://labs.k7computing.com/index.php/dissecting-cobalt-strike-loader/)	
			* [Random C2 Profile Generator](https://github.com/threatexpress/random_c2_profile)
				* This project is designed to generate malleable c2 profiles based on the reference profile at https://github.com/threatexpress/malleable-c2/.		
			* [Malleable-C2-Profiles](https://github.com/BC-SECURITY/Malleable-C2-Profiles)
				* Malleable C2 Profiles. A collection of profiles used in different projects using Cobalt Strike & Empire.
			* [C2concealer](https://github.com/FortyNorthSecurity/C2concealer)
				* C2concealer is a command line tool that generates randomized C2 malleable profiles for use in Cobalt Strike.
				* [Introducing C2concealer: a C2 Malleable Profile Generator for Cobalt Strike - FortyNorthSecurity](https://fortynorthsecurity.com/blog/introducing-c2concealer/)
				* [Customizing C2Concealer - Part 2](https://fortynorthsecurity.com/blog/customizing-c2concealer-part-ii/)
			* [cs2webconfig](https://github.com/bashexplode/cs2webconfig)
				* Convert Cobalt Strike profiles to IIS web.config files
	- **Loader**
		* [BokuLoader](https://github.com/boku7/BokuLoader)
	- **Loader**
		* [ElusiveMice](https://github.com/mgeeky/ElusiveMice)
			* "This is a fork of Cobalt Strike's User-Defined Reflective Loader which in turn is a fork of Stephen Fewer's ReflectiveDLLInjection implementation, but with a slight plot twist - it adds a few well-known AV/EDR evasion hooks/patches!"
	* **General**<a name="csg"></a>
		* [OPSEC Considerations for Beacon Commands](https://blog.cobaltstrike.com/2017/06/23/opsec-considerations-for-beacon-commands/)
		* [Modern Defenses and YOU!](https://blog.cobaltstrike.com/2017/10/25/modern-defenses-and-you/)
		* [Making AMSI Jump - RastaMouse(2020)](https://offensivedefence.co.uk/posts/making-amsi-jump/)
		* [D/Invokify PPID Spoofy & BlockDLLs - RastaMouse(2020)](https://offensivedefence.co.uk/posts/ppidspoof-blockdlls-dinvoke/)
		* [A tale of .NET assemblies, cobalt strike size constraints, and reflection. - Jean Maes(2020)](https://redteamer.tips/a-tale-of-net-assemblies-cobalt-strike-size-constraints-and-reflection/)
		* [Cobalt Strike Spawn & Tunnel - RastaMouse(2021)](https://rastamouse.me/cobalt-strike-spawn-tunnel/)
	* **Logging**<a name="csl"></a>
		* [cslogwatch](https://github.com/attactics/cslogwatch)
			* cslogwatch is python-based application that implements log watching, parsing, and storage functionality. It is capable of state tracking any cobalt strike log directory and monitoring for any file creations, modifications, or deletions. Once cslogwatch identifies a new log file creation or existing file modification, the log files are automatically parsed and the results are stored in an sqlite database.
			* [cslogwatch: Cobalt Strike Log Tracking, Parsing & Storage - attactick.org(2019)](https://attactics.org/2019/07/cslogwatch-cobalt-strike-tracking-parsing-storage/)
	* **Phishing**<a name="csp"></a>
		* [Cobalt Strike - Spear Phishing documentation](https://www.cobaltstrike.com/help-spear-phish)
		* [Spear phishing with Cobalt Strike - Raphael Mudge](https://www.youtube.com/watch?v=V7UJjVcq2Ao)
		* [Cobalt Strike Blog - What's the go-to phishing technique or exploit?(2014)](https://blog.cobaltstrike.com/2014/12/17/whats-the-go-to-phishing-technique-or-exploit/)
	* **Pivoting**
		* [HTTP(s) C2 Pivoting - Steve Borosh(2020)](https://medium.com/@rvrsh3ll/offensive-internal-http-s-agent-pivoting-2e9b4b7e58d8)
	* **Redirectors**<a name="csr"></a>
		* [Convert Cobalt Strike profiles to Apache mod_rewrite .htaccess files to support HTTP C2 Redirection](https://github.com/threatexpress/cs2modrewrite)
			* This is a quick script that converts a Cobalt Strike profile to a functional mod_rewrite .htaccess file to support HTTP proxy redirection from Apache to a CobaltStrike teamserver.
		* [redi](https://github.com/taherio/redi)
			* Automated redirector setup compatible with HTTP RATs (CobaltStrike Beacon, meterpreter, etc), and CobaltStrike DNS Beacon. The script can either set up nginx reverse proxy, or DNS proxy/forwarder using dnsmasq. If HTTPS was selected, it will automatically setup letsencrypt certbot and obtain valid letsencrypt SSL certificates for your redirector domain name, and start nginx using the generated configuration.
	* **Tool Extension/Integration**<a name="cstei"></a>
		* [ANGRYPUPPY](https://github.com/vysec/ANGRYPUPPY)
			* Bloodhound Attack Path Execution for Cobalt Strike
		* [HAMMERTHROW: Rotate my domain - Vincent Yiu](https://vincentyiu.com/red-team/domain-fronting/hammerthrow-rotate-my-domain)
			* HAMMERTHROW is an aggressor script for CobaltStrike that rotates your command and control domains automatically.
			* [Code link](https://github.com/vysecurity/Aggressor-VYSEC/blob/master/HAMMERTHROW.cna)
		* [DDEAutoCS](https://github.com/p292/DDEAutoCS)
			* A cobaltstrike script that integrates DDEAuto Attacks (launches a staged powershell CS beacon). This is not massively stealthy as far as CS scripts go anything like that at the moment, more of a proof of concept, and for having a play. Customise as you see fit to your needs.
		* [ADSearch](https://github.com/tomcarver16/ADSearch)
			* A tool written for cobalt-strike's execute-assembly command that allows for more efficent querying of AD.
		* [CrossC2](https://github.com/gloxec/CrossC2)
			* generate CobaltStrike's cross-platform payload 
		* [SharpAllTheThings](https://github.com/N7WEra/SharpAllTheThings)
			* The idea is to collect all the C# projects that are Sharp{Word} that can be used in Cobalt Strike as execute assembly command.
		* [SharpeningCobaltStrike](https://github.com/cube0x0/SharpeningCobaltStrike)
			* In realtime compiling of dotnet v35/v40 exe/dll binaries + obfuscation with ConfuserEx on your linux cobalt strike server.
	* **Other**<a name="cso"></a>
		* [Modern Defense and You - CS](https://blog.cobaltstrike.com/2017/10/25/modern-defenses-and-you/)
		* [User Driven Attacks - cs](https://blog.cobaltstrike.com/2014/10/01/user-driven-attacks/)
		* [Cobalt Strike Visualizations - SPARTan](https://medium.com/@001SPARTaN/cobalt-strike-visualizations-e6a6e841e16b)
		* [Move faster, Stay longer - Steven F](https://posts.specterops.io/move-faster-stay-longer-6b4efab9c644)
* **Empire**<a name="empire"></a>
	* **Articles**<a name="articles"></a>
		* [Powershell Empire 101 - @spottheplanet](https://ired.team/offensive-security/red-team-infrastructure/powershell-empire-101)
		* [Hunting Red Team Empire C2 Infrastructure](http://www.chokepoint.net/2017/04/hunting-red-team-empire-c2.html)
		* [Athena: The CIA’s RAT vs Empire](https://bneg.io/2017/05/22/athena-the-cias-rat-vs-empire/)
		* [Bringing the hashes home with reGeorg & Empire](https://sensepost.com/blog/2016/bringing-the-hashes-home-with-regeorg-empire/)
		* [Intercepting passwords with Empire and winning](https://sensepost.com/blog/2016/intercepting-passwords-with-empire-and-winning/)
		* [Advanced Weapons Training - for the Empire - Jeremy Johnson](https://www.slideshare.net/JeremyJohnson166/advanced-weapons-training-for-the-empire)
		* [Empire API Cheat Sheet](https://github.com/SadProcessor/Cheats/blob/master/EmpireAPI.md)
		* [Evading Anomaly-Based NIDS with Empire - Utku Sen blog](https://utkusen.com/blog/bypassing-anomaly-based-nids-with-empire.html)
		* [Empire & Tool Diversity: Integration is Key - sixdub](https://www.sixdub.net/?p=627)
		* [Empire Fails - harmj0y](http://www.harmj0y.net/blog/empire/empire-fails/)
		* [Empire Was Great Again…For a Week - CX01N(2020)](https://www.bc-security.org/post/microsoft-makes-empire-great-again)
	* **Customizing**<a name="ecustom"></a>
		* [Using PowerShell Empire with a Trusted Certificate](https://www.blackhillsinfosec.com/using-powershell-empire-with-a-trusted-certificate/)
		* [How to Make Empire Communication profiles - bluescreenofjeff](https://github.com/bluscreenofjeff/bluscreenofjeff.github.io/blob/master/_posts/2017-03-01-how-to-make-communication-profiles-for-empire.md)
		* [Empire – Modifying Server C2 Indicators](http://threatexpress.com/2017/05/empire-modifying-server-c2-indicators/)
		* [Empire Domain Fronting](https://www.xorrior.com/Empire-Domain-Fronting/)
		* [Empire without powershell](https://bneg.io/2017/07/26/empire-without-powershell-exe/)
		* [Build Your Own: Plugins in Empire - strikersecurity](https://strikersecurity.com/blog/empire-plugins/)
		* [How to Make Communication Profiles for Empire - Jeff Dimmock](https://posts.specterops.io/how-to-make-communication-profiles-for-empire-46da8554338a)
		* [Reigning the Empire, evading detection - vanmieghem.io](https://vanmieghem.io/reigning-the-empire-evading-detection/)
			* tl;dr: Configure a (valid) certificate and add jitter to have Empire communications stay below the radar.
	* **Manual**<a name="edoc"></a>
		* [RedTrooperFM - Empire Module Wiki](https://github.com/SadProcessor/Cheats/blob/master/RedTrooperFM.md)
			* A one page Wiki for all your Empire RTFM needs...
		* [Encrypted Key Exchange understanding - StackOverflow](https://stackoverflow.com/questions/15779392/encrypted-key-exchange-understanding)
	* **Modules & Additions/Extensions**<a name="emods"></a>
		* [Empire-mod-Hackplayers](https://github.com/Hackplayers/Empire-mod-Hackplayers)
			* Collection of custom Empire Modules
		* [Sharpire - An implimentation of the Empire Agent in C#](https://github.com/0xbadjuju/Sharpire)
		* [Automated Empire Infrastructure - bneg.io](https://bneg.io/2017/11/06/automated-empire-infrastructure/)
		* [firstorder](https://github.com/tearsecurity/firstorder)
			* firstorder is designed to evade Empire's C2-Agent communication from anomaly-based intrusion detection systems. It takes a traffic capture file (pcap) of the network and tries to identify normal traffic profile. According to results, it creates an Empire HTTP listener with appropriate options.
		* [e2modrewrite](https://github.com/infosecn1nja/e2modrewrite)
			* Convert Empire profiles to Apache mod_rewrite scripts
		* [PrintDemon](https://github.com/BC-SECURITY/Invoke-PrintDemon)
			* This is an PowerShell Empire launcher PoC using PrintDemon and Faxhell. The module has the Faxhell dll already embedded which levages CVE-2020-1048 for privilege escalation. The vulnerability allows an unprivileged user to gain system-level privileges and is based on @ionescu007 PoC.
		* [liniaal](https://github.com/sensepost/liniaal)
			* [Article](https://sensepost.com/blog/2017/liniaal-empire-through-exchange/)
			* Liniaal allows for the creation of a C2 channel for Empire agents, through an Exchange server. All communication is done through MAPI/HTTP or RPC/HTTP and directly between the Liniaal agent and the Exchange server. No traffic traverses the traditional network boundary as plain HTTP, bypassing most network based detection and blocking.
		* [PrintDemon](https://github.com/BC-SECURITY/Invoke-PrintDemon)
			* This is an PowerShell Empire launcher PoC using PrintDemon and Faxhell. The module has the Faxhell dll already embedded which levages CVE-2020-1048 for privilege escalation. The vulnerability allows an unprivileged user to gain system-level privileges and is based on @ionescu007 PoC.
			* [PrintDemon](https://github.com/ionescu007/PrintDemon)
			* [faxhell](https://github.com/ionescu007/faxhell)
	* **Multi-User GUI**
		* [StarKiller](https://github.com/BC-SECURITY/Starkiller)
			* Starkiller is a Frontend for Powershell Empire. It is an Electron application written in VueJS.
			* [An Introduction to Starkiller - CX01N](https://www.bc-security.org/post/an-introduction-to-starkiller)
---------------------------------------------------------------------------------------------------------------------------------























---------------------------------------------------------------------------------------------------------------------------------
### <a name="domains"></a>Domains and Domain Related Things
* **General**<a name="dg"></a>
	* **Articles/Writeups**
		* [Domain Dispute - don’t lose that great looking C2 domain - Matt “Rudy” Benton(2020)](https://medium.com/maverislabs/domain-dispute-dont-lose-that-great-looking-c2-domain-8472b6cc4c5b)
- **Domain Borrowing**
	- **101**
		* [Domain Borrowing: Catch My C2 Traffic if You Can - Tianze Ding & Junyu Zhou(BH Asia2021)](https://www.youtube.com/watch?v=eVr0kKdgM2I)
			* [Slides](https://i.blackhat.com/asia-21/Thursday-Handouts/as-21-Ding-Domain-Borrowing-Catch-My-C2-Traffic-If-You-Can.pdf)
			* For red teams, CDN is a good redirector and protector for their C2 traffic, especially with domain fronting. However, if there are HTTPS decryption devices in the network, domain fronting can be easily detected by comparing SNI and HOST. This talk will present a new method to hide your C2 traffic with CDN to circumvent censorship. We will detail some tricks we found in some CDN implementations, and how we chain them together to “borrow” a domain and its valid HTTPS certificate to hide our C2 traffic, especially, when the SNI and HOST of our C2 traffic are the same. We named this method “Domain Borrowing”. In addition, we will present a detection bypass demo against the Palo Alto PAN-OS, and release a C2 agent PoC to help your red team operations.
	- **Articles/Writeups**
		* [Domain Borrowing - Cerbersec(2021)](https://cerbersec.com/2021/05/18/domain-borrowing.html)
	- **Talks & Videos**
	- **Tools**
		* [DomainBorrowing](https://github.com/Dliv3/DomainBorrowing)
			* This repo provides a Covenant Implant Template, which uses Domain Borrowing for C2 communication.
		* [DomainBorrowingC2](https://github.com/Cerbersec/DomainBorrowingC2)
* **Domain Fronting**<a name="df"></a>
	* **101**
		* [Blocking-resistant communication through domain fronting](https://www.bamsoftware.com/talks/fronting-pets2015/)
		* [Camouflage at encryption layer: domain fronting](https://www.securityartwork.es/2017/01/24/camouflage-at-encryption-layer-domain-fronting/)
		* [Domain Fronting - Infosec Institute](http://resources.infosecinstitute.com/domain-fronting/)
		* [Continually Enhancing Domain Security on Amazon CloudFront - aws.amazon(2019)](https://aws.amazon.com/blogs/networking-and-content-delivery/continually-enhancing-domain-security-on-amazon-cloudfront/)
	* **Articles/Writeups**
		* [High-reputation Redirectors and Domain Fronting](https://blog.cobaltstrike.com/2017/02/06/high-reputation-redirectors-and-domain-fronting/)
		* [TOR Fronting – Utilising Hidden Services for Privacy](https://www.mdsec.co.uk/2017/02/tor-fronting-utilising-hidden-services-for-privacy/)
		* [Finding Domain frontable Azure domains - thoth / Fionnbharr (@a_profligate)](https://theobsidiantower.com/2017/07/24/d0a7cfceedc42bdf3a36f2926bd52863ef28befc.html)
		* [Domain Fronting Via Cloudfront Alternate Domains](https://www.mdsec.co.uk/2017/02/domain-fronting-via-cloudfront-alternate-domains/)
		* [TTP: Domain Fronting with Metasploit and Meterpreter - beyondbinary](https://beyondbinary.io/articles/domain-fronting-with-metasploit-and-meterpreter/)
		* [Alibaba CDN Domain Fronting - Vincent Yiu](https://medium.com/@vysec.private/alibaba-cdn-domain-fronting-1c0754fa0142)
		* [How I Identified 93k Domain-Frontable CloudFront Domains](https://www.peew.pw/blog/2018/2/22/how-i-identified-93k-domain-frontable-cloudfront-domains)
		* [Metasploit Domain Fronting With Microsoft Azure - chigstuff](https://chigstuff.com/blog/metasploit-domain-fronting-with-microsoft-azure/)
		* [Red Team Insights on HTTPS Domain Fronting Google Hosts Using Cobalt Strike](https://www.cyberark.com/threat-research-blog/red-team-insights-https-domain-fronting-google-hosts-using-cobalt-strike/)
		* [DomainFrontingLists](https://github.com/vysec/DomainFrontingLists)
			* A list of Domain Frontable Domains by CDN
		* [Metasploit Domain Fronting With Microsoft Azure - Chris Higgins](https://chigstuff.com/blog/metasploit-domain-fronting-with-microsoft-azure/)
		* [Being a Good Domain Shepherd - Christopher Maddalena](https://posts.specterops.io/being-a-good-domain-shepherd-57754edd955f?gi=2cadd2578045)
			* [Part 2](https://posts.specterops.io/being-a-good-domain-shepherd-part-2-5e8597c3fe63)
		* [Domain Fronting using StackPath CDN - Vincent Yiu](https://vincentyiu.com/red-team/domain-fronting/domain-fronting-using-stackpath-cdn)
			* A guide to setting up domain fronting, and exploring additional quirks that StackPath can provide.
		* [Domain Fronting, Beacons, and TLS! - Adam Brown(2019)](https://coffeegist.com/security/domain-fronting-beacons-and-tls/)
		* [Fastly and Fronting - FortyNorthSecurity(2020)](https://fortynorthsecurity.com/blog/fastly-and-fronting/)
		* [Hardening Your Azure Domain Front - Steve Borosh](https://medium.com/@rvrsh3ll/hardening-your-azure-domain-front-7423b5ab4f64)
		* [Empire Domain Fronting With Microsoft Azure - Truneski(2020)](https://truneski.github.io/blog/2019/02/27/empire-domain-fronting-with-microsoft-azure/)
		* [Covenant C2 Infrastructure with Azure Domain Fronting - Fat Rodzianko(2020)](https://fatrodzianko.com/2020/05/11/covenant-c2-infrastructure-with-azure-domain-fronting/)
		* [SCYTHE Domain Fronting through Azure CDN - Derek Johnson(2020)](https://www.scythe.io/library/scythe-domain-fronting-through-azure-cdn)
		* [Hiding Behind the Front Door - fortalicesolutions(2021)](https://www.fortalicesolutions.com/posts/hiding-behind-the-front-door-with-azure-domain-fronting)
		* [Using HTTPS Redirectors With Metasploit and SilentTrinity C2 Frameworks - assume-breach(2021)](https://assume-breach.medium.com/using-https-redirectors-with-metasploit-and-silenttrinity-c2-frameworks-4a5639e025ca)
		* [Firebase Domain Front - Hiding C2 as App traffic - redteam.cafe](https://www.redteam.cafe/red-team/domain-front/firebase-domain-front-hiding-c2-as-app-traffic)
		* [Hiding Behind the Front Door - fortalicesolutions(2021)](https://www.fortalicesolutions.com/posts/hiding-behind-the-front-door-with-azure-domain-fronting)
	* **Talks & Videos**
		* [Domain Fronting is Dead, Long Live Domain Fronting Using TLS 1.3 - Erik Hunstad(Defcon Safemode2020)](https://www.youtube.com/watch?v=TDg092qe50g)
			* Domain fronting, the technique of circumventing internet censorship and monitoring by obfuscating the domain of an HTTPS connection was killed by major cloud providers in April of 2018. However, with the arrival of TLS 1.3, new technologies enable a new kind of domain fronting. This time, network monitoring and internet censorship tools are able to be fooled on multiple levels. This talk will give an overview of what domain fronting is, how it used to work, how TLS 1.3 enables a new form of domain fronting, and what it looks like to network monitoring. You can circumvent censorship and monitoring today without modifying your tools using an open source TCP and UDP pluggable transport tool that will be released alongside this talk.
	* **Tools**
		* **Finding Vulnerable Domains**
			* [DomainFrontDiscover](https://github.com/peewpw/DomainFrontDiscover)
				* Scripts and results for finding domain frontable CloudFront domains
			* [FindFrontableDomains](https://github.com/rvrsh3ll/FindFrontableDomains)
				* Search for potential frontable domains
			* [Simple domain fronting PoC with GAE C2 server](https://www.securityartwork.es/2017/01/31/simple-domain-fronting-poc-with-gae-c2-server/)
				* In this entry we continue with domain fronting; on this occasion we will explore how to implement a simple PoC of a command and control and exfiltration server on Google App Engine (GAE), and we will see how to do the domain fronting from Windows, with a VBS or PowerShell script, to hide interactions with the C2 server.
			* [Finding Frontable Domain](https://github.com/rvrsh3ll/FindFrontableDomains)
* **Managing**
	* [Shepherd](https://github.com/GhostManager/Shepherd)
		* Shepherd is a Django application written in Python 3.7 and is designed to be used by a team of operators. It keeps track of domain names and each domain's current DNS settings, categorization, project history, and status. The tracked statuses include which domains are: ready to be used, burned/retired, or in use, and which team member checked out each of the active domains.
* **Obtaining**
	* [JustDropped.com](https://www.justdropped.com/)
		* Deleted Domain Names Daily 
* **Tools**<a name="dt"></a>
	* **Identifyin Useful Domains**
		* [Domain Hunter](https://github.com/minisllc/domainhunter)
			* Checks expired domains, bluecoat categorization, and Archive.org history to determine good candidates for phishing and C2 domain names
		* [AIRMASTER](https://github.com/t94j0/AIRMASTER)
			* Use ExpiredDomains.net and BlueCoat to find useful domains for red team.
	* **Domain Reputation/Identification**
		* [Chameleon](https://github.com/mdsecactivebreach/Chameleon)
			* Chameleon is a tool which assists red teams in categorising their infrastructure under arbitrary categories. Currently, the tool supports arbitrary categorisation for Bluecoat, McAfee Trustedsource and IBM X-Force. However, the tool is designed in such a way that additional proxies can be added with ease.
		* [CatMyFish](https://github.com/Mr-Un1k0d3r/CatMyFish)
			* Search for categorized domain that can be used during red teaming engagement. Perfect to setup whitelisted domain for your Cobalt Strike beacon C&C.  It relies on expireddomains.net to obtain a list of expired domains. The domain availability is validated using checkdomain.com
* **Domain Categorization**
	* [ProxyPunch](https://github.com/RythmStick/ProxyPunch)
		* Find website categories whitelisted from Proxy SSL Inspection.
* **Domain Reputation Sites**<a name="dr"></a>
	* [Alien Vault](http://www.alienvault.com)
	* [Isithacked?](http://www.isithacked.com)
	* [Robtex](https://dns.robtex.com)
	* [Scan4You](http://scan4you.net/)
	* [Sucuri](http://sitecheck.sucuri.net/scanner/)
	* [Trustedsource](http://www.trustedsource.org/)
	* [urlQuery](http://urlquery.net/search.php)
	* [URLVoid](http://www.urlvoid.com/scan/)
	* [VirusTotal](https://www.virustotal.com/)
	* [WOT](http://www.mywot.com/en/scorecard)
	* [Zeltser BL](http://zeltser.com)
---------------------------------------------------------------------------------------------------------------------------------

















-------------------------------------------------------------------------------------------------------------------------------
### <a name="egress"></a>Egress/Exfiltration
* **See <a href="Exfiltration.md">Exfiltration.md</a>**
-------------------------------------------------------------------------------------------------------------------------------










	


	
	
	
	


-------------------------------------------------------------------------------------------------------------------------------
### <a name="external"></a> External Attack Surface
* **Credential Stuffing**
	* **Articles/Blogposts/Writeups**
	* **Talks/Presentations/Videos**
		* [Credential Stuffing - Identifying and Fixing your Exposure - Jeff McJunkin( Wild West Hackin' Fest2020)](https://www.youtube.com/watch?v=zHvHsdC2Jqo)
			* Each of us only memorizes a few passwords. Most of your company's employees don't use password managers. Sites get breached. These three statements mean attackers can often get your employees' passwords from other sites (like LinkedIn) and re-use them against your organization to walk in the front door. This talk will define credential stuffing, walk through an example realistic attack, then discuss how you can safely check your own company's exposure and eliminate this risk.
* **Exchange**
	* **Articles/Blogposts/Writeups**
		* [Attacking MS Exchange Web Interfaces - Arseniy Sharoglazov(2020)](https://swarm.ptsecurity.com/attacking-ms-exchange-web-interfaces/)
		* [ProxyLogon(2021)](https://proxylogon.com/)
			* CVE-2021-26855
		* [EWS - InstallApp - Rastamouse](https://rastamouse.me/blog/ews/)
		* [CVE-2020-0688 Microsoft Exchange Remote Code Execution With POC - Stella Sebastian(2021)](https://reconshell.com/cve-2020-0688-microsoft-exchange-remote-code-execution-with-poc/)
	* **Talks/Presentations/Videos**
	* **Tools**
		* [EWSToolkit](https://github.com/rasta-mouse/EWSToolkit)
			* Abusing Exchange via EWS
		* [exchangy](https://github.com/Haxel0rd/haxel0rds/tree/master/tools/exchangy)
			* Exchange Server version & patchlevel detection
* **MS O365**
	* **Articles/Blogposts/Writeups**
		* [Office 365 network attacks - Gaining access to emails and files via an insecure Reply URL  - Dirk-jan Mollema(2019)](https://dirkjanm.io/office-365-network-attacks-via-insecure-reply-url/)
		* [Owning O365 Through Better Brute-Forcing - TrustedSec(2019)](https://www.trustedsec.com/blog/owning-o365-through-better-brute-forcing/)
		* [Achieving Passive User Enumeration with OneDrive - TrustedSec(2020)](https://www.trustedsec.com/blog/achieving-passive-user-enumeration-with-onedrive/)
		* [Obscured by Clouds: Insights into Office 365 Attacks and How Mandiant Managed Defense Investigates - Joseph Hladik, Josh Fleischer(2020)](https://www.fireeye.com/blog/threat-research/2020/07/insights-into-office-365-attacks-and-how-managed-defense-investigates.html)
		* [Making Clouds Rain :: Remote Code Execution in Microsoft Office 365 - Steven Seeley(2021)](https://srcincite.io/blog/2021/01/12/making-clouds-rain-rce-in-office-365.html)
	* **Talks/Presentations/Videos**
	* **Tools**
		* [UhOh365](https://github.com/Raikia/UhOh365)
			* A script that can see if an email address is valid in Office365 (user/email enumeration). This does not perform any login attempts, is unthrottled, and is incredibly useful for social engineering assessments to find which emails exist and which don't. 
		* [onedrive_user_enum](https://github.com/nyxgeek/onedrive_user_enum)
			* pentest tool to enumerate valid onedrive users
		* [365-Stealer](https://github.com/AlteredSecurity/365-Stealer/)
			* [Blogpost](https://www.alteredsecurity.com/post/365-stealer)
			* 365-Stealer is the tool written in python3 which steals data from victims office365 by using access_token which we get by phishing. It steals outlook mails, attachments, OneDrive files, OneNote notes and injects macros. 
		* [Thumbscr-EWS](https://github.com/sensepost/thumbscr-ews)
			* thumbscr-ews is a small Python utility used with Exchange Web Services. Using thumbscr-ews, it is possible to read and search through mail, retrieve the Global Address List, and download attachments. A lot of inspiration taken from MailSniper
* **Monitoring**
	* **Articles/Blogposts/Writeups**
		* [SCANdalous! (External Detection Using Network Scan Data and Automation) - Aaron Stephens, Andrew Thompson(2020)](https://www.fireeye.com/blog/threat-research/2020/07/scandalous-external-detection-using-network-scan-data-and-automation.html)
	* **Talks/Presentations/Videos**
		* [Scant Touch This - Aaron Stephens(2019)](https://www.youtube.com/watch?v=x1tEOkY-7JE)
* **NTLM Hashes**
	* **Articles/Blogposts/Writeups**
		* [Farming for Red Teams: Harvesting NetNTLM - Dominic Chell(2021)](https://www.mdsec.co.uk/2021/02/farming-for-red-teams-harvesting-netntlm/)
	* **Talks/Presentations/Videos**
* **User Enumeration**
	* **Articles/Blogposts/Writeups**
		* [User Enumeration Part 1 – Building Name Lists - Mike Saunders(2020)](https://www.redsiege.com/blog/2020/01/user-enumeration-part-1-building-name-lists/)
		* [User Enumeration Part 2 – Microsoft Office 365 - Mike Saunders(2020)](https://www.redsiege.com/blog/2020/03/user-enumeration-part-2-microsoft-office-365/)
	* **Talks/Presentations/Videos**
* **Other**
	* **Articles/Blogposts/Writeups**
	* **Talks/Presentations/Videos**
		* [#LOL They Placed Their DMZ in the Cloud: Easy Pwnage or Disruptive Protection - Carl Alexander(Derbycon2018)](https://www.irongeek.com/i.php?page=videos/derbycon8/stable-08-lol-they-placed-their-dmz-in-the-cloud-easy-pwnage-or-disruptive-protection-carl-alexander)
			* Uber Did It To Taxis, AirBnB Did It To Hotels, Could External Cloud DMZ Models do it to IT and InfoSec? The perimeter is open, Swiss cheese firewalls, compromised endpoints, vulnerable URLs, malware and ransomware... Things that make pentesting reasonably easy.... What if this all goes away in a new design model that truly limits movement based on simple principals; requiring two factor authentication from everyone, only white listed application connections, and the enabling of Drop all other "All Inbound and Outbound Traffic" Firewall Rules. Sound like a Pentester's nightmare, Welcome to your future.
-------------------------------------------------------------------------------------------------------------------------------





-------------------------------------------------------------------------------------------------------------------------------
##### <a name="hardware"></a>HW Related/Physical Devices/Implants
* **Access**<a name="access"></a>
	* **RDP**
		* [xrdp](https://github.com/neutrinolabs/xrdp)
			* xrdp provides a graphical login to remote machines using Microsoft Remote Desktop Protocol (RDP). xrdp accepts connections from a variety of RDP clients: FreeRDP, rdesktop, NeutrinoRDP and Microsoft Remote Desktop Client (for Windows, Mac OS, iOS and Android).
	* **SSH**
		* [ubuntu.autossh](https://github.com/Monadical-SAS/ubuntu.autossh)
			* Autossh reverse tunnel to central server.
	* **VPN**
		* [Penetration Testing Dropbox Part 2 - VPN Infrastructure - Casey Cammilleri](https://www.sprocketsecurity.com/blog/penetration-testing-dropbox-setup-part2)
		* **Wireguard**
			* [Wireguard - Wikipedia](https://en.wikipedia.org/wiki/Wireguard)
				* WireGuard is a free and open-source software application and communication protocol that implements virtual private network (VPN) techniques to create secure point-to-point connections in routed or bridged configurations. It is run as a module inside the Linux kernel, and aims for better performance and more power saving than the IPsec and OpenVPN tunneling protocols. It was written by Jason A. Donenfeld and is published under the GNU General Public License (GPL) version 2.
			* [wg-access-server](https://github.com/place1/wg-access-server/)
				* wg-access-server is a single binary that provides a WireGuard VPN server and device management web ui. We support user authentication, 1 click device registration that works with Mac, Linux, Windows, Ios and Android including QR codes. You can configure different network isolation modes for better control and more. This project aims to deliver a simple VPN solution for developers, homelab enthusiasts and anyone else feeling adventurous.
* **Dropboxes**<a name="dropboxes"></a>
	* **Articles/Blogpots/Writeups**
		* [A list of current UMPCs with physical keyboard - ciko.io(2019)](https://ciko.io/posts/umpc/)
		* [Making the Perfect Red Team Dropbox (Part 1) - Rogan Dawes(2020)](https://sensepost.com/blog/2020/making-the-perfect-red-team-dropbox-part-1/)
			* [Part 2](https://sensepost.com/blog/2020/making-the-perfect-red-team-dropbox-part-2/)
		* [How to Build a Pentest Dropbox - TheCyberMentor(2020)](https://www.youtube.com/watch?v=D2t4ADQnBEk)
		* [DigiDucky - How to setup a Digispark like a rubber ducky](http://www.redteamr.com/2016/08/digiducky/)
		* [Bash Bunny](https://hakshop.com/products/bash-bunny)
		* [How to Build Your Own Penetration Testing Drop Box - BHIS](https://www.blackhillsinfosec.com/?p=5156&)
		* [Create an Encrypted Leave-Behind Device - Andy(warroom2016)](https://warroom.rsmus.com/encrypted-leave-behind/)
	* **Talks/Presentations/Videos**
		* [Shells on Cells - Tj McClerain(ShellCon2018)](https://www.youtube.com/watch?v=tRytvE6WCyY&list=PL7D3STHEa66TbZwq9w3S2qWzoJeNo3YYN&index=4)
			* For my talk I'll be going into how to setup a Raspberry Pi Zero W with a Cellular modem to provide out of band persistence inside a target network for the purpose of using it as a pen test drop box. On the technical side of things I'll provide a hardware summary and demo along with code examples to get it all working.
		* [an Implantable Computer - Doug "c00p3r" Copeland(Circle City Con 2019)](https://www.irongeek.com/i.php?page=videos/circlecitycon2019/track-1-07-an-implantable-computer-doug-c00p3r-copeland)
			* fast prototyping an implantable computer from off the shelf parts, there are two phases to this project phase 1 is making a fast prototype from off the shelf parts, and implanting it into a host, this is meant to be a proof of concept for the implantable computer which is able to sniff wifi, bluetooth, and nfc from within the human body... allow the hacker to remote into the computer/host and gather information from a possible distributed array of people involved in the test. phase 2 is to take what is learned and create a custom pcb with all that has been learned from the original design and to create a smaller more compact form factor for the design... currently me and my team are in 5th official revision of phase 1 of this project... unofficially more like the 20th revision. The purpose of the talk is to do more then get up and say i built this thing and it does this, but instead to have a conversation about the process of fast proto-typing and to encourage others that may or may not have an idea to try building something themselves, and create their own DIY evolution! 
	* **Tools**
		* [P4wnP1](https://github.com/mame82/P4wnP1)
			* P4wnP1 is a highly customizable USB attack platform, based on a low cost Raspberry Pi Zero or Raspberry Pi Zero W.
* **Physical Implants**<a name="pimplants"></a>
	* **Articles/Writeups**
		* [Programmable HID USB Keystroke Dongle: Using the Teensy as a pen testing device - Adrian Crenshaw(2010)](https://www.irongeek.com/i.php?page=security/programmable-hid-usb-keystroke-dongle)
			* [Slides](https://www.defcon.org/images/defcon-18/dc-18-presentations/Crenshaw/DEFCON-18-Crenshaw-PHID-USB-Device.pdf)
		* [Implanting a Dropcam](https://www.defcon.org/images/defcon-22/dc-22-presentations/Moore-Wardle/DEFCON-22-Colby-Moore-Patrick-Wardle-Synack-DropCam-Updated.pdf)
		* [USBSamurai: how to make a remote controlled USB HID injecting cable for less than 10$ - Andrea Fortuna(2019)](https://andreafortuna.org/2019/08/21/usbsamurai-how-to-make-a-remote-controlled-usb-hid-injecting-cable-for-less-than-10/)
	- **Talks/Presentations**
		* [Hacking with Hardware: Introducing the Universal RF USB Keyboard Emulation Device - URFUKED(Defcon18)](https://www.youtube.com/watch?v=613BImjheoM)
			* [Slides](https://www.defcon.org/images/defcon-18/dc-18-presentations/Elkins/DEFCON-18-Elkins-Universal-RF-Keyboard.pdf)
		* [Hardware Backdooring is Practical - Jonathan Brossard(Defcon20)](https://www.youtube.com/watch?v=MqbvxrJqrPU)
			* [Slides](https://www.defcon.org/images/defcon-20/dc-20-presentations/Brossard/DEFCON-20-Brossard-Hardware-Backdooring-is-Practical.pdf)
			* [Paper](https://www.defcon.org/images/defcon-20/dc-20-presentations/Brossard/DEFCON-20-Brossard-Hardware-Backdooring-is-Practical-WP.pdf)
			* This presentation will demonstrate that permanent backdooring of hardware is practical. We have built a generic proof of concept malware for the intel architecture, Rakshasa, capable of infecting more than a hundred of different motherboards. The first net effect of Rakshasa is to disable NX permanently and remove SMM related fixes from the BIOS, resulting in permanent lowering of the security of the backdoored computer, even after complete earasing of hard disks and reinstallation of a new operating system. We shall also demonstrate that preexisting work on MBR subvertions such as bootkiting and preboot authentication software bruteforce can be embedded in Rakshasa with little effort. More over, Rakshasa is built on top of free software, including the Coreboot project, meaning that most of its source code is already public. This presentation will take a deep dive into Coreboot and hardware components such as the BIOS, CMOS and PIC embedded on the motherboard, before detailing the inner workings of Rakshasa and demo its capabilities. It is hoped to raise awareness of the security community regarding the dangers associated with non open source firmwares shipped with any computer and question their integrity. This shall also result in upgrading the best practices for forensics and post intrusion analysis by including the afore mentioned firmwares as part of their scope of work.
	* **Papers**
		* [Stealthy Dopant-Level Hardware Trojans](http://sharps.org/wp-content/uploads/BECKER-CHES.pdf)
			* Abstract: In this paper we propose an extremely stealthy approach for implementing hardware Trojans below the gate level, and we evaluate their impact on the security of the target device. Instead of adding additional circuitry to the target design, we insert our hardware Trojans by changing the dopant polarity of existing transistors. Since the modied circuit ap- pears legitimate on all wiring layers (including all metal and polysilicon), our family of Trojans is resistant to most detection techniques, including negrain optical inspection and checking against \golden chips". We demonstrate the e ectiveness of our approach by inserting Trojans into two designs | a digital post-processing derived from Intel's cryptographically secure RNG design used in the Ivy Bridge processors and a side-channel resistant SBox implementation | and by exploring their detectability and their effects on security.
		* [Implementation and Implications of a Stealth Hard-Drive Backdoor](https://www.ibr.cs.tu-bs.de/users/kurmus/papers/acsac13.pdf) 
			* Modern workstations and servers implicitly trust hard disks to act as well-behaved block devices. This paper analyzes the catastrophic loss of security that occurs when hard disks are not trustworthy. First, we show that it is possible to compromise the firmware of a commercial ovt-the-shelf hard drive, by resorting only to public information and reverse engineering. Using such a compromised firmware, we present a stealth rootkit that replaces arbitrary blocks from the disk while they are written, providing a data replacement back- door . The measured performance overhead of the compromised disk drive is less than 1% compared with a normal, non-malicious disk drive. We then demonstrate that a re- mote attacker can even establish a communication channel with a compromised disk to infiltrate commands and to ex-filtrate data. In our example, this channel is established over the Internet to an unmodified web server that relies on the compromised drive for its storage, passing through the original webserver, database server, database storage engine, filesystem driver, and block device driver. Additional experiments, performed in an emulated disk-drive environment, could automatically extract sensitive data such as /etc/shadow (or a secret key le) in less than a minute. This paper claims that the diffculty of implementing such an at- tack is not limited to the area of government cyber-warfare; rather, it is well within the reach of moderately funded criminals, botnet herders and academic researchers.
		* [Inside a low budget consumer hardware espionage implant](https://ha.cking.ch/s8_data_line_locator/)
	* **HID**
		* [What are malicious usb keys and how to create a realistic one? - Elie Bursztein(2016)](https://elie.net/blog/security/what-are-malicious-usb-keys-and-how-to-create-a-realistic-one/)
		* **Talks/Presentations**
			* [The Rise Of Evil HID Devices - Franck Bitsch and Arthur Villeneuve(GreHack 2019)](https://www.youtube.com/watch?v=Qhfqr3io3uw)
				* Our talk will present the principle of malicious HID attack with its strengths and weaknesses. Three USB devices that can be used to launch an attack will be compared: a "rubber ducky", the WHID Injector device and the USBNinja cable. We will present the results of forensic analyses performed on corporate computers after our Redteam launched attacks using the previously introduced USB devices. We will focus on the traces left by these devices at the operating system level (event logs of interest, USB traces ...) and the data exfiltration techniques that can be used during this type of attack. We will introduce a principle of hardware investigation and how to locate interface pinout to try to dump the content of the suspicious device to analyse its “malicious” capabilities.
		* **Teensy**
			* [USB teensy attack set OSX](http://samy.pl/usbdriveby/)
			* [Paensy](https://github.com/Ozuru/Paensy)
				* Paensy is a combination of the word payload and Teensy - Paensy is an attacker-oriented library written for the development of Teensy devices. Paensy simplifies mundane tasks and allows an easier platform for scripting.
				* [Blogpost](http://malware.cat/?p=89)
	* **Tooling**
		* * [USBSamurai — A Remotely Controlled Malicious USB HID Injecting Cable for less than 10$ - Luca Bongiorni](https://medium.com/@LucaBongiorni/usbsamurai-a-remotely-controlled-malicious-usb-hid-injecting-cable-for-less-than-10-ebf4b81e1d0b)
		* [USBsamurai For Dummies - Luca Bongiorni](https://medium.com/@LucaBongiorni/usbsamurai-for-dummies-4bd47abf8f87)
		* [whid-31337](https://github.com/whid-injector/whid-31337)
			* WHID Elite is a GSM-enabled Open-Source Multi-Purpose Offensive Device that allows a threat actor to remotely inject keystrokes, bypass air-gapped systems, conduct mousejacking attacks, do acoustic surveillance, RF replay attacks and much more.
		* [WiFiDuck](https://github.com/spacehuhn/WiFiDuck)
			* Wireless keystroke injection attack platform
		* [Caligo](https://github.com/secgroundzero/caligo)
			* Caligo is a simple C2 for hostile "dropbox" devices management used in physical security assessments. We have been using drop devices for a long time now but we never had an easy way to manage them especially when running multiple engagements at the same time with multiple devices for each. Caligo solves this problem by providing a client and server setup script which allows the user to control all of the devices from a web application.
			* [Blogpost](http://www.offensiveops.io/tools/project-caligo/)
		* [Smuggle Bus](https://github.com/CroweCybersecurity/smugglebus)
			* SmuggleBus is a Crowe developed USB bootable tool, built on a bare-bones Linux OS. It was designed to aid penetration testers and red teamers performing physical social engineering exercises.
		* [Int3rcept0r](https://github.com/unknwncharlie/Int3rcept0r)
			* Raspberry Pi Zero USB to Ethernet adapter MITM Gadget similar to the Lan Turtle
		* [Rubber Ducky on MacOS - Chad Duffey(2021)](https://www.chadduffey.com/2021/03/Rubber-Ducky-On-MacOS.html)
* **Other**
	* [PentestHardware](https://github.com/unprovable/PentestHardware)
		* Kinda useful notes collated together publicly	
	* [PhanTap (Phantom Tap)](https://github.com/nccgroup/phantap)
		* PhanTap is an ‘invisible’ network tap aimed at red teams. With limited physical access to a target building, this tap can be installed inline between a network device and the corporate network. PhanTap is silent in the network and does not affect the victim’s traffic, even in networks having NAC (Network Access Control 802.1X - 2004). PhanTap will analyze traffic on the network and mask its traffic as the victim device. It can mount a tunnel back to a remote server, giving the user a foothold in the network for further analysis and pivoting. PhanTap is an OpenWrt package and should be compatible with any device. The physical device used for our testing is currently a small, inexpensive router, the GL.iNet GL-AR150. You can find a detailed blogpost describing PhanTap [here](https://www.nccgroup.trust/us/our-research/phantap/?research=Public+tools)
	* [Tinyduck](https://github.com/justcallmekoko/Tinyduck)
		* The super tiny USB Rubber Ducky
-------------------------------------------------------------------------------------------------------------------------------























	


	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	

-------------------------------------------------------------------------------------------------------------------------------
### <a name="infra"></a>Infrastructure
* **101**<a name="i101"></a>
	* [Red Team Infrastructure Wiki](https://github.com/bluscreenofjeff/Red-Team-Infrastructure-Wiki)
		* Wiki to collect Red Team infrastructure hardening resources
		* Accompanying Presentation: [Doomsday Preppers: Fortifying Your Red Team Infrastructure](https://speakerdeck.com/rvrsh3ll/doomsday-preppers-fortifying-your-red-team-infrastructure)
	* [6 RED TEAM INFRASTRUCTURE TIPS](https://cybersyndicates.com/2016/11/top-red-team-tips/)
* **Articles & Writeups**<a name="iarticles"></a>
	* [Designing Effective Covert Red Team Attack Infrastructure - Jeff Dimmock](https://posts.specterops.io/designing-effective-covert-red-team-attack-infrastructure-767d4289af43)
	* [Building a Better Moat: Designing an Effective Covert Red Team Attack Infrastructure - @bluescreenofjeff](https://speakerdeck.com/bluscreenofjeff/building-a-better-moat-designing-an-effective-covert-red-team-attack-infrastructure)
	* [Infrastructure for Ongoing Red Team Operations - CS(2014)](https://blog.cobaltstrike.com/2014/09/09/infrastructure-for-ongoing-red-team-operations/)
	* [How to Build a C2 Infrastructure with Digital Ocean – Part 1](https://www.blackhillsinfosec.com/build-c2-infrastructure-digital-ocean-part-1/)
	* [Reverse HTTPS meterpreter behind Apache (or any other reverse SSL proxy) - Konrāds Klints(2016)](https://medium.com/@truekonrads/reverse-https-meterpreter-behind-apache-or-any-other-reverse-ssl-proxy-e898f9dfff54)
	* [Automated Red Team Infrastructure Deployment with Terraform - Part 1(2017)](https://rastamouse.me/2017/08/automated-red-team-infrastructure-deployment-with-terraform---part-1/)
	* [Migrating Your infrastructure](https://blog.cobaltstrike.com/2015/10/21/migrating-your-infrastructure/)
	* [Route 53 as Pentest Infrastructure - Jared Perry(2018)](https://blog.stratumsecurity.com/2018/10/17/route-53-as-a-pentest-infrastructure/)
	* [Automating Red Team Infrastructure with Terraform - @spottheplanet](https://ired.team/offensive-security/red-team-infrastructure/automating-red-team-infrastructure-with-terraform)
	* [Modern C2 Infrastructure with Terraform, DigitalOcean, Covenant and Cloudflare - Riccardo](https://riccardoancarani.github.io/2019-09-28-modern-c2-infra/)
	* [Testing your RedTeam Infrastructure - Adam Chester(2020)](https://blog.xpnsec.com/testing-redteam-infra/)
		* In this post I'm going to start with a quick review of how RedTeam infrastructure is defined in code which would typically live in a Git repo somewhere. More importantly however, we will continue this by looking at ways in which our environments can be tested as they evolve and increase in complexity, finishing with a walkthrough of how we can introduce a CI pipeline into the mix to help automate this testing.
	* [Modern Red Team Infrastructure - Brady Bloxham(2019)](https://silentbreaksecurity.com/modern-red-team-infrastructure/)
	* [Praetorian's Approach to Red Team Infrastructure - Adam Crosser(2020)](https://www.praetorian.com/blog/praetorians-approach-to-red-team-infrastructure)
	* [Automating red team infrastructure with Ansible part 1 – Raw infrastructure - Jean Maes(2020)](https://redteamer.tips/automating-red-team-infrastructure-with-ansible-part-1-raw-infrastructure/)
	* [Praetorian’s Approach to Red Team Infrastructure - Adam Crosser(2020)](https://www.praetorian.com/blog/praetorians-approach-to-red-team-infrastructure/)
	* [Taking the pain out of C2 infrastructure (Part 2) - Modernizing the CIA's operational infrastructure. Multi/Hybrid Cloud Docker Swarm clusters and mesh VPN networks 🐿(Marcello(2021)](https://byt3bl33d3r.substack.com/p/taking-the-pain-out-of-c2-infrastructure-3c4?r=jt535)
* **Talks/Presentations/Videos**
	* [Service Cloaking and Anonymous Access; Combining Tor with Single Packet Authorization (SPA) - Michael Rash(Defcon14)](https://www.youtube.com/watch?v=Cbiojmk_N9E)
		* [Slides](https://www.defcon.org/images/defcon-14/dc-14-presentations/DC-14-Rash.pdf)
		* "Single Packet Authentication is becoming an increasingly important method for protecting arbitrary network services through the use of a kernel level filtering mechanism such as Netfilter in the Linux kernel. By sending SPA packets over the Tor network, SPA packets can be endowed with an additional layer of privacy and anonymity. It becomes cryptographically difficult to deduce the communication of the SPA packet from any particular source address; even from the perspective of an attacker that is in the enviable position to montior all packets going to and leaving from the SPA client system. The end result it that the exploitation of even 0-day vulnerabilities in a service that is protected with SPA/Tor is much more difficult. This talk will focus on applied aspects of Single Packet Authentication, and will include a lengthy demonstration at the beginning of the talk. A new version of the Single Packet Authentication software "fwknop" will also be released contains new features such as GPG-hardened last-hop IP resolution, a web interface to monitor SPA usage in an Enterprise environment, remote Netfilter policy management, and more.
	* [Offensive Development: How To DevOps Your Red Team - Dominic Chell(BSidesMCR2019)](https://www.youtube.com/watch?v=n5_V61NI0tA)
		* During this talk we will explore how DevOps principles can be applied to red teaming, focusing on the implementation of a custom CI/CD pipeline to automatically consume, build and deploy existing and custom tooling to an environment in a manner agnostic to any command and control framework.   We will explain how this approach can not only significantly reduce indicators of compromise, but also introduce the capability to programmatically and automatically protect all your tools from DFIR. Following the talk, we will release redpipe, a custom CI/CD pipeline developed by MDSec for use during red team engagements. The future of red teaming is offensive development.
* **HW/SW for Remote Testing**<a name="remote-testing"></a>
	* [Trusted Attack Platform - TrustedSec](https://github.com/trustedsec/tap)
		* TAP is a remote penetration testing platform builder. For folks in the security industry, traveling often times becomes a burden and adds a ton of cost to the customer. TAP was designed to make the deployment of these boxes super simple and create a self-healing and stable platform to deploy remote penetration testing platforms. Essentially the concept is simple, you pre-configure a brand new box and run the TAP setup file. This will install a service on Linux that will be configured the way you want. What it will do is establish a reverse SSH tunnel back to a machine thats exposed on the Internet for you. From there you can access the box locally from the server it connects back to. TAP automatically detects when an SSH connection has gone stale and will automatically rebuild it for you.
	* [Red Team Laptop & Infrastructure (pt 1: Architecture) - hon1nbo](https://hackingand.coffee/2018/02/assessment-laptop-architecture/)
* **Logging & Monitoring**<a name="ilm"></a>
	 **101**
		* [Red Team Telemetry Part 1 - Zach Grace](https://zachgrace.com/posts/red-team-telemetry-part-1/)
		* [Attack Infrastructure Log Aggregation and Monitoring](https://posts.specterops.io/attack-infrastructure-log-aggregation-and-monitoring-345e4173044e)
		* [Pentest / Red Team Audit Logging - Mubix](https://www.youtube.com/watch?v=DYHadkG9iFg)
		* [Azure Web App Service For Offensive Operations - Stephan Borosh(2020)](https://www.trustwave.com/en-us/resources/blogs/spiderlabs-blog/azure-web-app-service-for-offensive-operations/)
	* **Talks/Presentations/Videos**
		* [How do I detect technique X in Windows?? Applied Methodology to Definitively Answer this Question - Matt Graeber(Derbycon 2019)](http://www.irongeek.com/i.php?page=videos/derbycon9/1-05-how-do-i-detect-technique-x-in-windows-applied-methodology-to-definitively-answer-this-question-matt-graeber)
			* Traditionally, the answer to this question has been to execute an attack technique in a controlled environment and to observe relevant events that surface. While this approach may suffice in some cases, ask yourself the following questions: ?Will this scale? Will this detect current/future variants of the technique? Is this resilient to bypass?? If your confidence level in answering these questions is not high, it?s time to consider a more mature methodology for identifying detection data sources. With a little bit of reverse engineering, a defender can unlock a multitude of otherwise unknown telemetry. This talk will establish a methodology for identifying detection data sources and will cover concepts including Event Tracing for Windows, WPP, TraceLogging, and security product analysis.
	 	* [Who watches the watchmen? Adventures in red team infrastructure herding and blue team OPSEC failures - Mark Bergman, Marc Smeets(HIP19)](https://www.youtube.com/watch?v=ZezBCAUax6c)
			* In this talk we explain our approach for red team infrastructure herding and using that to bust OPSEC failures of blue teams. We discuss our latest research on this topic and present a new version of our opensource tooling RedELK. 
	 	* [Using blue team techniques in red team ops - Mark Bergman & Marc Smeets(BruCON 0x0A)](https://www.youtube.com/watch?v=OjtftdPts4g)
			* When performing multi-month, multi-C2teamserver and multi-scenario red team operations, you are working with an infrastructure that becomes very large quickly. This makes it harder to keep track of what is happening on it. Coupled with the ever-increasing maturity of blue teams, this makes it more likely the blue team is somewhere analysing parts of your infra and/or artefacts. In this presentation we’ll show you how you can use that to your advantage. We’ll present different ways to keep track of the blue team’s analyses and detections, and to dynamically adjust your infra to fool the blue team. We will first set the scene by explaining common and lesser known components of red teaming infrastructures, e.g. dynamic redirectors, domain fronting revisited, decoy websites, html-smuggling, etc. Secondly, we’ll show how to centralize all your infrastructure’s and ops’ information to an ELK stack, leaving it open for intelligent querying across the entire infrastructure and operation. This will also help with better feedback to the blue team at the end of the engagement. Lastly, we’ll dive into novel ways of detecting a blue team’s investigation and we’ll give examples on how to react to these actions, for example by creating honeypots for the blue team.
	 * **Tools**
	 	* [unindexed](https://github.com/mroth/unindexed/blob/master/README.md)
			* The site is constantly searching for itself in Google, over and over and over, 24 hours a day. The instant it finds itself in Google search results, the site will instantaneously and irrevocably securely delete itself. Visitors can contribute to the public content of the site, these contributions will also be destroyed when the site deletes itself.
	 * **RedELK**
		* [RedELK](https://github.com/outflanknl/RedELK)
			* Red Team's SIEM - tool for Red Teams used for tracking and alarming about Blue Team activities as well as better usability for the Red Team in long term operations.
		* [Introducing RedELK – Part 1: why we need it - Marc Smeets(2019)](https://outflank.nl/blog/2019/02/14/introducing-redelk-part-1-why-we-need-it/)
			* [Part 2 – getting you up and running - Marc Smeets(2020)](https://outflank.nl/blog/2020/02/28/redelk-part-2-getting-you-up-and-running/)
			* [Part 3 – Achieving operational oversight - Marc Smeets(2020)](https://outflank.nl/blog/2020/04/07/redelk-part-3-achieving-operational-oversight/)
		* [Automating a RedELK Deployment Using Ansible - Jason Lang(2020)](https://www.trustedsec.com/blog/automating-a-redelk-deployment-using-ansible/)
	* **Other Setups**
		* [RedTeamSiem](https://github.com/SecurityRiskAdvisors/RedTeamSIEM)
			* Repository of resources for configuring a Red Team SIEM using Elastic
		* [VECTR](https://github.com/SecurityRiskAdvisors/VECTR)
			* VECTR is a tool that facilitates tracking of your red and blue team testing activities to measure detection and prevention capabilities across different attack scenarios. VECTR provides the ability to create assessment groups, which consist of a collection of Campaigns and supporting Test Cases to simulate adversary threats. Campaigns can be broad and span activity across the kill chain, from initial compromise to privilege escalation and lateral movement and so on, or can be a narrow in scope to focus on specific detection layers, tools, and infrastructure. VECTR is designed to promote full transparency between offense and defense, encourage training between team members, and improve detection & prevention success rate across the environment.
- **Proxies**
	- **Articles**
		* [Keep your eyes open: How to avoid exposing your internal proxy - Flant(2020)](https://medium.com/flant-com/stop-exposing-your-internal-proxy-dfdb7e5faff5)
		* [Design and setup of C2 traffic redirectors - Dmitrijs Trizna(2021)](https://ditrizna.medium.com/design-and-setup-of-c2-traffic-redirectors-ec3c11bd227d)
	- **DNS**
	- **gRPC**
		* [grpc-gateway](https://github.com/grpc-ecosystem/grpc-gateway)
			* gRPC to JSON proxy generator following the gRPC HTTP spec
	- **HTTP**
	- **Reverse**
		* [rathole](https://github.com/rapiz1/rathole)
			* A lightweight and high-performance reverse proxy for NAT traversal, written in Rust. An alternative to frp and ngrok.
* **Web Server**<a name="iws"></a>
	* **Apache**
		- **mod_rewrite**
			* [Apache Module mod_rewrite](https://httpd.apache.org/docs/2.4/mod/mod_rewrite.html)
			* [Apache Mod_Rewrite Terrafrom Automation](https://github.com/cedowens/Mod_Rewrite_Automation)
				* Scripts to automate standing up apache2 with mod_rewrite in front of C2 servers.
	* **Caddy**
		- **101**
			* [Download](https://caddyserver.com/download)
			* [Documentation](https://caddyserver.com/docs/)
		- **Articles/Blogposts**
			* [Taking the pain out of C2 Infrastructure (Part 1) - Marcello(2021](https://byt3bl33d3r.substack.com/p/taking-the-pain-out-of-c2-infrastructure)
			* [Staging Cobalt Strike with mTLS using Caddy - Nichlas Falk(2022)](https://improsec.com/tech-blog/staging-cobalt-strike-with-mtls-using-caddy)
				* [Code](https://github.com/improsec/CaddyStager)
	* **Nginx**
		* [nginx: Send HTTP User Agent Requests To Specific Backend Server - Vivek Gite(2010)](https://www.cyberciti.biz/faq/nginx-if-conditional-http_user_agent-requests/)	
		* [Resilient Red Team HTTPS Redirection Using Nginx - Adam Brown(2018)](https://coffeegist.com/security/resilient-red-team-https-redirection-using-nginx/)
	* **Routing**
		* **Articles/Blogposts/Writeups**
			* [Introduction To Modern Routing For Red Team Infrastructure - using Traefik, Metasploit, Covenant and Docker]
			* [Hosting and hiding your C2 with Docker and Socat - khast3x(2020)](https://khast3x.club/posts/2020-02-09-C2-Protection-Socat-Docker/)
			* [AWS Lambda Redirector - Adam Chester(2020)](https://blog.xpnsec.com/aws-lambda-redirector/)
			* [Redirecting Cobalt Strike DNS Beacons](http://www.rvrsh3ll.net/blog/offensive/redirecting-cobalt-strike-dns-beacons/)
			* [High-reputation Redirectors and Domain Fronting](https://blog.cobaltstrike.com/2017/02/06/high-reputation-redirectors-and-domain-fronting/)
			* [Cobalt Strike HTTP C2 Redirectors with Apache mod_rewrite - Jeff Dimmock](https://bluescreenofjeff.com/2016-06-28-cobalt-strike-http-c2-redirectors-with-apache-mod_rewrite/)
			* [HTTP Forwarders / Relays - @spottheplanet](https://ired.team/offensive-security/red-team-infrastructure/redirectors-forwarders)
				* Concealing attacking hosts through with redirectors/traffic forwarders using iptables or socat
			* [Resilient Red Team HTTPS Redirection Using Nginx - Adam Brown(2018)](https://coffeegist.com/security/resilient-red-team-https-redirection-using-nginx/)
			* [Azure Functions - Functional Redirection - FortyNorthSecurity(2020)](https://fortynorthsecurity.com/blog/azure-functions-functional-redirection/)
		* **Samples/Setups**
			* [Apache2Mod Rewrite Setup](https://github.com/n0pe-sled/Apache2-Mod-Rewrite-Setup)
		* **Tools**
			* [Expose](https://github.com/beyondcode/expose)
				* A completely open-source ngrok alternative - written in pure PHP.
			* [Traefik](https://github.com/containous/traefik)
			* [FlaskRedirectorProtector](https://github.com/rvrsh3ll/FlaskRedirectorProtector)
				* Protect your servers with a secret header
	* **BlockRules**
		* **Tools**
			* [redirect.rules](https://github.com/0xZDH/redirect.rules)
				* Quick and dirty dynamic redirect.rules generator
			* [mkhtaccess_red](https://github.com/violentlydave/mkhtaccess_red)
				* Auto-generate an HTaccess for payload delivery -- automatically pulls ips/nets/etc from known sandbox companies/sources that have been seen before, and redirects them to a benign payload.
			 * [Sephiroth](https://github.com/0xdade/sephiroth)
				* A Python3 script to build cloud block lists for servers.
			* [RT-CyberShield](https://github.com/op7ic/RT-CyberShield)
				* Protecting Red Team infrastructure with cyber shield blocking AWS/AZURE/IBM/Digital Ocean/TOR/AV IP/ETC. ranges 
* **SSL/TLS**
	* **JA3**
		* [Impersonating JA3 Fingerprints - Matthew Rinaldi](https://medium.com/cu-cyber/impersonating-ja3-fingerprints-b9f555880e42)
		* [JA3Transport](https://github.com/CUCyber/ja3transport)
			* A Go library that makes it easy to mock JA3 signatures.
* **Automation Tooling**<a name="iat"></a>
	* [Abaddon](https://github.com/wavestone-cdt/abaddon)
		* Red team operations involve miscellaneous skills, last several months and are politically sensitive; they require a lot of monitoring, consolidating and caution. Wavestone’s red team operations management software, Abaddon, has been designed to make red team operations faster, more repeatable, stealthier, while including value-added tools and bringing numerous reporting capabilities.
	* [Paragon](https://github.com/KCarretto/paragon)
		* Paragon is a Red Team engagement platform. It aims to unify offensive tools behind a simple UI, abstracting much of the backend work to enable operators to focus on writing implants and spend less time worrying about databases and css. The repository also provides some offensive tools already integrated with Paragon that can be used during engagements.
	* [SiestaTime](https://github.com/rebujacker/SiestaTime)
		* Red Team Automation tool powered by go and terraform.
		* [SiestaTime, Automation tool for Generation of Implants, Infrastructure and Reports - ](https://www.youtube.com/watch?v=3oAEO0eeiEI&list=PL7D3STHEa66QvxwnM8MSf8tUq1Zkhoq4P&index=21)
	* [Redcloud](https://github.com/khast3x/Redcloud)
		* Automated Red Team Infrastructure deployement using Docker 
	* [Red Baron](https://github.com/Coalfire-Research/Red-Baron)
		* Red Baron is a set of modules and custom/third-party providers for Terraform which tries to automate creating resilient, disposable, secure and agile infrastructure for Red Teams.
	* [RedTeam-Automation - bneg](https://github.com/bneg/RedTeam-Automation)
		* Automating those tasks which can or should be automated
	* [Red Team Hosted Infrastructure](https://github.com/redteaminfra/redteam-infra)
		* This project houses reference deployment recipies that can be used to build Red Team Infrastructure. As such, there are no security guarantees or promises. Use at your own risk. This infrastructure was discussed at CanSecWest 2019 and the slides can be found [here](https://speakerdeck.com/tophertimzen/attack-infrastructure-for-the-modern-red-team)
	* [Harvis](https://github.com/thiagomayllart/Harvis)
		* Harvis is a python tool to help you create multiple hauls for a specific operation during a red team engagement. It can automatically create your C2 machine, redirector machine, setup SSL, .htaccess configuration, firewall rules and more. Harvis also has the purpose of automating the job of the operator of identifying burned domains/redirectors that may be caught during the operation. After identifying the burned domains it provides the possibility of rotating the infrastructure, setting up different redirectors and atributing a different domain.
	* [Ansible-Red-EC2](https://github.com/jfmaes/Red-EC2)
		* Deploy RedTeam Specific EC2 via ansible.
	* [Overlord](https://github.com/qsecure-labs/overlord)
		* Overlord provides a python-based console CLI which is used to build Red Teaming infrastructure in an automated way. The user has to provide inputs by using the tool’s modules (e.g. C2, Email Server, HTTP web delivery server, Phishing server etc.) and the full infra / modules and scripts will be generated automatically on a cloud provider of choice. Currently supports AWS and Digital Ocean. The tool is still under development and it was inspired and uses the Red-Baron Terraform implementation found on Github.
	* [RedBoto](https://github.com/elitest/Redboto)
 		* Redboto is a collection of scripts that use the Amazon SDK for Python boto3 to perform red team operations against the AWS API.
	* [RedCommander](https://github.com/GuidePointSecurity/RedCommander)
		* [Introducing Red Commander: A GuidePoint Security Open Source Project - Alex Williams(2020)]
	* [Rapid Attack Infrastructure (RAI)](https://github.com/obscuritylabs/RAI)
		* With a RAI deployment, it can all be done in roughly `~1 hour`. This includes everything from your Teamserver (CobaltStrike), redirectors to Phishing Servers with full DKIM, DMARC, SPF, etc.
	* [Boomerang](https://github.com/paranoidninja/Boomerang)
		* Boomerang is a tool to expose multiple internal servers to web/cloud. Agent & Server are pretty stable and can be used in Red Team for Multiple levels of Pivoting and exposing multiple internal services to external/other networks
	* [Sephiroth](https://github.com/0xdade/sephiroth)
		* A Python3 script to build cloud block lists for servers.
* **Wireless**<a name="iw"></a>
	* [Rogue Toolkit](https://github.com/InfamousSYN/rogue)
		* The Rogue Toolkit: An extensible toolkit aimed at providing penetration testers an easy-to-use platform to deploy Access Points for the purpose of conducting penetration testing and red team engagements.
-------------------------------------------------------------------------------------------------------------------------------












































	
	
	

-------------------------------------------------------------------------------------------------------------------------------
### <a name="implantdev"></a>Implant & Payload Development
* **Creation & Development**<a name="pcd"></a>
	* **101**
		* [Matasano Security Recommendation #001: Avoid Agents - Thomas Ptacek(2006)](https://web.archive.org/web/20061215050427/http://www.matasano.com/log/646/matasano-security-recommendation-001-avoid-agents/)
		* [My making of a Metasploit Module - Aaron Ringo(NolaCon2019)](https://www.irongeek.com/i.php?page=videos/nolacon2019/nolacon-2019-c-11-my-making-of-a-metasploit-module-aaron-ringo)
			* Metasploit is one of the most well-known security products on the market. Not being a paid developer I had never used github for collaboration and had a lot to learn. I'll be discussing my motivation for making a module, the process, and pick up where some of the documentation left off.
		* [What is a stageless payload artifact? - Raphael Mudge(2016)](https://blog.cobaltstrike.com/2016/06/15/what-is-a-stageless-payload-artifact/)
		* [Vault7 Leaks: Development Tradecraft DOs and DON'Ts](https://wikileaks.org/ciav7p1/cms/page_14587109.html)
	* **Articles/Blogposts/Writeups**
		* [Software Development Principals for Offensive Developers — Part 1 (Fundamentals) - James(2020)](https://web.archive.org/web/20200219060000/https://medium.com/@two06/software-development-principals-for-offensive-developers-part-1-fundamentals-7293d2ad0bde)
		* [Pentest-and-Development-Tips - 3gstudent](https://github.com/3gstudent/Pentest-and-Development-Tips/blob/master/README-en.md)
		* [Red Team Diary, Entry #3: Custom Malware Development (Establishing A Shell Through the Target’s Browser) - Dimitrios Bougioukas](https://blog.usejournal.com/red-team-diary-entry-3-custom-malware-development-establish-a-shell-through-the-browser-bed97c6398a5)
		* [Red Team Diary, Entry #1: Making NSA’s PeddleCheap RAT Invisible - Dimitrios Bougioukas](https://medium.com/@d.bougioukas/red-team-diary-entry-1-making-nsas-peddlecheap-rat-invisible-f88ccbdc484d)
			* [Slides](https://drive.google.com/file/d/1xBwMuF62eYKv3A2TNRgKNVE_nAViSrVZ/view)
		* [Malware development part 1 - 0xPat](https://0xpat.github.io/Malware_development_part_1/)
			* [Part 2](https://0xpat.github.io/Malware_development_part_2/)
			* [Part 3](https://0xpat.github.io/Malware_development_part_3/)	
		* [Tutorial: Creating a custom full featured implant(Nuages)](https://github.com/p3nt4/Nuages/wiki/Tutorial:-Creating-a-custom-full-featured-implant)
		* [Software Development Principals for Offensive Developers — Part 1 (Fundamentals) - James(2020)](https://medium.com/@two06/software-development-principals-for-offensive-developers-part-1-fundamentals-7293d2ad0bde)
			* [Part 2](https://medium.com/@two06/software-development-principals-for-offensive-developers-part-2-adapters-59fcd97f844a)
		* [reading-notes](https://github.com/fun1355/reading-notes)
			* list some notes
		* [Danderspritz Docs](https://danderspritz.com/terms)
			* Documentation about the Equation Group's DanderSpritz post-exploitation framework
		* [DanderSpritz_docs](https://github.com/francisck/DanderSpritz_docs)
			* The goal of this project is to examine, reverse, and document the different modules available in the Equation Group's DanderSpritz post-exploitation framework leaked by the ShadowBrokers 
		* [Programming for Wannabes. Part V. A Dropper - pico(2020)](https://0x00sec.org/t/programming-for-wannabes-part-v-a-dropper/23090)
		* [Beyond pty.spawn - use pseudoterminals in your reverse shells (DNScat2 example) - @TheXC3LL(2018)](https://x-c3ll.github.io/posts/forkpty-dnscat2/)
		* [Vault7 Leaks : A look at Longhorn Trojan and Black Lambert spying backdoor - Arnaud Delmas(2017)](https://web.archive.org/web/20170715011527/http://adelmas.com:80/blog/longhorn.php)
		* [Stealthy Targeted Implant Loaders - Attactics](https://attactics.org/2019/06/stealthy-targeted-implant-loaders/)
		* [Stealthy Targeted Implant Loaders Addendum - Attactics](https://attactics.org/2019/07/stealthy-targeted-implant-loaders-addendum/)
	* **Papers**
		* [VXUG Papers](https://github.com/vxunderground/VXUG-Papers)
			* Research code & papers from members of vx-underground.
		* [Multi-Stage Delivery of Malware - Marco Ramilli, Matt Bishop](http://nob.cs.ucdavis.edu/bishop/papers/2010-malware/msmalware.pdf)
			* Malware signature detectors use patterns of bytes, orvariations of patterns of bytes, to detect malware attemptingto enter a systems. This approach assumes the signaturesare both or sufficient length to identify the malware, andto distinguish it from non-malware objects entering the sys-tem. We describe a technique that can increase the difficultyof both to an arbitrary degree. This technique can exploitan optimization that many anti-virus systems use to makeinserting the malware simple; fortunately, this particularexploit is easy to detect, provided the optimization is notpresent. We describe some experiments to test the effective-ness of this technique in evading existing signature-basedmalware detectors.
	* **Talks/Presentations/Videos**
		* [Hacking Malware: Offense Is the New Defense - Valsmith, Quist(2014)](https://www.youtube.com/watch?v=WEgxe85Pvc4&list=PL9fPq3eQfaaAxDI0xo83ZFzDAZgXO3Yhy&index=77)
			* The proliferation of malware is a serious problem, which grows in sophistication and complexity every day, but with this growth, comes a price. The price that malware pays for advanced features and sophistication is increased vulnerability to attack. Malware is a system, just like an OS or application. Systems employ security mechanisms to defend themselves and also suffer from vulnerabilities which can be exploited. Malware is no different. Malware authors are employing constantly evolving techniques including binary obfuscation, anti-debugging and anti-analysis, and built in attacks against protection systems such as anti-virus software and firewalls. This presentation will dig into these techniques and explain the basics. The idea of an open source malware analysis and research community will be explored. All the things the Anti-Virus vendors don't want you to know will be discussed. Methods for bypassing malware's security systems will be presented. These methods include detecting and defeating packers/encoders, hiding the debugger from the malware, and protecting analysis virtual machines. We will hack the malware. 
		* [Writing malware while the blue team is staring at you - Mubix "Rob" Fuller(Derbycon2016)](https://www.irongeek.com/i.php?page=videos/derbycon6/103-writing-malware-while-the-blue-team-is-staring-at-you-mubix-rob-fuller)
		* [Pages from a sword-maker’s notebook - Vyrus(SHELLCON 2017)](https://www.youtube.com/watch?v=2-zos1EAvNY&list=PL7D3STHEa66R0nWbixrTo3O7haiMmA71T&index=4&t=0s)
			* This talk is an encapsulation of implemented solutions for achieving common requirements when constructing software designed to perform long term covert intelligence gathering. It is a “grab bag” of “tips and tricks” developed and or abstracted from previous works by the presenter in a variety of intelligence gathering operations, none of which will be specifically disclosed. Full source code (almost all of it written in Golang) will be provided for tactic snippets, as well as several publicly available practical examples of solutions to various covert intelligence gathering roadblocks.  The technical details of this presentation will be prefaced by a small summery of “which tactics work from a methodical perspective and why” from a human perspective. Beyond this, specific mappings will be drawn from these methods to the specific technical capabilities disclosed in the latter portion of the presentation. The technical subjects in question will include but not be limited to. – anti virus evasion (with special emphasis on modern machine learning based solutions) – anti attribution techniques – covert channel methods – C2 “castle guarding” – covert administration & devops – solution scaling – persistence – future proofing – counter intelligence / anti reverse engineering.
		* [Practical Implants for Windows in PowerShell - Chris Bad2Beef(SHELLCON2017)](https://www.youtube.com/watch?index=8&list=PL7D3STHEa66R0nWbixrTo3O7haiMmA71T&t=0s&v=-HRLMfYfWTM&app=desktop)
			* Chances are there are a few things we all know about PowerShell. It’s great, it’s nearly ubiquitous on Windows, and we can get up to some crazy red team shenaniganry with it. One shouldn’t necessarily be judged if their knowledge of PowerShell ends there. After all, the information security space is far too vast for everyone to know everything. That said, we’re in a dangerous spot. So much thought space seems to be dedicated to matching pre-fabricated tools with pre-defined scenarios akin to the script kiddie methodology of yesteryear. We don’t need to be an expert on everything, but something that has become as core as PowerShell should at least warrant a little bit of study. To that end, we’ll walk through creation, execution, and persistence of a few basic implant prototypes written in PowerShell for Windows. Along the way we’ll look at a few different notes and techniques for coding, packaging, and execution within the contexts of detectability and mitigation. The talk will focus on practical instruction and key gimmies and gotchas. By the end of the discussion, the audience is expected to have a better understanding about how PowerShell tools are written an executed, leading to a greater command over existing tools and techniques. With a bit of additional study, the audience should be able to author tools of their own.
		* [Malproxying: Leave Your Malware at Home - Hila Cohen, Amit Waisel(Defcon27)](https://www.youtube.com/watch?v=GYZx0oJU1nI)
			* During a classic cyber attack, one of the major offensive goals is to execute code remotely on valuable machines. The purpose of that code varies on the spectrum from information extraction to physical damage. As defenders, our goal is to detect and eliminate any malicious code activity, while hackers continuously find ways to bypass the most advanced detection mechanisms. It’s an endless cat-and-mouse game where new mitigations and features are continuously added to the endpoint protection solutions and even the OS itself in order to protect the users against newly discovered attack techniques. In this talk, we present a new approach for malicious code to bypass most of endpoint protection measures. Our approach covertly proxies the malicious code operations over the network, never deploying the actual malicious code on the victim side. We are going to execute code on an endpoint, without really storing the code on disk or loading it to memory. This technique potentially allows attackers to run malicious code on remote victims, in such a way that the code is undetected by the victim’s security solutions. We denote this technique as “malproxying”.
		* [RATs Without Borders - Moving Your Chesse - Robert Neel(BsidesATX2019)](https://www.youtube.com/watch?v=ZubIQfHEUzA)
			* [Slides](https://penconsultants.com/home/wp-content/uploads/2019/03/BSides_ATX_2019.pdf)
			* [Code](https://gitlab.com/J35u5633k/RATsWithoutBorders_public)
		* [Offensive Tradecraft: Defence Evasion - Paul Laîné(Securi-Tay 2020)](https://www.youtube.com/watch?v=CUqKAaHQa14)
			* Over the last years, the cyber security posture of companies is improving, and, despite the general opinion, anti-viruses and endpoint protections are more and more sophisticated against “day-to-day threats”. Additionally, defenders are better trained and more aware of the techniques, tactics and procedures (TTPs) used by the bad guys, which subsequently make them readier to detect and respond to incoming threats. The two objectives of this presentation are (i) to define the numerous challenges faced while building and deploying malwares nowadays, and (ii) to provide a non-exhaustive list of techniques and tactics that can be implement in order to bypass defence mechanisms.
		* [Malware techniques from aggressor's perspective - Pawel Kordos, Patryk Czeczko(x33fcon2020)](https://www.youtube.com/watch?v=nTWJ0KtoGwI&list=PL7ZDZo2Xu330gMHAoeGvH9QkCJMC-qgeK&index=14)
			* We will demonstrate common techniques used by malicious software and leveraged by our team during adversary simulations, including: AV&sandbox evasion, code injection, persistence, C2 channels, polymorphic malware, environmental keying, obfuscation by API hashing and more… Sounds familiar? :) We will discuss techniques mentioned above. Code samples and working examples will be presented, including reverse engineer / malware analyst perspective. No boring slides, just working examples.
		* [C++ for Hackers - Josh Lospinoso(2020)](https://vimeo.com/384348826)
			* Shift5 co-founder, Josh Lospinoso, talks about how C++ can be a vital tool for infosec developers. In this talk, he presents a simple Stage 0 Implant written in modern C++ to tool developers from Army Cyber Command. Along the way, he illuminates many features of C++, the C++ Standard Library, and the Boost Libraries that are highly useful when developing cybersecurity tools.
			* [Code](https://github.com/jlospinoso/cpp-implant)
	* **Simple Samples**
		* [TCP Bind Shell Shellcode - Metasploit Framework](https://github.com/rapid7/metasploit-framework/blob/master/external/source/shellcode/windows/x86/src/block/block_bind_tcp.asm)
* **Anti-Tricks**<a name="anti-tricks"></a>
	* **Collection Projects**
		* [Unprotect Project](https://search.unprotect.it/map/)
			* Malware authors spend a great deal of time and effort to develop complex code to perform malicious actions against a target system. It is crucial for malware to remain undetected and avoid sandbox analysis, antiviruses or malware analysts. With this kind of technics, malware are able to pass under the radar and stay undetected on a system. The goal of this free database is to centralize the information about malware evasion techniques. This project aims to provide Malware Analysts and Defenders with actionable insights and detection capabilities to shorten their response times.
		* [al-khaser](https://github.com/LordNoteworthy/al-khaser)
			* Public malware techniques used in the wild: Virtual Machine, Emulation, Debuggers, Sandbox detection.
		* [Evasion techniques - CheckPoint Research](https://evasions.checkpoint.com/)
			* [Evasions Github](https://github.com/CheckPointSW/Evasions)
			* "In this encyclopedia we have attempted to gather all the known ways to detect virtualized environment grouping them into big categories. Some categories are inactive on main page: it means that content will be added later. If it isn’t stated explicitly which operating system is described, Windows is meant by default."
	* **Anti-Debug**<a name="anti-dbg"></a>
		* **Articles/Blogposts/Writeups**
			* [Windows Anti-Debug Reference - Nicholas Falliere(2007)](https://community.broadcom.com/symantecenterprise/communities/community-home/librarydocuments/viewdocument?DocumentKey=230d68b2-c80f-4436-9c09-ff84d049da33&CommunityKey=1ecf5f55-9545-44d6-b0f4-4e4a7f5f5e68&tab=librarydocuments)
			* [Tricks used by malware authors to protect their malicious code from detection - Avi Lamay(2018)](https://deceptivebytes.com/2018/07/09/tricks-used-by-malware-authors-to-protect-their-malicious-code-from-detection/)
			* [Anti Debugging Protection Techniques with Examples - Oleg Kulchytskyy, Anton Kukoba(2021)](https://www.apriorit.com/dev-blog/367-anti-reverse-engineering-protection-techniques-to-use-before-releasing-software)
		* **Papers**
			* [The "Ultimate" Anti-Debugging Reference - Peter Ferrie(2011)](http://pferrie.epizy.com/papers/antidebug.pdf?i=1)
				* [Archive Link](https://web.archive.org/web/20191114080821/http://pferrie.host22.com/papers/antidebug.pdf)
			* [Antiforensic techniques deployed by custom developed malware in evading anti-virus detection - Ivica Stipovic(2019)](https://arxiv.org/abs/1906.10625)
		* **Presentations/Talks/Videos**
			* [Introduction to Sandbox Evasion and AMSI Bypasses - BC-Security(2019)](https://github.com/BC-SECURITY/DEFCON27)
		* **Tools**
			* [Anti-Debug Tricks](https://github.com/CheckPointSW/Anti-Debug-DB)
				* [Anti-Debug Tricks](https://anti-debug.checkpoint.com/)
				* Anti-Debug encyclopedia contains methods used by malware to verify if they are executed under debugging. It includes the description of various anti-debug tricks, their implementation, and recommendations of how to mitigate the each trick.
			* [CheckPlease](https://github.com/Arvanaghi/CheckPlease)
			* [aegis](https://github.com/rafael-santiago/aegis)
				* Aegis is a library that allows you detect if your software is being debugged or not on Linux, FreeBSD, NetBSD, OpenBSD and Windows. You can use it natively from C or use the Go bind.
			* [Fake Sandbox Artifacts (FSA)](https://github.com/NavyTitanium/Fake-Sandbox-Artifacts)
				* This script allows you to create various artifacts on a bare-metal Windows computer in an attempt to trick malwares that looks for VM or analysis tools
			* [simpliFiRE.AntiRE - An Executable Collection of Anti-Reversing Techniques](https://bitbucket.org/fkie_cd_dare/simplifire.antire/src/master/)
				* AntiRE is a collection of such anti analysis approaches, gathered from various sources like Peter Ferrie's The "Ultimate" Anti-Debugging Reference and Ange Albertini's corkami. While these techniques by themselves are nothing new, we believe that the integration of these tests in a single, executable file provides a comprehensive overview on these, suitable for directly studying their behaviour in a harmless context without additional efforts. AntiRE includes different techniques to detect or circumvent debuggers, fool execution tracing, and disable memory dumping. Furthermore, it can detect the presence of different virtualization environments and gives examples of techniques used to twarth static analysis.
			* [Corkami](https://github.com/corkami)
			* [Anti-DBG](https://github.com/HackOvert/AntiDBG)
				* AntiDBG is a collection of Windows Anti Debugging techniques. The techniques are categorized by the methods they use to find a debugger.
			* [Unprotect_Submission](https://github.com/fr0gger/Unprotect_Submission)
			* [Anti-Debugging](https://github.com/ThomasThelen/Anti-Debugging)
				* A collection of c++ programs that demonstrate common ways to detect the presence of an attached debugger.
			* [antidebug](https://github.com/waleedassar/antidebug)
				* Collection Of Anti-Debugging Tricks
	* **Anti-RE**<a name="anti-re"></a>
		* **Articles/Blogposts/Writeups**
			* [RDTSCP – a recooked AntiRe trick - Hexacorn(2014)](https://www.hexacorn.com/blog/2014/06/15/rdtscp-a-recooked-antire-trick/)
			* [Simple Anti-RE Trick - `@_qaz_qaz`(2019)](https://secrary.com/Random/anti_re_simple/)
		* **Presentations/Talks/Videos**
			* [Computer Security 資安實務: Windows Reversing [Dark Art] -  Sheng-Hao Ma(2018)](https://speakerdeck.com/aaaddress1/computer-security-zi-an-shi-wu-windows-reversing-dark-art)
		* **Papers**
			* ["Smart" trash: building of logic - pr0mix(2011)](https://vxug.fakedoma.in/archive/VxHeaven/lib/vpo01.html)
				* "The main goal of garbage instructions - a hiding/protection of useful code (from av'ers, a watchful eye reverser and other curious). However, the "wrong" trash can lead to detection of viral code, thereby undermining all our efforts.  This text is about how to improve the quality of the generated garbage."
		* **Tools**
			* [ANTI](https://github.com/nihilboy/anti)
				* Automated Integration of anti-Reversing methods in PE executables
	* **Anti-Sandbox**<a name="antisandbox"></a>
		* **Sandbox Detection**<a name="anti-sandbox"></a>
			* **Articles/Blogposts/Writeups**
				* [Sandbox evasion: Identifying Blue Teams - Víctor Calvo(2020)](https://www.securityartwork.es/2020/10/12/sandbox-evasion-identifying-blue-teams/)
				* [Detecting VMware on 64-bit systems - Matteo Malvica(2021)](https://www.matteomalvica.com/blog/2018/12/05/detecting-vmware-on-64-bit-systems/)
				* [Playing with GuLoader Anti-VM techniques - Carlos Rubio, Blueliv labs(2020)](https://www.blueliv.com/cyber-security-and-cyber-threat-intelligence-blog-blueliv/research/playing-with-guloader-anti-vm-techniques-malware/)
			* [Evasion techniques - CheckPoint Research](https://evasions.checkpoint.com/)
				* [Evasions Github](https://github.com/CheckPointSW/Evasions)
				* "In this encyclopedia we have attempted to gather all the known ways to detect virtualized environment grouping them into big categories. Some categories are inactive on main page: it means that content will be added later. If it isn’t stated explicitly which operating system is described, Windows is meant by default."
			* **Papers**
				* [Hot Knives Through Butter: Evading File-based Sandboxes - Abhishek Singh, Zheng Bu(2014)](https://www.fireeye.com/content/dam/fireeye-www/current-threats/pdfs/pf/file/fireeye-hot-knives-through-butter.pdf)
					* This report details the following categories of sandbox-evasion techniques: Human interaction—mouse clicks and dialog boxes; Configuration-specific—sleep calls, time triggers, process hiding, malicious downloaders, execution name of the analyzed files, volume information, and execution after reboot; Environment-specific—version, embedded iframes (in flash, swf, jpg files), embedded executable in an image file, and DLL loaders; VMware-specific—system-service lists, unique files, and the VMX Port
				* [Sleeping Your Way out of theSandbox - Hassan  Mourad(2015)](https://www.sans.org/reading-room/whitepapers/malicious/sleeping-sandbox-35797)
					* In recent years,the security landscape has witnessed the rise of a new breed of malware, Advanced Persistence Threat, or APT for short. With all traditional security solutions failing to address this new threat, a demand was created for new solutions that are capable of addressing the advanced capabilities of APT. One of the offeredsolutions was file-based sandboxes,asolution that dynamically analyzes files and judgestheir threat levelsbased on their behavior in an emulated/virtual environment. But security is a cat and mouse game, and malware authors are always trying to detect/bypass such measures. Some of the common techniques used by malware for sandbox evasionwill be discussed in this paper. This paperwill also analyze how to turn somecountermeasuresused by sandboxes against it. Finally, it will introduce some new ideas for sandbox evasion along with recommendationsto address them.
				* [Spotless Sandboxes: Evading Malware AnalysisSystems using Wear-and-Tear Artifacts - Najmeh Miramirkhani, Mahathi Priya Appini, Nick Nikiforakis, Michalis Polychronakis(2017)](https://www3.cs.stonybrook.edu/~mikepo/papers/wearntear.sp17.pdf)
					* We observe that as the fidelity and transparency of dynamicmalware analysis systems improves, malware authors can resortto other system characteristics that are indicative of artificialenvironments. We present a novel class of sandbox evasiontechniques that exploit the “wear and tear” that inevitably occurson real systems as a result of normal use. By moving beyond howrealistic a system looks like, to how realisticits past uselooks like,malware can effectively evade even sandboxes that do not exposeany instrumentation indicators, including bare-metal systems. Weinvestigate the feasibility of this evasion strategy by conductinga large-scale study of wear-and-tear artifacts collected from realuser devices and publicly available malware analysis services. Theresults of our evaluation are alarming: using simple decision treesderived from the analyzed data, malware can determine that asystem is an artificial environment and not a real user devicewith an accuracy of 92.86%. As a step towards defending againstwear-and-tear malware evasion, we develop statistical models thatcapture a system’s age and degree of use, which can be used toaid sandbox operators in creating system images that exhibit arealistic wear-and-tear state.
				* [Stealthy and in-depth behavioral malware analysis with Zandbak - Tim van Dijk(2019)](https://www.ru.nl/publish/pages/769526/z6_timvandijk_masterthesis.pdf)
					* "In this thesis, we present Zandbak: a malware analysis sandbox with in-depth analytical capabilities that defends against evasive techniques. Zandbak resides purely in kernel space, making it nearly undetectable to user space malware which does not have the necessary privileges to detect the presence of Zandbak. Furthermore, Zandbak has novel approaches and techniques to performing real-time stack walking, snapshotting and infection scope tracking. We describe the implementation of Zandbak in detail. We perform a series of experiments and a case study where we analyze an implant of the PlugX malware. With this, we demonstrate that Zandbak indeed bypasses anti-analysis techniques used in the wild and has the ability to perform in-depth analysis."
			* **Presentations/Talks/Videos**
				* [Countering Innovative Sandbox Evasion Techniques Used by Malware - Frederic Besler, Carsten Willems, and Ralf Hund(FIRST2017)]()
					* [Slides](https://www.first.org/resources/papers/conf2017/Countering-Innovative-Sandbox-Evasion-Techniques-Used-by-Malware.pdf)
				* [Operating System Fingerprinting for Virtual Machines - Nguyen Anh Quynh(Defcon18)](https://www.youtube.com/watch?v=wQvyu8oR14c)
					* [Slides](https://www.defcon.org/images/defcon-18/dc-18-presentations/Quynh/DEFCON-18-Quynh-OS-Fingerprinting-VM.pdf)
					* This paper analyzes the drawbacks of current OSF approaches against VM in the cloud, then introduces a novel method, named UFO, to fingerprint OS running inside VM. Our solution fixes all the above problems: Firstly, it can recognize all the available OS variants and (in lots of cases) exact OS versions with excellent accuracy, regardless of OS tweaking. Secondly, UFO is extremely fast. Last but not least, it is hypervisor-independent: we proved that by implementing UFO for Xen and Hyper-V.
				* [Sandbox fingerprinting: Evadiendo entornos de análisis - Roberto Amado & Victor Calvo(RootedCon2020)](https://www.youtube.com/watch?v=AyVgIttiUpQ)
					* This talk will therefore present the results of the study of the operation of different online automatic file analysis services in order to avoid them. In addition, this study is completed with different factors that try to identify which service is performing the analysis in order to better understand the tools of the defenders. In a complementary way, the possibility of identifying / attacking the analysts in charge of studying the threats will be exposed through vulnerabilities identified in the management panels of some sandboxes such as Virustotal and which were reported to the Google team. This last technique allows identifying which analyst or entity is analyzing the malicious sample. The audience will be able, from a Blue team point of view, to identify which aspects of their sandbox solutions should improve to avoid their evasion and, on the other hand, from a Red Team point of view, which control elements should be applied to their attack tools to avoid the greater part of these security solutions.
			* **Tools**
				* [wsb-detect](https://github.com/LloydLabs/wsb-detect)
					* "wsb-detect enables you to detect if you are running in Windows Sandbox ("WSB"). The sandbox is used by Windows Defender for dynamic analysis, and commonly manually by security analysts and alike. At the tail end of 2019, Microsoft introduced a new feature named Windows Sandbox (WSB for short). The techniques used to fingerprint WSB are outlined below, in the techniques section."
				* [Pufferfish](https://github.com/dsnezhkov/pufferfish)
					* The goal of this project is to create a way to utilize (userland) Sandbox checks into offensive workflow in a flexible, robust and opsec safe manner. Mainly, to address the decision making process of payload detonation in destination environment.
				* [Fake Sandbox Artifacts (FSA)](https://github.com/NavyTitanium/Fake-Sandbox-Artifacts)
					* This script allows you to create various artifacts on a bare-metal Windows computer in an attempt to trick malwares that looks for VM or analysis tools
				* [anti-analysis-tricks](https://github.com/ricardojrdez/anti-analysis-tricks)
					* Bunch of techniques potentially used by malware to detect analysis environments
				* [No_Sandboxes](https://github.com/Th4nat0s/No_Sandboxes)
					* Test suite for bypassing Malware sandboxes.
				* [anticuckoo](https://github.com/David-Reguera-Garcia-Dreg/anticuckoo)
				* [al-khaser](https://github.com/LordNoteworthy/al-khaser)
					* Public malware techniques used in the wild: Virtual Machine, Emulation, Debuggers, Sandbox detection.
				* [InviZzzible](https://github.com/CheckPointSW/InviZzzible)
					* "InviZzzible is a tool for assessment of your virtual environments in an easy and reliable way. It contains the most recent and up to date detection and evasion techniques as well as fixes for them."
	* **Anti-VM**<a name="anti-vm"></a>
		* **101**
			* [Evasions](https://github.com/CheckPointSW/Evasions)
				* "Evasions encyclopedia gathers methods used by malware to evade detection when run in virtualized environment. Methods are grouped into categories for ease of searching and understanding. Also provided are code samples, signature recommendations and countermeasures within each category for the described techniques."
		* **Articles/Blogposts/Writeups**
		* **Presentations/Talks/Videos**
		* **Tools**
		* **Tools**
			* [Pafish](https://github.com/a0rtega/pafish)
				* Pafish is a testing tool that uses different techniques to detect virtual machines and malware analysis environments in the same way that malware families do 
			* [Detect-VM-and-Hypervisor](https://github.com/LazyAhora/Detect-VM-and-Hypervisor)
				* Detect VM and Hypervisor
			* [Virtual Machines Detection Enhanced](https://github.com/hfiref0x/VMDE)
				* "Source from VMDE paper, adapted to 2015" + Pdf of paper
	* **Bring-Your-Own-`*`**<a name="byof"></a>
		* **Land(Compiler/Interpreter)**
			* **Articles/Blogposts/Writeups**
				* [Bring Your Own Land (BYOL) – A Novel Red Teaming Technique - Nathan Kirk](https://www.fireeye.com/blog/threat-research/2018/06/bring-your-own-land-novel-red-teaming-technique.html)
				* [Red Teamer’s Cookbook: BYOI (Bring Your Own Interpreter) - Marcello Salvati(2020)](https://www.blackhillsinfosec.com/red-teamers-cookbook-byoi-bring-your-own-interpreter/)
				* [Red Team: How to embed Golang tools in C# - Shantanu Khandelwal(2020)](https://medium.com/@shantanukhande/red-team-how-to-embed-golang-tools-in-c-e269bf33876a)
				* [Malware Dropping a Local Node.js Instance - Xme(2019)](https://isc.sans.edu/forums/diary/Malware+Dropping+a+Local+Nodejs+Instance/25284/)
			* **Talks/Presentations/Videos**
				* [Quick Retooling in Net for Red Teams - Dimitry Snezhkov(CircleCityCon5.0)](https://www.youtube.com/watch?v=C04TD4dVLSk)
				* [Waiter theres a compiler in my shellcode - Josh Stone(NolaCon2019)](https://www.youtube.com/watch?v=55234oZ0EDU)
					* Join me in this talk about a programming language and environment built specifically with subversive remote control in mind. It's a native code, optimizing compiler that fits in about 5KB of shellcode, requires no runtime environment, can be deployed any way you like, and yet gives you all the access you need on the target host. And to top it all off, it's built around an interactive coding paradigm that makes dynamic exploratory post-exploitation fun. This talk approaches some complex topics, but is designed to be interesting to anyone, whether you're into compiler theory or not. Even a non-coder should get something out of it, so anyone with an interest in offensive hacking is encouraged to attend.
				* [Red Team Level over 9000! Fusing the powah of .NET with a scripting language of your choosing: introducing BYOI (Bring Your own Interpreter) payloads. -  Marcello Salvati(Derbycon2019)](https://www.irongeek.com/i.php?page=videos/derbycon9/1-17-red-team-level-over-9000-fusing-the-powah-of-net-with-a-scripting-language-of-your-choosing-introducing-byoi-bring-your-own-interpreter-payloads-marcello-salvati)
					* [Slides](https://github.com/byt3bl33d3r/Slides/blob/master/RT%20Level%209000%2B%2B_BsidesPR.pdf)
					* With all of the defenses Microsoft has implemented in the PowerShell run-time over the past few years Red Teamers & APT groups have started too shy away from using PowerShell based payloads/delivery mechanisms and migrate over to C#. However, C# is a compiled language, operationally this has a few major downsides: we can?t be as ?flexible? as we could be with scripting languages, setting up a proper development environment has overhead, things need to be compiled etc... in this talk, I will be covering my approach to solving these operational problems by using some of the (possibly?) lesser known features of the .NET framework and introducing BYOI (Bring Your Own Interpreter) payloads which allow you to embed a scripting language of your choosing into any .NET language!
			* **Tools**
				* [typhoon](https://github.com/dsnezhkov/typhoon)
				* [GolanginCsharp](https://github.com/shantanu561993/GolanginCsharp)
					* Project to use Golang inside C# 
				* [EvilVM](https://github.com/jephthai/EvilVM)
					* EvilVM compiler for information security research tools. The project is built around a native code Forth compiler that is deployed as a position independent shellcode. It provides a platform for remote code execution, useful in information security contexts.
					* [Talk](https://www.youtube.com/embed/55234oZ0EDU)
				* [WheresMyImplant](https://github.com/0xbadjuju/WheresMyImplant)
					* A Bring Your Own Land Toolkit that Doubles as a WMI Provider 
	* **Crypters**<a name="crypter"></a>
		* **Articles/Blogposts/Writeups**
			* [100% evasion - Write a crypter in any language to bypass AV - Xentropy(2020)](https://netsec.expert/2020/02/06/write-a-crypter-in-any-language.html)
			* [Windows PE run-time encryption with Hyperion - Andrea Fortuna(2018)](https://www.andreafortuna.org/2018/01/26/windows-pe-run-time-encryption-with-hyperion/)
			* [100% evasion - Write a crypter in any language to bypass AV - xentropy(2020)](https://netsec.expert/2020/02/06/write-a-crypter-in-any-language.html)
		* **Papers**
			* [Hyperion: Implementation of a PE-Crypter - Christian Ammann(2012)](https://raw.githubusercontent.com/nullsecuritynet/papers/master/nullsec-pe-crypter/nullsec-pe-crypter.pdf)
				* "This paper reveals the theoretic aspects behind run-time crypters and describes a reference implementation for Portable Executables (PE) which is the windows file format for dynamic-link libraries (DLLs), object files and regular executables."
		* **Samples**
			* [Xencrypt](https://github.com/the-xentropy/xencrypt)
				* A PowerShell script anti-virus evasion tool
			* [hyperion](https://github.com/nullsecuritynet/tools/tree/master/binary/hyperion)
				* Hyperion is a runtime encrypter for 32/64 bit portable executables. It is a reference implementation and bases on the paper "Hyperion: Implementation of a PE-Crypter".
		* **Examples**
			* [aes_dust](https://github.com/odzhan/aes_dust)
				* Unlicensed tiny / small portable implementation of 128/256-bit AES encryption in C, x86, AMD64, ARM32 and ARM64 assembly
	* **Cryptography**<a name="crypto"></a>
		* **Tools**
			* [aes_dust](https://github.com/odzhan/aes_dust)
				* Unlicensed tiny / small portable implementation of 128/256-bit AES encryption in C, x86, AMD64, ARM32 and ARM64 assembly
			* [Secure Compatible Encryption Examples](https://github.com/luke-park/SecureCompatibleEncryptionExamples)
				* A collection of secure encryption examples for encrypting strings and binary data. 
			* [Themis](https://github.com/cossacklabs/themis)
				* Easy to use cryptographic framework for data protection: secure messaging with forward secrecy and secure data storage. Has unified APIs across 14 platforms.
	- **Obfuscation Techniques**<a name="obfuscation"></a>
		- **101**
		- **Articles/Blogposts/Writeups**
			* [A Look At Some Real-World Obfuscation Techniques - Nicolas Guigo(2021)](https://research.nccgroup.com/2021/10/12/a-look-at-some-real-world-obfuscation-techniques/)
		- **Talks/Presentations/Videos**
			* [Binary Obfuscation from the Top-Down: Obfuscating Executables Without Writing Assembly - Sean "Frank^2(Defcon17)](https://www.youtube.com/watch?v=iva16Bg5imQ)
				* [Slides](https://www.defcon.org/images/defcon-17/dc-17-presentations/defcon-17-sean_taylor-binary_obfuscation.pdf)
				* Binary obfuscation is commonly applied in malware and by software vendors in order to frustrate the efforts of reverse engineers to understand the underlying code. A common misconception is one must be a master of assembly in order to properly obfuscate a binary. However, with knowledge of compiler optimizations and certain keywords, one can frustratingly obfuscate their binary simply by writing specifically crafted high-level code. This talk will attempt to teach an array of methods that can be employed to obfuscate a binary as it is compiled rather than afterward. Knowledge of C/C++ is the only prerequisite for this talk.
			* [Data Obfuscation: How to hide data and payloads to make them "not exist" (in a mathematically optimal way) - Parker Schmitt(Derbycon2016)](https://www.irongeek.com/i.php?page=videos/derbycon6/400-data-obfuscation-how-to-hide-data-and-payloads-to-make-them-not-exist-in-a-mathematically-optimal-way-parker-schmitt)
				* Many times the answer to any question about cryptography is: "never roll your own crypto". While the logic behind this is understandable it has become a bit of a lost art. Despite the fact that for the most part standard crypto used in normal situations works; when trying to hide the existence of encrypted data alltogether it is far from an optimal solution. Most modern crypto is designed with the fact that the evesdropper knows that an encrypted message exists. However these days with ssl proxys, reversing antivirus, and "anti-crypto" law proposals the assumption that having an evesdropper knowing the existence of said crypto is no longer an easy concession. Despite the fact of many "next-gen" antiviruses failing to detect many obfuscation methods using algorithms such as AES for encrypting a payload is the WRONG way. The reason they are not detected is such an antivirus is just not looking for traces of such an algorithm. From a forensics standpoint, if you're using AES the private key is on the victim's machine for example. In addition, the permutations or S-Boxes are well known permutations and easy to spot in your algorithm. This talk will be on how to design algorithms to make the existence of the cryptography unknown. We will keep some of it high level but also show how to properly implement your own cryptography and/or steganography in such a way that the evesdropper doesn't know it exists. We will talk about side channels and how to keep out of band and/or homemade crypto "cryptographically strong" but also how to generate it on the fly so that no only can you encrypt data in side channels, you can generate a new algorithm on the fly. We want to make it so the randomness of the algorithm itself is "cryptographically strong" Even though many next-gen antivirus fails at such detection as it inproves we need to study obfuscation as much as the mathematics and/or science of standard cryptography.
			* [An Effective Approach to Software Obfuscation - Yu-Jye Tung(BSidesSF2020)](https://www.youtube.com/watch?v=ExiXtdjNGlg&feature=share)
				* Understanding the essential aspects that make up obfuscation allows us to see the fundamental flaw with modern obfuscation implementations and the right way to approach it. We use examples of modern obfuscation techniques to illustrate our points and demonstrate an example of the correct approach.		
		- **Papers**
			* [Obfuscation for object-oriented programs: dismantling instance methods - Heh-Tyan Liaw, Shih-Chieh Wei(2013)](https://onlinelibrary.wiley.com/doi/10.1002/spe.2193)
				* Code obfuscation can help software developers protect technological secrets. Code readability is greatly enhanced with object-oriented technology that represents dynamic binding using instance method invocation. Therefore, dismantling instance methods is proposed in this paper as a critical obfuscating technique for object-oriented programs. The interception classes are interpolated first into the project. The static images and the up forwarders are then created. For each virtual function system and each interface function system, a respective dispatching function is set up. By properly arranging the class identifiers and binding identifiers, the switch statement in the dispatching function can be compiled into constant-time low-level code. After using dispatching functions to simulate virtual function system or interface function system invocations, all original instance methods in the project will be removed. Interception functions and export functions are indispensable in supporting the operation of callback methods. A prototype of our obfuscation system was implemented and successfully tested on some practical scale applications. 
			* [Layered obfuscation: a taxonomy of software obfuscation techniques for layered security - Hui Xu, Yangfan Zhou, Jiang Ming, Michael Lyu(2020)](https://cybersecurity.springeropen.com/articles/10.1186/s42400-020-00049-3)
				* In the paper, we conduct a systematic review of existing obfuscation techniques based on the idea of layered obfuscation and develop a novel taxonomy of obfuscation techniques. Following our taxonomy hierarchy, the obfuscation strategies under different branches are orthogonal to each other. In this way, it can assist developers in choosing obfuscation techniques and designing layered obfuscation solutions based on their specific requirements.
			* [malWASH: Washing Malware to Evade Dynamic Analysis - Kyriakos K. Ispoglou, Mathias Payer](https://www.usenix.org/conference/woot16/workshop-program/presentation/ispoglou)
				* We present malWASH, a dynamic diversification engine that executes an arbitrary program without being detected by dynamic analysis tools. Target programs are chopped into small components that are then executed in the context of other processes, hiding the behavior of the original program in a stream of benign behavior of a large number of processes. A scheduler connects these components and transfers state between the different processes. The execution of the benign processes is not impacted. Furthermore, malWASH ensures that the executing program remains persistent, complicating the removal process.		
		- **Tools**
			* [Tigress_protection](https://github.com/JonathanSalwan/Tigress_protection)
				* "Playing with the Tigress binary protection. Break some of its protections and solve some of its challenges. Automatic deobfuscation using symbolic execution, taint analysis and LLVM."
			* [malWASH v2.0](https://github.com/HexHive/malWASH)
				* "malWASH is a dynamic diversification engine that executes an arbitrary program without being detected by dynamic analysis tools. In other words, it is a malware engine, that can make existing malware, to evade all existing behavioral and dynamic analysis detection methods.  Note that malWASH is research project (i.e. not stable). The goal of this project is to demonstrate that this new generation of malware is possible. It needs a lot of additional work to become a tool that can be used in the wild."
		- **Compiler-based**<a name="obfus-compiler"></a>
			- **LLVM**
				* **101**
					* [Tickling VMProtect with LLVM: Part 1 - fvrmatteo(2021)](https://secret.club/2021/09/08/vmprotect-llvm-lifting-1.html)
						* [Part 2](https://secret.club/2021/09/08/vmprotect-llvm-lifting-2.html)
						* [Part 3](https://secret.club/2021/09/08/vmprotect-llvm-lifting-3.html)
				* **Articles/Blogposts/Writeups**
					* [Build your first LLVM Obfuscator - polarply(2020)](https://medium.com/@polarply/build-your-first-llvm-obfuscator-80d16583392b)
						* In this post we will briefly present LLVM, discuss popular obfuscation approaches and their shortcomings and build our own epic LLVM-based string obfuscator.
						* [Code](https://github.com/tsarpaul/llvm-string-obfuscator)
				* **Tools**
					* [Grimheart](https://github.com/Naville/Grimheart)
						* Torture your LLVM Obfuscation
					* [CodeObfs](https://github.com/bigBestWay/CodeObfs)
						* LLVM based "VM" obfuscator
					* [SheLLVM](https://github.com/SheLLVM/SheLLVM)
						* A collection of LLVM transform and analysis passes to write shellcode in regular C
					* [Obfuscator-LLVM](https://github.com/obfuscator-llvm/obfuscator/wiki)
						* The aim of this project is to provide an open-source fork of the LLVM compilation suite able to provide increased software security through code obfuscation and tamper-proofing. 
					* [llvm2019](https://github.com/mangh/llvm2019)
					* [llvm-mingw](https://github.com/mstorsjo/llvm-mingw)
						* An LLVM/Clang/LLD based mingw-w64 toolchain; This is a recipe for reproducibly building a LLVM/Clang/LLD based mingw-w64 toolchain.
					* [vs-obfuscation](https://github.com/Tai7sy/vs-obfuscation)
					* [HikariCore](https://github.com/HikariRebooted/HikariCore)
						* Fork of the core LLVM Obfuscation Library of Hikari.
					* [Obfuscator](https://github.com/klezVirus/obfuscator/tree/llvm-9.0.1)
						* ollvm, based on llvm-clang 5.0.2, 6.0.1, 7.0.1, 8.0, 9.0, 9.0.1
		- **MarkovChains**
			* **Tools**
				* [MarkovObfuscate](https://github.com/CylanceSPEAR/MarkovObfuscate)
					* Use Markov Chains to obfuscate data as other data
		- **Shellcode-based**
			- **Tools**
				* [Obfuscator](https://github.com/3xpl01tc0d3r/Obfuscator)
					* The program is designed to obfuscate the shellcode.
				* [xObf](https://github.com/d35ha/xObf)
					* Simple x86/x86_64 instruction level obfuscator based on a basic SBI engine	
				* [Obfuscator](https://github.com/3xpl01tc0d3r/Obfuscator)
					* The program is designed to obfuscate the shellcode. Currently the tool supports 2 encryption.
				* [TinyObfuscate - A small String Obfuscator - Michael Haephrati(2017)](https://www.codeproject.com/Articles/1210398/TinyObfuscate-A-small-String-Obfuscator)					
		- **Steganography**<a name="obfus-stego"></a>
			* **101**
				* [Steganograhpy - Wikipedia](https://en.wikipedia.org/wiki/Steganography)
			* **Articles/Blogposts/Writeups**
			* **Tools**
				* [Don't Kill My Cat (DKMC)](https://github.com/Mr-Un1k0d3r/DKMC)
					* Don't kill my cat is a tool that generates obfuscated shellcode that is stored inside of polyglot images. The image is 100% valid and also 100% valid shellcode. The idea is to avoid sandbox analysis since it's a simple "legit" image. For now the tool rely on PowerShell the execute the final shellcode payload.
				* [GG-AESY](https://github.com/jfmaes/GG-AESY)
					* [Article](https://redteamer.tips/introducing-gg-aesy-a-stegocryptor/)
					* Hide cool stuff in images :)
		- **VirtualMachine-based**<a name="obfus-vm"></a>
			- **LLVM**
				* **101**
				* **Articles/Blogposts/Writeups**
				* **Tools**
					* [x86 Code Virtualizer](https://github.com/NIKJOO/x86-Code-Virtualizer)
						* Open-source and lite application to obfuscate binary codes and makes challenge for reverse engineers to understand code.
					* [NoVmp](https://github.com/can1357/NoVmp)
						* NoVmp is a project devirtualizing VMProtect x64 3.0 - 3.5 (latest) into optimized VTIL and optionally recompiling back to x64 using the Virtual-machine Translation Intermediate Language library. It is rather experimental and is mostly a PoC I wanted to release. Most things can be improved especially with the new NativeLifters repo, but it did not exist back in the time this was written.
					* [StackVMSharp](https://github.com/japajoe/StackVMCPP)
						* A stack and register based virtual machine which can compile and run arbitrary code in runtime.
	- **Meta/Poly/Oligo-Morphism**<a name="metapoly"></a>
		* **101**
			* [Metamorphism and permutation: feel the difference - Z0mbie](https://vxug.fakedoma.in/archive/VxHeaven/lib/vzo24.html)
			* [Oligomorphism vs polymorphism vs metamorphism in malware - StackExchange(2011)](https://security.stackexchange.com/questions/4619/oligomorphism-vs-polymorphism-vs-metamorphism-in-malware)
		* **Articles/Blogposts/Writeups**
			* [Metamorphism in practice or "How I made MetaPHOR and what I've learnt" - The Mental Driller(2002)](https://vxug.fakedoma.in/archive/VxHeaven/lib/vmd01.html)
			* [Whitecomet-Research](https://github.com/PoCInnovation/Whitecomet-Research)
				* Research on malware creation and protection
			* [BMP / x86 Polyglot - Spencer(2016)](https://warroom.rsmus.com/bmp-x86-polyglot/)
		* **Talks/Presentations/Videos**
			* [Antivirus Evasion through Antigenic Variation (Why the Blacklisting Approach to AV is Broken) - Trenton Ivey, Neal Bridges(Derbycon 2013)](https://www.irongeek.com/i.php?page=videos/derbycon3/4108-antivirus-evasion-through-antigenic-variation-why-the-blacklisting-approach-to-av-is-broken-trenton-iveyneal-bridges)
				* Think of the last time you got sick. Your immune system is an amazing piece of machinery, but every now and then, something gets past it. Antivirus evasion techniques can become more effective when modeled after infectious diseases. This talk highlights many of the antivirus evasion techniques in use today. Going further, this talk shows how genetic algorithms can quickly and repeatedly “evolve” code to evade many malicious code detection techniques in use today.
			* **Papers**
			* **Tools**
				* [Enneos](https://github.com/hoodoer/ENNEoS)
					* Evolutionary Neural Network Encoder of Shenanigans. Obfuscating shellcode with an encoder that uses genetic algorithms to evolve neural networks to contain and output the shellcode on demand.
				* [MorphAES](https://github.com/cryptolok/MorphAES)
					* MorphAES is the world's first polymorphic shellcode engine, with metamorphic properties and capability to bypass sandboxes, which makes it undetectable for an IDPS, it's cross-platform as well and library-independent.
				* [Fetch-n-Exec](https://github.com/x0reaxeax/Fetch-n-Exec)
					* The idea behind this one is to fetch opcodes and data from a remote server to rewrite the binary with during runtime. Except this time, we go x64 and -nostdlib, so everything will be done using syscalls and a few helper buddies from x0lib.	
	- **Packers**<a name="packers"></a>
		- **101**
			* [Awesome Executable Packing](https://github.com/dhondta/awesome-executable-packing)
			* [PaaS, or how hackers evade antivirus software - (2021)](https://www.ptsecurity.com/ww-en/analytics/pt-esc-threat-intelligence/paas-or-how-hackers-evade-antivirus-software/)
			* [Writing a PE packer – Intro - BidouilleSecurity(2021)](https://bidouillesecurity.com/tutorial-writing-a-pe-packer-intro/)
				* [Code](https://github.com/jeremybeaume/packer-tutorial)
				* [Part 1](https://bidouillesecurity.com/tutorial-writing-a-pe-packer-part-1/)
				* [Part 2](https://bidouillesecurity.com/tutorial-writing-a-pe-packer-part-2/)
				* [Part 3](https://bidouillesecurity.com/tutorial-writing-a-pe-packer-part-3/)
				* [Part 4](https://bidouillesecurity.com/tutorial-writing-a-pe-packer-part-4/)
				* [Part 5](https://bidouillesecurity.com/tutorial-writing-a-pe-packer-part-5/)
		- **Articles/Blogposts/Writeups**
		- **Papers**
			* [Anti-Unpacker Tricks - Peter Ferrie](https://web.archive.org/web/20160328144423/http://pferrie.tripod.com/papers/unpackers.pdf)
				* "Unpackers are as old as the packers themselves, but anti-unpacking tricks are a more recent development. These anti-unpacking tricks have developed quickly in number and, in some cases, complexity. In this paper, we will describe some of the most common anti-unpacking tricks, along with some countermeasures.
		- **Tools**
			* [Pakkero](https://github.com/89luca89/pakkero)
				* Pakkero is a binary packer written in Go made for fun and educational purpose. Its main goal is to take in input a program file (elf binary, script, even appimage) and compress it, protect it from tampering and intrusion.
	- **USB**
		* [libusb](https://github.com/libusb/libusb)
			* libusb is a library for USB device access from Linux, macOS, Windows, OpenBSD/NetBSD, Haiku and Solaris userspace.
- **General Evasion Stuff**<a name="evasion"></a>
	- **Articles/Blogposts/Writeups**
		* [How “Encrypted and Authenticated” Payload is Constructed - secfu.net](https://www.secfu.net/2020/06/28/how-encrypted-and-authenticated-payload-is-constructed/)
		* [Hindering Threat Hunting, a tale of evasion in a restricted environment - Borja Merino(2020)](https://www.blackarrow.net/hindering-threat-hunting-a-tale-of-evasion-in-a-restricted-environment/)
		* [Evadere Classifications - Jonathan Johnson(2021)](https://posts.specterops.io/evadere-classifications-8851a429c94b?gi=b4339934bff4)
	- **Talks/Presentations/Videos**
		* [Adventures in Asymmetric Warfare - Will Schroeder(BSides Augusta2014)](https://www.youtube.com/watch?v=53qQfCkVM_o)
			* As a co-founder and principal developer of the Veil-Framework, the speaker has spent a considerable amount of time over the past year and a half researching AV-evasion techniques. This talk will briefly cover the problem space of antivirus detection, as well as the reaction to the initial release of Veil-Evasion, a tool for generating AV-evading executables that implements much of the speaker’s research. We will trace through the evolution of the obfuscation techniques utilized by Veil-Evasion’s generation methods, culminating in the release of an entirely new payload language class, as well as the release of a new ..NET encryptor. The talk will conclude with some basic static analysis of several Veil-Evasion payload families, showing once and for all that antivirus static signature detection is dead.
	- **Tools**
		* [HashDB](https://github.com/OALabs/hashdb)
			* HashDB can be used as a stand alone hashing library, but it also feeds the HashDB Lookup Service run by OALabs. This service allows analysts to reverse hashes and retrieve hashed API names and string values.
- **Updates**<a name="updates"></a>
	- **101**
		* [The Update Framework: A framework for securing software update systems](https://theupdateframework.io/)
		* [The Update Framework (TUF) - code](https://github.com/theupdateframework)
	- **Articles/Blogposts/Writeups**
	- **Tools**
- **Network Communications**<a name="netcomms"></a>
	* **Agnostic**
		* [Securing Custom Protocols With Noise - grund.me(2021)](https://grund.me/posts/securing-custom-protocols-with-noise/)	
	- **Articles/Blogposts/Writeups**<a name="netcomart"></a>
		* [Designing Peer-To-Peer Command and Control - cobbr(2019)](https://cobbr.io/Designing-Peer-To-Peer-C2.html)
			* "In this post we will discuss the design and implementation of peer-to-peer command and control protocols in general, as well as the concrete example of the peer-to-peer design implemented in Covenant, an open-source command and control framework, as of v0.2 (released today), which I will refer to often."
	- **Talks/Presentations**<a name="c2comtalks"></a>
		* [DIY Command & Control For Fun And *No* Profit - David Schwartzberg(Derbycon2013)](https://www.irongeek.com/i.php?page=videos/derbycon3/3106-diy-command-control-for-fun-and-no-profit-david-schwartzberg)
			* Description: Many security professionals have heard about Command & Control botnets, even more have been infected by them. Very few have had the opportunity to actually look inside the server control panel of a C&C. This mainly hands – on presentation will walk you through a very dark corner of the Internet and provide a glimpse of the daily life of a cybercriminal. Live malware will be used during this presentation so make sure you turn off your Wi-Fi.
		* [C2 Channels - Creative Evasion - Justin Wilson(Derbycon2017)](https://www.irongeek.com/i.php?page=videos/derbycon7/s22-c2-channels-creative-evasion-justin-wilson)
		* Shining light on new ways attackers are being creative with C2 channels.
		* [Designing & building a stealth C2 LDAP channel - Rindert Kramer(Derbycon2019)](https://www.irongeek.com/i.php?page=videos/derbycon9/stable-04-designing-building-a-stealth-c2-ldap-channel-rindert-kramer)
			* When organizations choose to isolate networks, they often choose to implement technologies like private VLANs, use separate hosts and hypervisors and maybe even separate physical locations in order to guarantee the isolation. But what if these separated environments share the same Active Directory environment? It's not hard to come up with ideas why this might seem like a good idea, however, it also provides an opportunity to exchange data over LDAP. After all, even in non-Windows environments LDAP is still used as a central node within the network. During this talk I will go into detail about the process of designing & building a stealth C2 LDAP channel, which makes communication between different strictly firewalled network segments possible.
		* [Killsuit: The Equation Group's Swiss Army knife for persistence, evasion, and data exfil - Francisco Donoso(Derbycon2018)](https://www.irongeek.com/i.php?page=videos/derbycon8/track-3-17-killsuit-the-equation-groups-swiss-army-knife-for-persistence-evasion-and-data-exfil-francisco-donoso)
			* Most researchers have focused on the Equation Group's brilliant exploits but very few researchers have focused on their extremely effective post exploitation capabilities. During this talk, we will dissect the KillSuit framework, the Equation Group's Swiss Army Knife for persistence, information gathering, defense evasion, and data exfiltration. KillSuit is a little-known part of the DanderSpritz post-exploitation toolkit, leaked by the Shadow Brokers in April 2017. KillSuit is a full featured and versatile framework used by a variety of the Equation Group's tools and implants. KillSuit provides the ability to stealthily establish persistence on machines, install keyloggers, packet capture tools, perform WiFi MITM, and other more information gathering tools. Killsuit includes many interesting ways to silently exfiltrate data and intel - including custom written IPSEC-like protocols and misuse of ""disabled"" WIFI cards and near-by open networks.
		* [Sharing the Myth - Cody Thomas(2020)](https://posts.specterops.io/sharing-the-myth-d14eb1b4fc23)
		* [Mythic External Agent](https://github.com/its-a-feature/Mythic_External_Agent)
			* This repo defines the folder structure for an external Mythic agent that can be remotely "installed" into a Mythic instance. This process allows users to create their own Mythic agents and host them on their own GitHub repositories while also allowing an easy process to install agents.
		* [LARRYCHATTER](https://github.com/slaeryan/LARRYCHATTER)
			*  Covert C2 Framework - PoC HAMMERTOSS Revenant - C2 over Twitter
		* [Hunting the Hunters - RCE in Covenant C2 - 0xcoastal(2020)](https://blog.null.farm/hunting-the-hunters)
		* [Foxtrot C2: A Journey of Payload Delivery - Dimitry Snezhkov(Derbycon2018)](https://www.irongeek.com/i.php?page=videos/derbycon8/stable-11-foxtrot-c2-a-journey-of-payload-delivery-dimitry-snezhkov)
			* [Slides](https://www.slideshare.net/dimas050/foxtrot-c2-a-journey-of-payload-delivery)
			* Execution of an offensive payload may begin with a safe delivery of the payload to the endpoint itself. When secure connections in the enterprise are inspected, reliance only on transmission level security may not be enough to accomplish that goal. Foxtrot C2 serves one goal: safe last mile delivery of payloads and commands between the external network and the internal point of presence, traversing intercepting proxies, with the end-to-end application level encryption. While the idea of end-to-end application encryption is certainly not new, the exact mechanism of Foxtrot's delivery implementation has advantages to Red Teams as it relies on a well known third party site, enjoying elevated ranking and above average domain fronting features. Payload delivery involves several OpSec defenses: sensible protection from direct attribution, active link expiration to evade consistent interception, inspection, tracking and replay activities by the defenders. Asymmetric communication channels will also be used. And if your standalone Foxtrot agent is caught, the delivery mechanism may live on, you could still manually bring the agent back into the environment via the browser. A concept tool built on these ideas will be presented and released. It will be used as basis for our discussion.
		* [99 Reasons Your Perimeter Is Leaking - Evolution of C&C - John Askew(Derbycon2018)](https://www.irongeek.com/i.php?page=videos/derbycon8/track-4-11-99-reasons-your-perimeter-is-leaking-evolution-of-cc-john-askew)
			* From the venerable bind shell, to the reverse shell, the IRC bot channel, the icmp/dns/custom UDP tunnel, and the asynchronous HTTP C&C server, remote access has taken many forms since we first began remotely exploiting software. Even today, many traditional methods will still frequently bypass firewalls and detection, and additional methods continue to be devised. But as an attacker, what do I do when my favorite method is blocked? What are my options other than reusing a stale python script from github or creating my own ad-hoc, informally-specified, bug-ridden, slow implementation of a high-level messaging protocol? And as a defender, how can I measure my ability to detect the diverse C&C traffic that may be seen today, and also prepare for new and unexpected channels? In this talk, we will discuss the evolution of command and control methods, their strengths and weaknesses from an attacker's perspective, and the capabilities of a defender to detect and respond to them. We will identify what aspects a forward-thinking C&C framework might require, and then demonstrate a proof-of-concept with 99(ish) different interchangeable methods for communication. Finally, we will discuss some of the shortcomings of egress filtering in enterprise environments that should be addressed in order to mature our detection and response in kind.
		* [Victim Machine has joined #general: Using Third Party APIs as C&C Infrastructure - Stephen Hilt, Lord Alfred Remorin(Derbycon2017)](https://www.irongeek.com/i.php?page=videos/derbycon7/t115-victim-machine-has-joined-general-using-third-party-apis-as-cc-infrastructure-stephen-hilt-lord-alfred-remorin)
			* The popularity of third party chat applications is on the rise for both personal and enterprise use. They provide the ability to send brief messages similar to previously popular platforms such as ICQ, AIM, and even IRC. However, one of the main reasons they are being adopted is due to their functionality and cost. The challenge is that these same benefits are attracting cybercriminals to the services.   Cybercriminals are utilizing legitimate chat services as command and control channels to facilitate malicious activity. To achieve this, actors are using the platforms’ API services to integrate custom applications within the chat platforms. On most of these platforms, “bots” are automated scripts that are running on a remote machine to provide integrated information, including anything from a cat fact and meme creation, to running OS commands. The APIs allow for flexibility to listen for an action and then perform a task based on the information. Threat actors are taking notice of this and utilizing API functions for command and control. This talk will delve into the API functions, and how malware and cybercriminals are utilizing these functions as command and control capabilities. Attendees will understand how to identify, mitigate and prevent such communications from happening in their own organizations.
		* [The Art of C2: Myths vs. Reality - Yossi Sassi, Dor Amit(BSidesTLV2020)](https://www.youtube.com/watch?v=Gy_UKIzYohY&feature=share)
		* [Functional Cloud C2 - Chris Truncer(SANS HackFest Summit 2020)](https://www.youtube.com/watch?v=FYZWOBR3g3o&list=PLdVJWiil7RxoW8rBeKc0flY8bRuD3M68L&index=13)
			* It’s no surprise that attackers repurpose legitimate cloud services for malicious use, such as command and control. Defenders are also aware of this shift and have spent their time researching this move to build better defenses. As such, attackers are forced to innovate.  Azure Functions is Microsoft’s entry into “server-less code”. Beyond developing code that can run anywhere in the cloud, it provides users with the ability to trigger arbitrary code execution that performs any task you’ve developed, including proxying communications. We’re going to look at how Azure Functions can be leveraged by security professionals, and attackers, for command and control.  This talk will dive into two methods for establishing command and control communications while leveraging the cloud to control compromised systems.
	- **Data-Serialization-related**
		- **Cap'n Proto**
			* [Cap'n Proto](https://capnproto.org/)
		- **FlatBuffers**
			* [FlatBuffers](https://google.github.io/flatbuffers/)
				* FlatBuffers is an efficient cross platform serialization library for C++, C#, C, Go, Java, Kotlin, JavaScript, Lobster, Lua, TypeScript, PHP, Python, Rust and Swift. It was originally created at Google for game development and other performance-critical applications.
		- **Protobufs**
			- **101**
			- **Articles/Blogposts/Writeups**
				* [Practical API Design at Netflix, Part 1: Using Protobuf FieldMask - Alex Borysov, Ricky Gardiner(2021)](https://netflixtechblog.com/practical-api-design-at-netflix-part-1-using-protobuf-fieldmask-35cfdc606518)
					* [Part 2](https://netflixtechblog.com/practical-api-design-at-netflix-part-2-protobuf-fieldmask-for-mutation-operations-2e75e1d230e4?gi=d941091d8f1)
		- **Python**
			* [marshmallow: simplified object serialization](https://marshmallow.readthedocs.io/en/stable/)
				* marshmallow is an ORM/ODM/framework-agnostic library for converting complex datatypes, such as objects, to and from native Python datatypes.
	- **Authentication Methods**
		* **OPAQUE**
			* [opaque(rust implementation)](https://github.com/gustin/opaque)
				* OPAQUE protocol, a secure asymmetric password authenticated key exchange (aPAKE) that supports mutual authentication in a client-server setting without reliance on PKI and with security against pre-computation attacks upon server compromise.
	- **Tools**
		* [Toxiproxy](https://github.com/Shopify/toxiproxy)
			* A TCP proxy to simulate network and system conditions for chaos and resiliency testing
- **Communication Channel Examples/Samples/PoCs**<a name="c2commsamples"></a>
	- **Samples**
		* [cflsh](https://github.com/dsnezhkov/cflsh)
			* CloudFlare Worker Shell
		* [Mistica](https://github.com/IncideDigital/Mistica)
			* An open source swiss army knife for arbitrary communication over application protocols
	- **404**
		* [How to Build a 404 page not found C2](https://www.blackhillsinfosec.com/?p=5134)
		* [404 File not found C2 PoC](https://github.com/theG3ist/404)
	- **ActiveDirectory Features**
		* [Command and Control Using Active Directory - harmj0y(2016)](http://www.harmj0y.net/blog/powershell/command-and-control-using-active-directory/)
		* [Active Directory as a C2 (Command & Control) - akijos(2018)](https://akijosberryblog.wordpress.com/2018/03/17/active-directory-as-a-c2-command-control/)
	- **ARP**
		* [Zarp](https://github.com/hatRiot/zarp)
			* Zarp is a network attack tool centered around the exploitation of local networks. This does not include system exploitation, but rather abusing networking protocols and stacks to take over, infiltrate, and knock out. Sessions can be managed to quickly poison and sniff multiple systems at once, dumping sensitive information automatically or to the attacker directly. Various sniffers are included to automatically parse usernames and passwords from various protocols, as well as view HTTP traffic and more. DoS attacks are included to knock out various systems and applications.
	- **Browser**
		* [Browser-C2](https://github.com/0x09AL/Browser-C2)
			* Post Exploitation agent which uses a browser to do C2 operations.
		* [Using Firefox webextensions as c2 client - Matheus Bernardes](https://mthbernardes.github.io/persistence/2019/03/07/using-firefox-webextensions-as-c2-client.html)
		* [InternetExplorer.Application for C2 - @leoloobeek(2017)](https://adapt-and-attack.com/2017/12/19/internetexplorer-application-for-c2/)
			* Using IE COM object for comms.
	- **Chrome Extension**
		* [Abusing Google Chrome extension syncing for data exfiltration and C&C - Bojan(Sans(2021))](https://isc.sans.edu/forums/diary/Abusing+Google+Chrome+extension+syncing+for+data+exfiltration+and+CC/27066/)
	- **Cobalt Strike**
		* [External C2](https://github.com/ryhanson/ExternalC2)
			* A library for integrating communication channels with the Cobalt Strike External C2 server
	- **DNS**
		- **101**
			* [Domain Name System - Wikipedia](https://wikipedia.org/wiki/Domain_Name_System)
			* [Multicast DNS - Wikipedia](https://en.wikipedia.org/wiki/Multicast_DNS)
		- **Articles/Blogposts/Writeups**
			* [C2 with DNS - NetbiosX(2017)](https://pentestlab.blog/2017/09/06/command-and-control-dns/)
			* [DNS for red team purposes - redteam.pl(2020)](https://blog.redteam.pl/2020/03/dns-c2-rebinding-fast-flux.html?m=1)
				* In the following blog post I would like to demonstrate a proof-of-concept for how red teamers can build DNS command & control (DNS C2, DNS C&C), perform DNS rebinding attack and create fast flux DNS. We will focus only on the DNS server part without building a complete working platform.			
		- **Tools**
			* [dnscat2-powershell](https://github.com/lukebaggett/dnscat2-powershell)
				* A Powershell client for dnscat2, an encrypted DNS command and control tool
			* [DNS-Persist](https://github.com/0x09AL/DNS-Persist)
				* DNS-Persist is a post-exploitation agent which uses DNS for command and control. The server-side code is in Python and the agent is coded in C++.
			* [ddor](https://github.com/rek7/ddoor)
				* ddor is a cross platform light weight backdoor that uses txt records to execute commands on infected machines.
			* [DNSStager](https://github.com/mhaskar/DNSStager)
				* "DNSStager is an open-source project based on Python used to hide and transfer your payload using DNS. DNSStager will create a malicious DNS server that handles DNS requests to your domain and return your payload as a response to specific record requests such as AAAA or TXT records after splitting it into chunks and encoding the payload using different algorithms."
	- **DNS-over-HTTPS(DoH)**
		* **101**
			* [DNS over HTTPS - Wikipedia](https://en.wikipedia.org/wiki/DNS_over_HTTPS)
			* [RFC 8484: DNS Queries over HTTPS (DoH)](https://datatracker.ietf.org/doc/html/rfc8484)
				* "This document defines a protocol for sending DNS queries and getting DNS responses over HTTPS.  Each DNS query-response pair is mapped into an HTTP exchange."
		* **Articles/Blogposts/Writeups**
			* [Playing with DNS over HTTPS (DoH) - DTM(2018)](https://dtm.uk/playing-with-dns-over-https/)
			* [DNS over HTTPS (DoH) Servers - DTM(2018)](https://dtm.uk/dns-over-https-doh-servers/)
			* [DNS Over HTTPS for Cobalt Strike - Kyle Avery(2021)](https://www.blackhillsinfosec.com/dns-over-https-for-cobalt-strike/)
		* **Tools**
			* [DoH-Stager](https://github.com/APTortellini/DoH-Stager)
				* "DoH-Stager is an expansion of the awesome DNSStager tool made by @mohammadaskar2. DoH-Stager is aimed at providing the same functionalities as the original version, but using DNS-over-HTTPS instead of classic DNS."
			* [TitanLdr](https://github.com/SecIdiot/TitanLdr)
				* "Titan: A crappy Reflective Loader written in C and assembly for Cobalt Strike. Redirects DNS Beacon over DoH"
	- **Email**
		- **Agnostic**
			* [DicerosBicornis](https://github.com/maldevel/dicerosbicornis)
				* A stealthy Python based Windows backdoor that uses email as a command and control server.
		- **Gmail**
			* [gcat](https://github.com/s1l3nt78/gcat)
				* Command Line RAT that uses Gmail as its central C2Server. Bypassing common issues, such as the need for port forwarding or proxies.
	- **Firefox Send**
		* [Foxtrot C2](https://github.com/dsnezhkov/foxtrot)
			* C&C to deliver files and shuttle command execution instructions between an external actor and an internal agent with the help of Firefox Private Encrypted File Sharing 
	- **Google Translate**
		* [GTRS - Google Translator Reverse Shell](https://github.com/mthbernardes/GTRS/blob/master/README.md)
			* This tools uses Google Translator as a proxy to send arbitrary commands to an infected machine.
		* [BabyShark](https://github.com/UnkL4b/BabyShark)
	- **HTTP/S**
		* **101**
		* **Articles/Blogposts/Writeups**
			* [C2 with https](https://pentestlab.blog/2017/10/04/command-and-control-https/)
		* **Tools**
			* [Galvatron](https://github.com/khr0x40sh/Galvatron)
				* Powershell fork of Monohard by Carlos Ganoza P. This botnet/backdoor was designed to egress over unecrypted web using very little, but effective obfuscation. Egress over ICMP and DNS are planned as features. Lastly, the server code is designed to setup the C2 on a LAMP-esque server. The default creds are admin/admin.
			* [C2 over TLS Certs - Casey Smith](https://gist.github.com/caseysmithrc/a4c4748160ff9c782d8a86723dbc7334?t=1&cn=ZmxleGlibGVfcmVjcw%3D%3D&refsrc=email&iid=6e15d70104f847a8ae7723921067fe1d&fl=4&uid=150127534&nid=244+285282312)
			* [ThunderShell](https://github.com/Mr-Un1k0d3r/ThunderShell)
				* ThunderShell is a Powershell based RAT that rely on HTTP request to communicate. All the network traffic is encrypted using a second layer of RC4 to avoid SSL interception and defeat network hooks.
			* [FruityC2](https://github.com/xtr4nge/FruityC2)
				* FruityC2 is a post-exploitation (and open source) framework based on the deployment of agents on compromised machines. Agents are managed from a web interface under the control of an operator.
			* [PlugBot-C2C](https://github.com/redteamsecurity/PlugBot-C2C)
				* This is the Command & Control component of the PlugBot project
			* [EggShell](https://github.com/neoneggplant/EggShell)
				* EggShell is an iOS and macOS post exploitation surveillance pentest tool written in Python. This tool creates 1 line multi stage payloads that give you a command line session with extra functionality. EggShell gives you the power and convenience of uploading/downloading files, taking pictures, location tracking, shell command execution, persistence, escalating privileges, password retrieval, and much more. Server communication features end to end encryption with 128 bit AES and the ability to handle multiple clients. This is a proof of concept pentest tool, intended for use on machines you own.
			* [EggShell Blogpost](http://lucasjackson.me/dWkKX/index.php/eggshell)
			* [A Guide to Configuring Throwback](https://silentbreaksecurity.com/throwback-thursday-a-guide-to-configuring-throwback/)
				* [Throwback - beacon](https://github.com/silentbreaksec/Throwback)
				* [Throwback Listener](https://github.com/silentbreaksec/ThrowbackLP)
	- **HTTP/2**
		* **101**
		* **Articles/Blogposts/Writeups**
		* **Tools**
	- **HTTP3**
		* **101**
		* **Articles/Blogposts/Writeups**
		* **Tools**
			* [Merlin](https://github.com/Ne0nd0g/merlin)
				* Merlin is a cross-platform post-exploitation HTTP/2 Command & Control server and agent written in golang.
	- **ICMP**
		* [ICMP C2](https://pentestlab.blog/2017/07/28/command-and-control-icmp/)
		* [C2 with ICMP](https://pentestlab.blog/2017/07/28/command-and-control-icmp/)
	- **Images/Imgur**
		* [Dali](https://github.com/h0mbre/Dali)
			* Dali is the server-side half of an image-based C2 channel which utilizes Imgur to host images and task agents.
	- **Named Pipes**
		* [AsyncNamedPipes](https://github.com/rasta-mouse/AsyncNamedPipes)
			* Quick PoC to send and receive messages over Named Pipes asynchronously. Start Server.exe and then Client.exe.
	- **OCR**
		* [Implementing Proof-of-Concept C2 with Microsoft OCR - Adrian Denkiewicz(CQLabs2020)](https://cqureacademy.com/cqure-labs/implementing-proof-of-concept-c2-with-microsoft-ocr)
	- **Office365**
		* [Callidus](https://github.com/3xpl01tc0d3r/Callidus)
			* Latin word for “sneaky” is called “Callidus”. It is developed for learning and improving my knowledge about developing custom toolset in C# and learning how to leverage cloud services for the benefit of the user. It is developed using .net core framework in C# language. Allows operators to leverage O365 services for establishing command & control communication channel. It usages Microsoft Graph APIs for communicating with O365 services.
		* [Introduction to Callidus - 3xpl01tc0d3r(2020)](https://3xpl01tc0d3r.blogspot.com/2020/03/introduction-to-callidus.html)
	- **PAC**
		* [Pacdoor](https://github.com/SafeBreach-Labs/pacdoor)
			* Pacdoor is a proof-of-concept JavaScript malware implemented as a Proxy Auto-Configuration (PAC) File. Pacdoor includes a 2-way communication channel, ability to exfiltrate HTTPS URLs, disable access to cherry-picked URLs etc.
	- **Print Jobs**
		* [Using and detecting C2 printer pivoting - Alfie Champion, James Coote(2020)](https://labs.f-secure.com/blog/print-c2/)
			* This post introduces the novel concept of Command & Control (C2) using print jobs, and demonstrates how this can be achieved using C3's Print channel. It also explores the OPSEC considerations behind the use of this technique, and outlines the detection opportunities that it can create.
	- **QUIC**
		* **101**
		* **Articles/Blogposts/Writeups**
		* **Tools**
	- **Reddit**
		* [The Resilient Reddit C2](https://www.irongeek.com/i.php?page=videos/circlecitycon2019/track-2-08-the-resilient-reddit-c2-zach-zenner)
			* Twitter is frequently utilized to issue commands to a botnet: an account creates a post that is ran by a program locally on a user’s computer. Why limit it to Twitter? Reddit is a very viable platform that can be used to perform Command and Control operations while being able to blend in with other users as well as other network traffic. By combining multiple accounts with the post structure of Reddit, a Command and Control Herder can be persistent even past account or post deletion.
	- **SSH** 
		* [Spidernet](https://github.com/wandering-nomad/Spidernet)
			* Proof of Concept of SSH Botnet C&C Using Python 
	- **Social Media-based**
		* [JSBN](https://github.com/Plazmaz/JSBN)
			* JSBN is a bot client which interprets commands through Twitter, requiring no hosting of servers or infected hosts from the command issuer. It is written purely in javascript as a Proof-of-Concept for javascript's botnet potentials.
		* [C2 with twitter](https://pentestlab.blog/2017/09/26/command-and-control-twitter/)
		* [C2 with Telegram](https://github.com/graniet/gshark-framework)
		* [BrainDamage](https://github.com/mehulj94/BrainDamage)
			* A fully featured backdoor that uses Telegram as a C&C server
		* [twittor - twitter based backdoor](https://github.com/PaulSec/twittor)
			* A stealthy Python based backdoor that uses Twitter (Direct Messages) as a command and control server This project has been inspired by Gcat which does the same but using a Gmail account.
		* [Instegogram](https://github.com/endgameinc/instegogram)
		* [canisrufus](https://github.com/maldevel/canisrufus)
			* A stealthy Python based Windows backdoor that uses Github as a command and control server.
	- **SQL Server**
		* [Databases and Clouds: SQL Server as a C2 - Scott Sutherland](https://blog.netspi.com/databases-and-clouds-sql-server-as-a-c2/)
	- **Trello**
		* [TrelloC2](https://github.com/securemode/TrelloC2)
			* Simple C2 over the Trello API
	- **WebDAV**
		* [C2 with webdav](https://pentestlab.blog/2017/09/12/command-and-control-webdav/)
		* [Using WebDAV features as a covert channel](https://arno0x0x.wordpress.com/2017/09/07/using-webdav-features-as-a-covert-channel/)
	- **Web Services**
		* [C2 with Dropbox](https://pentestlab.blog/2017/08/29/command-and-control-dropbox/)
		* [DBC2](https://github.com/Arno0x/DBC2)
			* DBC2 (DropboxC2) is a modular post-exploitation tool, composed of an agent running on the victim's machine, a controler, running on any machine, powershell modules, and Dropbox servers as a means of communication.
		* [C2 with gmail](https://pentestlab.blog/2017/08/03/command-and-control-gmail/)	
		* [Simple domain fronting PoC with GAE C2 server](https://www.securityartwork.es/2017/01/31/simple-domain-fronting-poc-with-gae-c2-server/)
		* [google_socks](https://github.com/lukebaggett/google_socks)
			* A proof of concept demonstrating the use of Google Drive for command and control.
		* [Powershell Github Shell](https://github.com/zlocal/Powershell-Github-Shell)
		* [google_RAT](https://github.com/a-rey/google_RAT)
			* A remote access tool for Windows systems using google apps script as the middle man
	- **WebSockets**
		* [WSC2](https://github.com/Arno0x/WSC2)
			* WSC2 is a PoC of using the WebSockets and a browser process to serve as a C2 communication channel between an agent, running on the target system, and a controller acting as the actual C2 server.
		* [Using WebSockets and IE/Edge for C2 communications](https://arno0x0x.wordpress.com/2017/11/10/https://github.com/leoloobeek/GoGreen/blob/master/README.mdusing-websockets-and-ie-edge-for-c2-communications/)
		* [MurDock - Mutable Universal Relay Document Kit](https://github.com/themson/MurDocK)
			* The purpose of this tool is to provide a protocol independent framework that contains a base set of features that can piggyback on top of any collaborative web platform or service. The base docClient and docServer are meant to be extended upon with Buffer classes written for individual web services. These buffer classes can be plugged into the MurDock framework in order to create a unique shell infrastructure that will always contains a base set of features, as well as the ability to tunnel over any web application traffic for which a buffer class has been constructed. The framework can be extended to operate over lower level protocols if desired.
		* [PetaQ](https://github.com/fozavci/petaqc2)
			* PetaQ is a malware which is being developed in .NET Core/Framework to use websockets as Command & Control (C2) channels. It's designed to provide a Proof of Concept (PoC) websocket malware to the adversary simulation exercises (Red & Purple Team exercises).
	- **WireGuard**
		* **101**
		* **Articles/Blogposts/Writeups**
		* **Tools**
			* [onetun](https://github.com/aramperes/onetun)
	- **WMI-based**
		* [WMImplant](https://github.com/ChrisTruncer/WMImplant)
			* WMImplant is a PowerShell based tool that leverages WMI to both perform actions against targeted machines, but also as the C2 channel for issuing commands and receiving results. WMImplant will likely require local administrator permissions on the targeted machine.	
		* [WheresMyImplant](https://github.com/0xbadjuju/WheresMyImplant)
			* A Bring Your Own Land Toolkit that Doubles as a WMI Provider 
		* [PowerProvider](https://github.com/0xbadjuju/PowerProvider/)
			* PowerProvider: A toolkit to manipulate WMI. Used with WheresMyImplant
	- **Tricks**<a name="tricks1"></a>
		- **Port Multiplexing**
			* **101**
				* [TCP Port Service Multiplexer - Wikipedia](https://en.wikipedia.org/wiki/TCP_Port_Service_Multiplexer)
				* [Multiplexing and Demultiplexing in Transport Layer - GeeksforGeeks(2021)](https://www.geeksforgeeks.org/multiplexing-and-demultiplexing-in-transport-layer/)
				* [Understanding TCP and UDP Multiplexing - Imad Daou](https://www.ccnahub.com/ip-fundamentals/understanding-tcp-and-udp-multiplexing/)
				* [OpenSSH/Cookbook/Multiplexing](https://en.wikibooks.org/wiki/OpenSSH/Cookbook/Multiplexing)
			* **Tools**
				* [sslh](https://github.com/yrutschle/sslh)
					* Applicative Protocol Multiplexer (e.g. share SSH and HTTPS on the same port)
- **Publishing**<a name="ipub"></a>
	- **Linux**
		* [fpm](https://github.com/jordansissel/fpm)
			*  Effing package management! Build packages for multiple platforms (deb, rpm, etc) with great ease and sanity. 
	- **Windows**
		* **Converting an .exe to an .msi**
			* [Exe to MSI Converter](http://www.exetomsi.com/)
			* [EMCO MSI Package Builder](https://emcosoftware.com/msi-package-builder)
- **Language Specific**<a name="langspec"></a>
	- **AutoIT**<a name="autoitlang"></a>
		- **101**
			* [Auto(It)mating your .NET tradecraft - vivi(2021)](https://thevivi.net/blog/pentesting/2021-11-24-autoitmating-your-dotnet-tradecraft/)
		- **Collection**
			* [OffensiveAutoIT](https://github.com/V1V1/OffensiveAutoIt)
	- **Basic**<a name="basiclang"></a>
	- **C**<a name="clang"></a>
		- **ASM-related**
			* **Articles/Blogposts/Writeups**
				* [Abusing Forced Inline in C - Jurriaan Bremer(2012)](http://jbremer.org/abusing-forced-inline-in-c/)
					* [Part 2](http://jbremer.org/abusing-forced-inline-part-2-breakpoints/)
			* **Tools**
				* [Template Assembly (tasm)](https://github.com/mattbierner/Template-Assembly)
					* Uses C++ templates to embed x86 assembly code directly in normal C++ at compile-time using a domain specific language.		
				* [Assemblyline](https://github.com/0xADE1A1DE/AssemblyLine)
					* A C library and binary for generating machine code of x86_64 assembly language and executing on the fly without invoking another compiler, assembler or linker.
		- **Binary Files**
			* [LIEF](https://github.com/lief-project/LIEF)
				* LIEF - Library to Instrument Executable Formats. The purpose of this project is to provide a cross platform library which can parse, modify and abstract ELF, PE and MachO formats.
			* [Binary Loaders(C)](https://github.com/malisal/loaders)
				* This repo is about small, self-contained implementations of various binary formats loaders (Macho on OSX, ELF on Linux/`*BSD` and PE on Windows). The rationale for these libraries is the following: You wrote an exploit and achieved arbitrary code execution. Now what? These loaders enable you to load and execute an arbitrary binary in your exploited process. The loaders are coded in a way that it's all done in memory, and they do not require access to system libraries/methods - it's all resolved on the fly. The Macho loader enables you to run bundle files, the ELF loader standard ELF files (no shared objects), and the PE loader enables you to run both DLLs and PE files alike.
		- **Building/Compiler-related**
			* **Articles/Blogposts/Writeups**
				* [Getting the maximum of your C compiler, for security - airbus-seclab](https://airbus-seclab.github.io/c-compiler-security/)
			* **Tools**
				* [ocean](https://github.com/STBoyden/ocean)
					* A C/C++ build system/project manager written in Rust; Ocean is a project manager, similar to Rust's Cargo, for C and C++ written with Rust - that other systems programming language. The command syntax is very similar to that of Cargo's.
				* [Awesome CMake](https://github.com/onqtam/awesome-cmake)
					* A curated list of awesome CMake resources, scripts, modules and examples.
				* [CMake Examples](https://github.com/ttroy50/cmake-examples)
					* Useful CMake Examples
				* [VC-LTL](https://github.com/Chuyu-Team/VC-LTL5)
					* Shared to msvcrt.dll or ucrtbase.dll and optimize the C/C++ application file size.
				* [Cosmopolitan](https://justine.lol/cosmopolitan/)
					* " Cosmopolitan makes C a build-once run-anywhere language, similar to Java, except it doesn't require interpreters or virtual machines be installed beforehand. Cosmo provides the same portability benefits as high-level languages like Go and Rust, but it doesn't invent a new language and you won't need to configure a CI system to build separate binaries for each operating system. What Cosmopolitan focuses on is fixing C by decoupling it from platforms, so it can be pleasant to use for writing small unix programs that are easily distributed to a much broader audience. "
					* [Code](https://github.com/jart/cosmopolitan)
		- **C to X Lang**
			- **Go**
				* [c2goasm: C to Go Assembly](https://github.com/minio/c2goasm)
					* This is a tool to convert assembly as generated by a C/C++ compiler into Golang assembly. It is meant to be used in combination with asm2plan9s in order to automatically generate pure Go wrappers for C/C++ code (that may for instance take advantage of compiler SIMD intrinsics or template<> code).
			- **Rust**
				* [C2Rust](https://github.com/immunant/c2rust)
					* "C2Rust helps you migrate C99-compliant code to Rust. The translator (or transpiler) produces unsafe Rust code that closely mirrors the input C code. The primary goal of the translator is to preserve functionality; test suites should continue to pass after translation. Generating safe and idiomatic Rust code from C ultimately requires manual effort. However, we are building a scriptable refactoring tool that reduces the tedium of doing so. You can also cross-check the translated code against the original (tutorial)."
		- **CLI Parameters**
			* [ParamKit](https://github.com/hasherezade/paramkit)
				* A small library helping to parse commandline parameters (for C/C++ on Windows).
		- **Collection**
			* [wcap](https://github.com/mmozeiko/wcap)
				* Simple and efficient screen recording utility for Windows.
		- **Cryptographic Operations**
			- **Collections of**
				* [WjCryptLib](https://github.com/WaterJuice/WjCryptLib)
					* Public Domain C Library of Cryptographic functions. Including: MD5, SHA1, SHA256, SHA512, RC4, AES, AES-CTR, AES-OFB, AES-CBC
			- **Encryption**
				* **Articles/Blogposts/Writeups**
					* [String encryption using macro and cryptor - Emeric Nasi(2014)](http://blog.sevagas.com/?String-encryption-using-macro-and)
				* **Tools**
					* [tiny-AES-c](https://github.com/kokke/tiny-AES-c)
						* Small portable AES128/192/256 in C
					* [encrypt](https://github.com/skahwah/encrypt)
						* Pseudorandom AES-256 encryption designed to protect shellcode and arbitrary strings. C# and C/C++ compatible.
			- **Hashing**
				* [xxHash](https://github.com/Cyan4973/xxHash)
					* xxHash is an Extremely fast Hash algorithm, running at RAM speed limits. It successfully completes the SMHasher test suite which evaluates collision, dispersion and randomness qualities of hash functions. Code is highly portable, and hashes are identical across all platforms (little / big endian).
				* [K-Hash](https://github.com/Keith-Cancel/k-hash)
					* "A simple single header 64 bit hash function using only add, sub, ror, and xor. This a just general-purpose hash function for like making hash maps and similar data-structures. It's is not a cryptographic hash function!"
				* [sha-2](https://github.com/amosnier/sha-2)
					* SHA-2 algorithm implementations
		- **Data Storage**
			- **Compression**
				* [tinf - tiny inflate library](https://github.com/jibsen/tinf)
					* "tinf is a small library implementing the decompression algorithm for the deflate compressed data format (called 'inflate'). Deflate compression is used in e.g. zlib, gzip, zip, and png."
			- **Storage**
				* [plf::colony](https://github.com/mattreecebentley/plf_colony)
					* An unordered data container providing fast iteration/insertion/erasure while maintaining pointer/iterator/reference validity to non-erased elements. Documentation and function descriptions here: https://plflib.org/colony.htm#functions
		- **Discovery**
			* [LocalDllParse](https://github.com/N4kedTurtle/LocalDllParse)
				* Checks all loaded Dlls in the current process for a version resource. Useful for identifying EDRs on a system without making calls out of the current process and avoids all commonly monitored API calls. Just a PoC.
			* [process-enumeration-stealth](https://github.com/LloydLabs/process-enumeration-stealth)
				* "This is a simple PoC which allows you to return a list of PIDs currently using NTFS, by querying the \ntfs\ base device (the Windows filesystem base object). Using this method circumvents the need to use typical APIs, such as NtQuerySystemInformation or the higher level EnumProcesses. Using this non-typical reconnaissance method could allow operators to evade typical monitoring on endpoints 🎉. Thank you to Jonas Lyk for originally finding this bug."
			* [Ps-Tools](https://github.com/outflanknl/Ps-Tools)
				* an advanced process monitoring toolkit for offensive operations.
				* [Red Team Tactics: Advanced process monitoring techniques in offensive operations - Cornelis de Plaa(2020)](https://outflank.nl/blog/2020/03/11/red-team-tactics-advanced-process-monitoring-techniques-in-offensive-operations/)
		- **Dissasembly**
			* [x86_dasm](https://github.com/thejanit0r/x86_dasm)
				* "This lightweight library aims at providing x86-64 disassembling features while being compact and simple to understand and fix. There are no dependencies other than the C standard library, which can also be avoided with slight modifications, depending on the compilation options. It does not use any dynamic memory allocation."
		- **ELF Loaders**
		- **Embedded Interpreters/Scripting**
			- **JavaScript**
				* [mujs](https://github.com/ccxvii/mujs)
					* An embeddable Javascript interpreter in C.
		- **Execution**
		- **GUI**
			* **Agnostic**
				* [raygui](https://github.com/raysan5/raygui)
					* raygui is a simple and easy-to-use immediate-mode-gui library.
			* **Linux**
			* **macOS**
			* **Windows**	
				* [SlimApp](https://github.com/HardCoreCodin/SlimApp)
					* A minimalist andf platform-agnostic application layer for writing graphical applications, with a strong emphasis on simplicity and ease of use.
			* [LCUI](https://github.com/lc-soft/LCUI)
				* A small C library for building user interfaces with C, XML and CSS.
		- **`*`-Injection**
			* [LoadLibrary() and GetProcAddress() replacements for x86, x64, and ARM - @zerosum0x0](https://zerosum0x0.blogspot.com/2016/02/loadlibrary-and-getprocaddress.html)
				* [Code](https://github.com/zerosum0x0-archive/archive)
			* [C-S1lentProcess1njector](https://github.com/s1egesystems/C-S1lentProcess1njector)
				* Process Injector written in C that scans for target processes, once found decrypts RC4 encrypted shellcode and injects/executes in target process' space with little CPU & Memory usage. 
			* [SeasideBishop](https://github.com/SolomonSklash/SeasideBishop)
				* A C port of b33f's UrbanBishop
		- **JSON**
			* **Articles/Blogposts/Writeups**
				* [jWrite - A Really Simple JSON Writer in C - tonywilk(2018)](https://www.codeproject.com/Articles/887604/jWrite-a-really-simple-JSON-writer-in-C)
					* [jWrite](https://github.com/jonaskgandersson/jWrite)
			* **Tools**
				* [cJSON](https://github.com/DaveGamble/cJSON)
					* Ultralightweight JSON parser in ANSI C.
		- **Loaders/Stage0/1 Samples**
			* **Articles/Blogposts/Writeups**
				* [Building a Custom shellcode stager with process injection to Bypass Windows Defender - 0xrob(2020)](https://lowery.tech/building-a-custom-shellcode-stager-with-process-injection-to-bypass-windows-defender/)
				* [Building a Custom Shellcode Loader with Syswhispers to Utilise Direct Syscalls  - 0xrob(2021)](https://lowery.tech/building-a-custom-shellcode-loader-with-syswhispers-to-utilise-direct-syscalls/)
				* [Custom C Program to Download and Inject a Sliver Stager - mr.d0x(2021)](https://mrd0x.com/download-and-execute-sliver-stager/)
			* **Examples**
				* [Nobelium PdfDownloadRunAesMalware](https://github.com/boku7/Nobelium-PdfDLRunAesShellcode)
					* A recreation of the "Nobelium" malware based on Microsofts Malware analysis - Part 1: PDF2Pwn
				* [Prism](https://github.com/andreafabrizi/prism)
					* PRISM is an user space stealth reverse shell backdoor, written in pure C.
				* [Ninja_UUID_Runner](https://github.com/boku7/Ninja_UUID_Runner)
					* Module Stomping, No New Thread, HellsGate syscaller, UUID Shellcode Runner for x64 Windows 10!
				* [TitanLdr](https://github.com/SecIdiot/TitanLdr)
					* "Titan: A crappy Reflective Loader written in C and assembly for Cobalt Strike. Redirects DNS Beacon over DoH"
				* [yarhLoader](https://github.com/vxunderground/VXUG-Papers/blob/main/yarhLoader/Main.c)
					* "yarhLoader is an x86/x64 file loader, file reader, and file writer that abuses NTFS File identifiers for file accessibility."
		- **Networking**
			* **Articles/Blogposts/Writeups**
				* [c-ares](https://github.com/c-ares/c-ares)
					* A C library for asynchronous DNS requests
			* **Tools**
				* [HevSocks5Core](https://github.com/heiher/hev-socks5-core)
					* A simple, lightweight socks5 library. (IPv4/IPv6/TCP/UDP/Client/Server)
				* [EDR Sniper](https://github.com/magisterquis/EDRSniper)
					* Windows tool to drop TCP connections as they happen, like a PCAP-based firewall
				* [MbedTLS](https://github.com/ARMmbed/mbedtls)
					* Mbed TLS is a C library that implements cryptographic primitives, X.509 certificate manipulation and the SSL/TLS and DTLS protocols. Its small code footprint makes it suitable for embedded systems.
		- **Obfuscation**
			* **Tools**
				* [CompileTime-String-Encryption](https://github.com/stevemk14ebr/CompileTime-String-Encryption)
					* C++ 17 compile time string encryption supporting vs2010-2019.
		- **PE/COFF/DLL Loading**
			* **Articles/Blogposts/Writeups**
				* [COFFLoader: Building your own in memory loader or how to run BOFs - Kevin Haubris(2021)](https://www.trustedsec.com/blog/coffloader-building-your-own-in-memory-loader-or-how-to-run-bofs/)
			* **Tools/Examples**
				* [pedump](https://github.com/buaabyl/pedump)
					* An simplest PE parser, which list all import and export entries
				* [MemJect](https://github.com/danielkrupinski/MemJect)
					* Simple Dll injector loading from memory. Supports PE header and entry point erasure. Written in C99.
				* [RunPE-In-Memory](https://github.com/aaaddress1/RunPE-In-Memory)
					* Run a Exe File (PE Module) in memory (like an Application Loader)
				* [COFFLoader](https://github.com/trustedsec/COFFLoader)
					* This is a quick and dirty COFF loader (AKA Beacon Object Files). Currently can run un-modified BOF's so it can be used for testing without a CS agent running it. The only exception is that the injection related beacon compatibility functions are just empty.
		- **Polymorphism**
			* [Reflective Polymorphism](https://github.com/zeroSteiner/reflective-polymorphism)
				* This project provides various utilities for the self-modification of PE images with the intention that they can be incorporated into external projects.
		- **Publishing**
			* [tcc - Tiny C Compiler](https://bellard.org/tcc/)
			* [cosmopolitan libc](https://justine.lol/cosmopolitan/index.html)
				*  Cosmopolitan makes C a build-once run-anywhere language, similar to Java, except it doesn't require interpreters or virtual machines be installed beforehand. Cosmo provides the same portability benefits as high-level languages like Go and Rust, but it doesn't invent a new language and you won't need to configure a CI system to build separate binaries for each operating system. What Cosmopolitan focuses on is fixing C by decoupling it from platforms, so it can be pleasant to use for writing small unix programs that are easily distributed to a much broader audience.
				* [Code](https://github.com/jart/cosmopolitan)
		- **Regular Expressions**
			* [tiny-regex-c](https://github.com/kokke/tiny-regex-c)
				* "Small and portable Regular Expression (regex) library written in C."
		* **Samples/Examples**
			* [PersistentCReverseShell](https://github.com/1captainnemo1/PersistentCReverseShell/blob/master/creverse.c)
				*  A PERSISTENT FUD Backdoor ReverseShell coded in C for any Windows distro, that will make itself persistent on every BOOT and fire a decoy app in the foreground while connecting back to the attacker machine as a silent background process , spawning a POWERSHELL on the attacker machine. 
			* [AQUARMOURY](https://github.com/slaeryan/AQUARMOURY)
				* This is a tool suite consisting of miscellaneous offensive tooling aimed at red teamers/penetration testers to primarily aid in Defense Evasion TA0005;
			* [revsh](https://github.com/emptymonkey/revsh)
				* A reverse shell with terminal support, data tunneling, and advanced pivoting capabilities.
		- **Source Obfuscation**
			* [avcleaner](https://github.com/scrt/avcleaner)
				* C/C++ source obfuscator for antivirus bypass
		- **Testing**
			* [Criterion](https://github.com/Snaipe/Criterion)
				* A cross-platform C and C++ unit testing framework for the 21st century
		- **WebServers**
		- **OS Specific**
			- **Linux**
			- **macOS**
			- **Windows**
				* [inline_syscall](https://github.com/JustasMasiulis/inline_syscall)
					* Header only library that allows you to generate direct syscall instructions in an optimized, inlineable and easy to use manner.
		- **Other Stuff(unsorted/didn't fit above)**
	* **C++**<a name="cppp"></a>
		* **Tradecraft**
			* [Building C2 Implants in C++: A Primer - shogunlab(2020)](https://shogunlab.gitbook.io/building-c2-implants-in-cpp-a-primer/)
		* **Binaries**
			* [LIEF](https://github.com/lief-project/LIEF)
				* LIEF - Library to Instrument Executable Formats. The purpose of this project is to provide a cross platform library which can parse, modify and abstract ELF, PE and MachO formats.
		* **Examples/Samples**
			* [serpentine](https://github.com/jafarlihi/serpentine)
				* C++/Win32/Boost Windows RAT (Remote Administration Tool) with a multiplatform Java/Spring RESTful C2 server and Go, C++/Qt5 frontends
			* [ghost](https://github.com/AHXR/ghost)
			* [Source Code Files for Building C2 Implants in C++: A Primer](https://github.com/shogunlab/building-c2-implants-in-cpp)
			* [UBoat HTTP](https://github.com/UBoat-Botnet/UBoat)
				* A proof-of-concept HTTP Botnet designed to replicate a full weaponized commercial botnet.				* [cpp-implant](https://github.com/JLospinoso/cpp-implant)
				*  A simple implant showcasing modern C++ 
			* [revp](https://github.com/jafarlihi/revp)
				* Reverse HTTP proxy that works on Linux, Windows, and macOS. Made with C++ and Boost. 
			* [WSAAcceptBackdoor](https://github.com/EgeBalci/WSAAcceptBackdoor)
				* This project is a POC implementation for a DLL implant that acts as a backdoor for accept Winsock API calls. Once the DLL is injected into the target process, every accept call is intercepted using the Microsoft's detour library and redirected into the BackdooredAccept function. When a socket connection with a pre-defined special source port is establised, BackdooredAccept function launches a cmd.exe process and binds the accepted socket to the process STD(OUT/IN) using a named pipe.
			* [RTO-Implant](https://github.com/jhackz/RTO-Implant)
				* This is an overview of my RTO-Implant from the Malware Development Essentials Course by @Sektor7Net
			* [TinyNuke](https://github.com/rossja/TinyNuke)
				*  zeus-style banking trojan 
			* [Keylogger](https://github.com/EgeBalci/Keylogger)
				* Simple C++ Keylogger...
			* [Callidus](https://github.com/3xpl01tc0d3r/Callidus)
				* [Blogpost](https://3xpl01tc0d3r.blogspot.com/2020/03/introduction-to-callidus.html)
				* Latin word for “sneaky” is called “Callidus”. It is developed for learning and improving my knowledge about developing custom toolset in C# and learning how to leverage cloud services for the benefit of the user. It is developed using .net core framework in C# language. Allows operators to leverage O365 services for establishing command & control communication channel. It usages Microsoft Graph APIs for communicating with O365 services.
		* **Crypter/Obfuscator**
			* **Articles**
				* [C++ Runtime Crypter - ConnorPatterson(2017)](https://www.codeproject.com/Articles/1174823/Cplusplus-Runtime-Crypter)
					* Tutorial on the structure of writing a runtime crypter in C++
				* [Code segment encryption - Emeric Nasi(2014)](http://blog.sevagas.com/?Code-segment-encryption)
			* **Tools/Libraries**
				* [avcleaner](https://github.com/scrt/avcleaner)
					* C/C++ source obfuscator for antivirus bypass
				* [Simple-XTEA-Crypter](https://github.com/NateBrune/Simple-XTEA-Crypter)
					* Simple runtime crypter in C++.
				* [ADVobfuscator](https://github.com/andrivet/ADVobfuscator)
					* ADVobfuscator demonstates how to use C++11/14 language to generate, at compile time, obfuscated code without using any external tool and without modifying the compiler. The technics presented rely only on C++11/14, as standardized by ISO. It shows also how to introduce some form of randomness to generate polymorphic code and it gives some concrete examples like the encryption of strings literals and the obfuscation of calls using finite state machines.
				* [Obfuscate](https://github.com/adamyaxley/Obfuscate)
					* Guaranteed compile-time string literal obfuscation header-only library for C++14.
				* [Rubicon](https://github.com/asaurusrex/Rubicon)
					* "Rubicon is designed to provide a barebones custom encryption algorithm (which I encourage you to further customize!) which will be crafted into C++ payloads for you! That's right, you won't have to write any C++ (but you will need to compile it), but you will benefit from your shellcode being custom encrypted in unmanaged code. It is a basic stream cipher which is implemented as, fundamentally, a Caesar cipher. It is NOT meant to be cryptographically secure, but to prevent automated detection/analysis from detecting malicious payloads. It calls NO crypto libraries when decrypted (except python does call the library secrets, but that isn't inherently for crypto as opposed to randomness), which is a big plus to avoiding automated detection."
				* [cpp-obfuscator](https://github.com/revsic/cpp-obfuscator)
					* C++ implementation of compile time obfuscator
		- **Cryptographic Operations**
			* [plusaes](https://github.com/kkAyataka/plusaes)
				* Header only C++ AES cipher library.
		* **Networking**
			* [liblacewing](https://github.com/udp/lacewing)
				* liblacewing is a library for writing cross-platform, networked applications in C/C++.
			* [winhttp](https://github.com/ericroy/winhttp)
				* C++ wrapper around the WinHTTP library
		* **PE32**
			* [libpebliss](https://github.com/imag0r/libpebliss)
				* Cross-Platform PE(Portable Executable) Manipulating Library
		* **Shellcode/Injection**
			* **Articles**
				* [Shellcode Techniques in C++ - Topher Timzen(2015)](https://www.tophertimzen.com/blog/shellcodeTechniquesCPP/)
			* **Tools/Libraries**
				* [netstub](https://github.com/freesoul/netstub)
					* Create a C++ PE which loads an XTEA-crypted .NET PE shellcode in memory.
				* [Shellcode Compiler](https://github.com/nytrorst/shellcodecompiler)
					* Shellcode Compiler is a program that compiles C/C++ style code into a small, position-independent and NULL-free shellcode for Windows (x86 and x64) and Linux (x86 and x64). It is possible to call any Windows API function or Linux syscall in a user-friendly way.
				* [CodeInjection](https://github.com/revsic/CodeInjection)
					* Code Injection technique written in cpp language
		- **Stage0/1 Loader/Dropper/Shellcode Runners**
			- **Examples/PoCs/Samples**
				* [UUID Loader](https://github.com/pwn1sher/uuid-loader)
					* Experimental Stage-1 Shellcode Loader, using IE COM Object Methods to fetch Shellcode and uses UUID as shellcode.
		* **Unhooking**
			* [Firewalker](https://github.com/mdsecactivebreach/firewalker)
				* This repo contains a simple library which can be used to add FireWalker hook bypass capabilities to existing code;
		* **WebServer**
			* [civeweb](https://github.com/civetweb/civetweb)
				* Embedded C/C++ web server
		* **Other**
			* [cpp_vs_payload_template](https://github.com/0xC0D1F1ED/cpp_vs_payload_template)
				* Visual Studio (C++) Solution Template for Payloads
		* **Windows**
			* [Windows Process Hacking Library](https://github.com/0xZ0F/CPPMemory)
				* Code that can be used as a reference, library, or inspiration for hacking Windows memory.
		* **Virtual calls**
			* [Devirtualization in C++, part 1 -Honza Hubička(2014)](https://hubicka.blogspot.com/2014/01/devirtualization-in-c-part-1.html)
	* **C#**<a name="csharppay"></a>
		* **101**
			* [A tour of the C# language - docs.ms](https://docs.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/)
				* C# (pronounced "See Sharp") is a modern, object-oriented, and type-safe programming language. C# has its roots in the C family of languages and will be immediately familiar to C, C++, Java, and JavaScript programmers. This tour provides an overview of the major components of the language in C# 8 and earlier. 
			* [Donuts!🍩](https://github.com/RandomThings23/donut)
				* DONUTS DONUTS DONUTS 🍩
		* **Learning**
			* [Get started with C# - docs.ms](https://docs.microsoft.com/en-us/dotnet/csharp/getting-started/)
			* [Inside a C# program - docs.ms](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/)
				* The section discusses the general structure of a C# program, and includes the standard "Hello, World!" example.
			* [C# 101 - Channel9 MSDN](https://channel9.msdn.com/Series/CSharp-101)
		* **Reflection**
			* [Security Considerations for Reflection - docs.ms](https://docs.microsoft.com/en-us/dotnet/framework/reflection-and-codedom/security-considerations-for-reflection)
			* [Securing the loading of dynamic code - F-Secure(2016)](https://labs.f-secure.com/archive/securing-the-loading-of-dynamic-code/)
			* [Use reflection to list a class’s properties in C# - Rod Stephens(2018)](http://csharphelper.com/blog/2018/02/use-reflection-to-list-a-classs-properties-in-c/)	
			* [.NET Reflection and Disposable AppDomains - Rasta Mouse(2021)](https://rastamouse.me/net-reflection-and-disposable-appdomains/)
		* **Scripting/ClearScript**
			* [ClearScript](https://github.com/microsoft/ClearScript)
				* A library for adding scripting to .NET applications. Supports V8 (Windows, Linux, macOS) and JScript/VBScript (Windows). 
			* [ClearScript FAQtorial](https://microsoft.github.io/ClearScript/Tutorial/FAQtorial)
			* [Cutting Edge : A Look at ClearScript - Dino Esposito(2014 docs.ms)](https://docs.microsoft.com/en-us/archive/msdn-magazine/2014/september/cutting-edge-a-look-at-clearscript)
		* **Internals**
			* [Ninja Patching .NET - Jon McCoy(Dojocon2010)](https://web.archive.org/web/20170321162306/http://www.irongeek.com/i.php?page=videos/dojocon-2010-videos#Ninja%20Patching%20.NET)
				* [Youtube](https://www.youtube.com/watch?v=3jit5unJzys)
			* [Hacking .NET Applications at Runtime: A Dynamic Attack - Jon McCoy(Defcon18)](https://web.archive.org/web/20191203175515/https://www.defcon.org/html/defcon-18/dc-18-speakers.html#McCoy)
				* [Slides](https://www.defcon.org/images/defcon-19/dc-19-presentations/McCoy/DEFCON-19-McCoy-Hacking-Net.pdf)
			* [Attacking .Net at Runtime - Jonathan McCoy(2013)](https://web.archive.org/web/20181028060806/http://www.digitalbodyguard.com/Papers/Attacking%20.Net%20at%20Runtime.pdf)
				* This paper will introduce methodology forattacking  .NET programs at runtime. Thisattack will grant control over the targetsvariables, core logic, and the GUI. Thisattack is implemented with .NET code,and is heavily based on reflection. 
			* [.NET Method Internals - Common Intermediate Language (CIL) Basics - @mattifestation(2014)](http://www.exploit-monday.com/2014/07/dotNETMethodInternals.html)
			* [Acquiring .NET Objects from the Managed Heap - Topher Timzen(2015)](https://www.tophertimzen.com/resources/grayStorm/AcquiringDotNetObjectsFromTheManagedHeap.pdf)
				* This paper will describe how to use any instantiated objectin the .NET CLR managed heap as if it were declared locally.It will be shown that by referencing object pointers fromthe managed heap, an attacker control objects being used inan application. Reflective techniques will be discussed and asignature will be introduced to find any object on the managedheap
			* [Attacking Microsoft’s .NET Framework Through CLR - Yu Hong, Shikang Xing(HITB2018AMS)](https://conference.hitb.org/hitbsecconf2018ams/sessions/attacking-microsofts-net-framework-through-clr/)
				* In this talk, we first introduce managed execution environment and managed code under .NET Framework and discuss the security weaknesses of this code execution method . After that, we show a exploit for SQL Server through CLR and our automated tools for this exploitation. We will introduce a backdoor with administrator privilege based on CLR hijacking arbitrary .NET Applications.
			* [.NET Malware Threat: Internals and Reversing - Alexandre Borges(Defcon2019)](http://www.blackstormsecurity.com/docs/ALEXANDREBORGES_DEFCON_2019.pdf)
			* [Hijacking .NET to Defend PowerShell - Amanda Rosseau](https://arxiv.org/pdf/1709.07508.pdf)
				* Abstract—With the rise of attacks using PowerShell in the recent months, there has not been a comprehensive solution for monitoring or prevention. Microsoft recently released the AMSI solution for PowerShell v5, however this can also be bypassed. This paper focuses on repurposing various stealthy runtime .NET hijacking techniques implemented for PowerShell attacks for defensive monitoring of PowerShell. It begins with a brief introduction to .NET and PowerShell, followed by a deeper explanation of various attacker techniques, which is explained from the perspective of the defender, including assembly modification, class and method injection, compiler profiling, and C based function hooking. Of the four attacker techniques that are repurposed for defensive real-time monitoring of PowerShell execution, intermediate language binary modification, JIT hooking, and machine code manipulation provide the best results for stealthy run-time interfaces for PowerShell scripting analysis		
			* [How .NET executables are loaded - repnz(2019)](https://repnz.github.io/posts/dotnet-executable-load/)
			* [Common Language Runtime: Who? why? how? - Mez0](https://mez0.cc/posts/common-language-runtime-1/)
			* [Common Language Runtime 2: In memory execution - Mez0](https://mez0.cc/posts/common-language-runtime-2/)
		* **Managed vs Unmanaged code**
			* [What is "managed code"? - docs.ms](https://docs.microsoft.com/en-us/dotnet/standard/managed-code)
				* When working with .NET Framework, you will often encounter the term "managed code". This document will explain what this term means and additional information around it.
		* **Papers**
			* [Reflection’s Hidden Power: “Modifying Programs at Run-Time”](https://web.archive.org/web/20171208224139/http://www.digitalbodyguard.com/Papers/ReflectionsHiddenPower.pdf)
				* This paper will demonstrate using Reflection to take control over a DotNet (.Net)compiled code. The focus of this paper will be on how to use Reflection to navigate and gainaccess to values and functionality that would normally be off limits. This paper will be gearedfor any DotNet programmer (focus will be in C#). No special knowledge of Reflection isnecessary. The basic concept of Reflection and DotNet will be given, along with some lighttraining on using reflection. This paper is written for the DotNet v2.0 and v3.5 versions ofDotNet. Examples will be given on attacks, like forcing a program to change values and executefunctionality
			* [ASM in .NET: The old is new again - Jon McCoy(2015)](https://web.archive.org/web/20170829012346/http://www.digitalbodyguard.com/Papers/ASM%20in%20.NET-The%20old%20is%20new%20again.pdf)
				* This paper will cover running raw Machine Code(ASM) from within .NET. As we all know .NET runson IL(Intermediate Language) also known as “Managed byte code”. A program can declare an unsafesection of code and drop out from the managed area to run something like unmanaged C++ or the like.This paper will show how to run raw/unmanaged ASM in a normal safe C# application.
		* **Articles/Blogposts/Writeups**
			* [An Introduction to Writing .NET Executables for Pentesters](https://www.peew.pw/blog/2017/11/24/an-introduction-to-writing-net-executables-for-pentesters)
			* [Changeling - A Feature Morphing Creature - Adam Brown](https://coffeegist.com/security/changeling-a-feature-morphing-creature/)
				* The feature that we’ll be taking a look at today is Embedded Resources in C# projects. This is a feature that will allow us to compile code once, and reuse it on multiple assessments			
			* [How to Execute a Command in C# ? - Sandeep Aparajit(2008)](https://www.codeproject.com/Articles/25983/How-to-Execute-a-Command-in-C)
		* **Talks/Presentations/Videos**
			* [Quick Retooling in .Net for Red Teams - Dimitry Snezhkov(CircleCityCon2018](https://www.irongeek.com/i.php?page=videos/circlecitycon2018/circle-city-con-50-112-quick-retooling-in-net-for-red-teams-dimitry-snezhkov)
				* Quick Retooling in .Net for Red Teams PowerShell gave us a super-highway of convenient building blocks for offensive toolkits and operational automation. However, use of standalone .Net implants may be a desirable option in cases where PowerShell is heavily inspected and logged. While there are great toolkits to invoke unmanaged PowerShell or directly interface with .Net CLR - they are also statically compiled, and therefore easier identified by the defense. Red Teams are faced with specific challenges when they need to retool quickly in the field with .Net payloads. Can .Net toolkits accomplish their goals while maintaining flexibility, quick in-field retooling and operational security in the face of current detection mechanisms? We think so. This talk walks through some of the options present to the operators for .Net code compilation and presents ideas for extensibility of .Net tools at runtime, with the help of Dynamic Language Runtime (DLR). We will dive deeper into operational security lessons learned from dynamic code compilation. We will attempt to move beyond static nature of .Net assemblies into reflective DLR, achieving on-the-fly access to native Windows API. We will also discuss some methods of hiding sensitive aspects of execution in managed code memory. We will also touch on ways to help Defense fingerprint the attacks involving dynamic compilation of .Net assemblies, use of DLR and building blocks of offensive tooling involved in the process. A concept tool built on these ideas will be presented and released. It will be used as basis for our discussion.
			* [Building an Empire with (Iron)Python - Jim Shaver(Derbycon2018)](https://www.irongeek.com/i.php?page=videos/derbycon8/track-1-06-building-an-empire-with-ironpython-jim-shaver)
				* This talk discusses porting Python payloads to Windows using a little known, former Microsoft project. It explores offensive uses of .Net and how to reduce attack surface on .Net payloads.
			* [Staying # and Bringing Covert Injection Tradecraft to .NET - Ruben Boonen, The Wover(2020)](https://raw.githubusercontent.com/FuzzySecurity/BlueHatIL-2020/master/Ruben%20Boonen%20%26%20TheWover%20-%20BHIL2020_Staying%23_v0.4.pdf)
			* [.NET Core for Malware – Ryan Cobb (SO-CON 2020)](https://www.youtube.com/watch?v=woRfx5D2Y9Y&list=PLJK0fZNGiFU-2vFpjnt96j_VSuQVTkAnO&index=10)
				* .NET Core is the future of .NET. The Windows-only .NET Framework is on it's way out, and the cross-platform .NET Core is Microsoft's new flagship framework for building software. As red teamers, it's time to go back to the well of .NET as a host for implants and post-exploitation. In this talk, we will analyze the opportunities presented by the new .NET Core platform and practical examples to take advantage of them.
			* [Modern Red Team Weaponization - Mike Felch(WWHF Deadwood 2020)](https://www.youtube.com/watch?v=5W-Nlkh6nhg)
				* In an effort to seamlessly equip operators and reduce leaving breadcrumbs, this presentation will walk through methods for modern red team weaponization of offsec tooling. First we will step through the build process which will include automated builds, continuous integration/deployment, and C2 framework integration. Next, we will step through OPSEC considerations for payloads and tooling in an effort to reduce the breadcrumbs being left behind from assemblies. Finally, we will take a look at payload tradecraft for calling managed code (C# tooling) from unmanaged C++ (stub/launchers), low-level syscalls using C#, and code execution leveraging the Windows kernel.
			* [Getting Started in Covert .NET Tradecraft for Post-Exploitation – Kyle Avery(2021)](https://www.youtube.com/watch?v=g27DorVva3M)
				* This Black Hills Information Security (BHIS) webcast will cover OPSEC safe fork-n-run execution with Cobalt Strike, .NET log sources available to network defenders and security vendors, and obfuscation of public C# tools to evade EDR products consistently. If you're curious why penetration testers, red teamers, and even real threat actors prefer C# over PowerShell for post-exploitation, come find out how you can more effectively use these tools in secure environments.
			* [WWHF (Virtual): DOT NET Advanced Malware Development - Joff Thyer(2020)](https://www.youtube.com/watch?v=8lk6VhmlhoI&list=PLXF21PFPPXTPwX8mccVIQB5THhU_paWmN&index=29)
				* This talk will walk through how a penetration tester can use the C# language to develop a DOT NET assembly (DLL) designed to deliver shellcode into memory on a Windows system.  The talk will cover aspects of the necessary API calls into kernel32.dll, and describe how to build an MSBUILD XML file in order to evade whitelisting solutions.  Attendees of the talk should preferably have some familiarity with the C# programming language.  Techniques mentioned will include shellcode residing in the same thread, versus injecting into a remote process.
		* **General**
			* [SharpSploit](https://github.com/cobbr/SharpSploit)
				* SharpSploit is a .NET post-exploitation library written in C# that aims to highlight the attack surface of .NET and make the use of offensive .NET easier for red teamers.
			* [SharpUtils](https://github.com/IllidanS4/SharpUtils)
			* [GhostPack](https://github.com/GhostPack)
			* [Sharp-Suite](https://github.com/FuzzySecurity/Sharp-Suite)
				* FuzzySecurity: 'My musings with C#'
			* [OffensiveCSharp-matterpreter](https://github.com/matterpreter/OffensiveCSharp)
				* This is a collection of C# tooling and POCs I've created for use on operations. Each project is designed to use no external libraries. Open each project's .SLN in Visual Studio and compile as "Release".
			* [bytecode-api](https://github.com/bytecode77/bytecode-api)
				* C# library with common classes, extensions and additional features in addition to the .NET Framework. BytecodeApi implements lots of extensions and classes for general purpose use. In addition, specific classes implement more complex logic for both general app development as well as for WPF apps. Especially, boilerplate code that is known to be part of any Core DLL in a C# project is likely to be already here. In fact, I use this library in many of my own projects. For this reason, each class and method has been reviewed numerous times. BytecodeApi is highly consistent, particularly in terms of structure, naming conventions, patterns, etc. The entire code style resembles the patterns used in the .NET Framework itself. You will find it intuitive to understand.
			* [OutlookToolbox](https://github.com/ThunderGunExpress/OutlookToolbox)
				* OutlookToolbox is a C# DLL that uses COM to do stuff with Outlook. Also included is a Cobalt Strike aggressor script that uses Outlooktoolbox.dll to give it a graphical and control interface.
				* [Blogpost](https://ijustwannared.team/2017/10/28/outlooktoolbox/)
			* [OffensiveDLR](https://github.com/byt3bl33d3r/OffensiveDLR)
				* Toolbox containing research notes & PoC code for weaponizing .NET's DLR
			* [RedTeamCSharpScripts -  Mr-Un1k0d3r](https://github.com/Mr-Un1k0d3r/RedTeamCSharpScripts)
			* [CSharpScripts - Arno0x](https://github.com/Arno0x/CSharpScripts)
			* [StandIn](https://github.com/xforcered/StandIn)
				* "StandIn is a small .NET35/45 AD post-exploitation toolkit"
			* [awesome-dotnet](https://github.com/quozd/awesome-dotnet#database)
			* [Homework of C-Sharp](https://github.com/3gstudent/Homework-of-C-Sharp)
			* [csharptoolbox](https://gitlab.com/KevinJClark/csharptoolbox)
		* **AD**
			* [SharpSystemTriggers](https://github.com/cube0x0/SharpSystemTriggers)
				* Collection of remote authentication triggers coded in C# using MIDL compiler for avoiding 3rd party dependencies.
		- **Assembly Inline**
			- **101**
			- **Articles/Blogposts/Writeups**
				* [Inline Assembler - docs.ms](https://docs.microsoft.com/en-us/cpp/assembler/inline/inline-assembler?view=msvc-170)
					* "You can use the inline assembler to embed assembly-language instructions directly in your C and C++ source programs without extra assembly and link steps. The inline assembler is built into the compiler, so you don't need a separate assembler such as the Microsoft Macro Assembler (MASM). Inline assembly is not supported on the ARM and x64 processors."
				* [Inline Assembly in C# and .NET - Trojaner(2019)](https://web.archive.org/web/20210331194757/https://esozbek.me/inline-assembly-in-csharp-and-dotnet/)
					* [Code](https://github.com/Trojaner/csharp-inline-assembly)
			- **Tools**
				* [Fasm.NET](https://github.com/JamesMenetrey/Fasm.NET)
					* "A managed wrapper to use FASM compiler from .NET applications. This library is written in C++/CLI and embeds FASM compiler as a linkable Microsoft COFF object. As FASM compiler is built in 32-bit, the managed assembly can only be used within a 32-bit development."
		- **Assembly Merge**
			* [Merging C# Assemblies using dnMerge - ethicalchaos.dev(2021)](https://ethicalchaos.dev/2021/07/04/merging-c-assemblies-using-dnmerge/)
			* [dnMerge](https://github.com/CCob/dnMerge)
				* dnMerge is an MSBuild plugin that will merge multiple .NET reference assemblies into a single .NET executable or DLL. dnMerge can be included within your .NET project using the NuGet package available from the central repo.  Merged assembiles are compressed with 7-Zip's LZMA SDK which has the added benefit of smaller executables in comparison with other .NET assembly mergers. No additional .NET references are including during merging, making dnMerge suitable for cross-compiling on Linux without pulling in .NET Core assembly references into the final merged assembly.
		* **Backdooring Binaries**
			* [Backdoor .NET assemblies with… dnSpy 🤔 - Rasta Mouse(2021)](https://rastamouse.me/backdoor-net-assemblies-with-dnspy-%f0%9f%a4%94/)
		* **Browsers**
			* [Canary](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/Canary)
				* Canary is a small DIY extension to SharpChrome. It lets you pull browser history for Chrome or the new Chromium Edge. Results are orderd by visit_count and you can pull all data or use the "-l" flag to pull only the last X days. Most of the boilerplate is ripped out of SharpChrome and can be added there easily if someone wants to make a PR for that.
			* [SharpWeb](https://github.com/djhohnstein/SharpWeb)
				* SharpWeb is a .NET 2.0 CLR compliant project that can retrieve saved logins from Google Chrome, Firefox, Internet Explorer and Microsoft Edge. In the future, this project will be expanded upon to retrieve Cookies and History items from these browsers.
		* **Collection**
			* [1Password Secret Retrieval — Methodology and Implementation - Dwight Hohnstein(2021)](https://posts.specterops.io/1password-secret-retrieval-methodology-and-implementation-6a9db3f3c709)
	    	* [WireTap](https://github.com/djhohnstein/WireTap)
				* .NET 4.0 Project to interact with video, audio and keyboard hardware.
			* [SharpLogger](https://github.com/djhohnstein/SharpLogger)
				* Keylogger written in C#
			* [SharpLeftOvers](https://github.com/ceramicskate0/SharpLeftOvers)
			* [Xst Reader](https://github.com/Dijji/XstReader)
				* Xst Reader goes beyond Outlook in that it will allow you to open .ost files, which are the caches created by Outlook to hold a local copy of a mailbox. Wanting to read an .ost file as the original motivation for this project: now it also as the ability to export the header and body of an email in its native format (plain text, HTML, or rich text), and inspect and export all the properties of an email.
		* **COM**
			* [COM Interop](https://github.com/AaronRobinsonMSFT/COMInterop)
				* This project is an example on how to manually consume a COM server from C# or a C# server from COM client. It also contains projects for less common scenarios involving .NET and COM.			
		* **Credentials**
			* [SharpHandler](https://github.com/jfmaes/SharpHandler)
				* This project reuses open handles to lsass to parse or minidump lsass, therefore you don't need to use your own lsass handle to interact with it.
			* [SharpLoginPrompt](https://github.com/shantanu561993/SharpLoginPrompt)
				* This Program creates a login prompt to gather username and password of the current user. This project allows red team to phish username and password of the current user without touching lsass and having adminitrator credentials on the system.
			* [ICU](https://github.com/WingsOfDoom/ICU)
				* Cred Prompt Phishing
			* [CloneVault](https://github.com/mdsecactivebreach/CloneVault)
				* CloneVault allows a red team operator to export and import entries including attributes from Windows Credential Manager. This allows for more complex stored credentials to be exfiltrated and used on an operator system. It is aimed at making it possible to port credentials that store credential material in binary blobs or those applications that store data in custom attributes. There are many use cases, please see our demonstration of cloning access to Microsoft OneDrive on the [MDSec Blog](https://www.mdsec.co.uk/knowledge-centre/insights/)
			* [WinBoost](https://github.com/mobdk/WinBoost)
			* **Clipboard**
				* [SharpClipboard](https://github.com/slyd0g/SharpClipboard)
					* C# Clipboard Monitor
					* [Blogpost](https://grumpy-sec.blogspot.com/2018/12/i-csharp-your-clipboard-contents.html)
				* [SharpClipHistory](https://github.com/FSecureLABS/SharpClipHistory)
					* SharpClipHistory is a .NET application written in C# that can be used to read the contents of a user's clipboard history in Windows 10 starting from the 1809 Build.
			* **DPAPI**
				* [DonPAPI ](https://github.com/login-securite/DonPAPI)
					* Dumping DPAPI credz remotely
			* **Hooking**
				* [SharpHook](https://github.com/IlanKalendarov/SharpHook)
					* SharpHook is inspired by the SharpRDPThief project, It uses various API hooks in order to give us the desired credentials. In the background it uses the EasyHook project, Once the desired process is up and running SharpHook will automatically inject its dependencies into the target process and then, It will send us the credentials through EasyHook's IPC server.
			- **NTLM-Relay**
			- **Password Spraying**
				* [SharpSMBSpray](https://github.com/rvrsh3ll/SharpSMBSpray)
					* Spray a hash via smb to check for local administrator access
			- **Process Memory**
					* [Writing Minidumps in C# - docs.ms](https://docs.microsoft.com/en-us/archive/blogs/dondu/writing-minidumps-in-c)
					* [Dumping Process Memory with Custom C# Code - 3xplo1tcod3r](https://3xpl01tc0d3r.blogspot.com/2019/07/dumping-process-memory-with-custom-c-sharp.html)
					* [SharpDump](https://github.com/GhostPack/SharpDump)
						* SharpDump is a C# port of PowerSploit's Out-Minidump.ps1 functionality.
					* [ATPMiniDump](https://github.com/b4rtik/ATPMiniDump)
						* Dumping LSASS memory with MiniDumpWriteDump on PssCaptureSnapShot to evade WinDefender ATP credential-theft.
						* [Blogpost](https://www.matteomalvica.com/blog/2019/12/02/win-defender-atp-cred-bypass/)
					* [SafetyKatz](https://github.com/GhostPack/SafetyKatz)
						* SafetyKatz is a combination of slightly modified version of @gentilkiwi's Mimikatz project and @subtee's .NET PE Loader.
					* [KittyLitter](https://github.com/djhohnstein/KittyLitter)
						* This project was made for an upcoming event. It is comprised of two components, KittyLitter.exe and KittyScooper.exe. This will bind across TCP, SMB, and MailSlot channels to communicate credential material to lowest privilege attackers.
				- **RDP**
					* [RemoteViewing](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/RemoteViewing)
						* RemoteViewing, is quick POC to demo RDP credential theft through API hooking using EasyHook for .Net payloads combined with Costura to pack resources into a single module. 
		- **Cryptographic Operations**
			- **Collections**
			- **Encryption**
			- **Hashing**
		- **D/Invoke**
			* [DInvoke](https://github.com/TheWover/DInvoke)
				* Dynamically invoke arbitrary unmanaged code from managed code without PInvoke.
			* [Primer to DInvokes Injection API and a tale of token duplication and command-line spoofing on the cheap - Jean Maes(2021)](https://redteamer.tips/primer-to-dinvokes-injection-api-and-a-tale-of-token-duplication-and-command-line-spoofing-on-the-cheap/)
				* [DinvokeDupetokenAndThreadSwitcheroo](https://github.com/redteamertips/DinvokeDupetokenAndThreadSwitcheroo)
			* [D/Invokify PPID Spoofy & BlockDLLs - Rasta Mouse(2020)](https://offensivedefence.co.uk/posts/ppidspoof-blockdlls-dinvoke/)
			* [Process Injection using DInvoke - Rasta Mouse](https://web.archive.org/web/20210601171512/https://rastamouse.me/blog/process-injection-dinvoke/)
			* [Syscalls with D/Invoke - RastaMouse2021](https://offensivedefence.co.uk/posts/dinvoke-syscalls/)
			* [Primer to DInvokes Injection API and a tale of token duplication and command-line spoofing on the cheap - Jean Maes(2021)](https://redteamer.tips/primer-to-dinvokes-injection-api-and-a-tale-of-token-duplication-and-command-line-spoofing-on-the-cheap/)
				* [DinvokeDupetokenAndThreadSwitcheroo](https://github.com/redteamertips/DinvokeDupetokenAndThreadSwitcheroo)
			* [DInjector](https://github.com/snovvcrash/DInjector)
				* Collection of shellcode injection techniques packed in a D/Invoke weaponized DLL
			* [DInvokeProcessHollowing](https://github.com/passthehashbrowns/DInvokeProcessHollowing)
			* [BetterSafetyKatz](https://github.com/Flangvik/BetterSafetyKatz)
				*  Fork of SafetyKatz that dynamically fetches the latest pre-compiled release of Mimikatz directly from gentilkiwi GitHub repo, runtime patches signatures and uses SharpSploit DInvoke to PE-Load into memory.
			* [NoAmci](https://github.com/med0x2e/NoAmci)
				* A PoC for using DInvoke to patch AMSI.dll in order to bypass AMSI detections triggered when loading .NET tradecraft via Assembly.Load(). .Net tradecraft can be compressed, encoded (encrypted if required) in order to keep the assembly size less than 1MB, then embedded as a resource to be loaded after patching amsi.dll memory.
		* **Discovery (Local)**
			* [SharpDirLister](https://github.com/EncodeGroup/SharpDirLister)
				* A .NET 4.0 application that uses an optimized file search algorithm that will output a full directory / file listing of a drive in a matter of seconds and at the end it will compress it to a .gz
			* [SharpProcEnum](https://github.com/antman1p/SharpProcEnum)
				* .NET tool for enumeration processes and dumping memory.
			* [SharpSearch](https://github.com/djhohnstein/SharpSearch)
				* Search files for extensions as well as text within.
			* [EventLog Searcher - benpturner(2021)](https://redteaming.co.uk/2021/03/15/eventlog-searcher/)
			* [GetNetworkInterfaces](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/GetNetworkInterfaces)
				* "GetNetworkInterfaces is a small .Net45 utility to pull local network adapter information. It mostly has feature parity with "ipconfig /all" and can be useful for some fast enumeration."
			* [SharpMapModules](https://github.com/cube0x0/SharpMapModules)
				* C# modules made for easy recon with SharpMapExec execute assembly function
			* [SharpEDRChecker](https://github.com/PwnDexter/SharpEDRChecker)
				* Checks running processes, process metadata, Dlls loaded into your current process and the each DLLs metadata, common install directories, installed services and each service binaries metadata, installed drivers and each drivers metadata, all for the presence of known defensive products such as AV's, EDR's and logging tools.
			* [CheckSafeBoot](https://github.com/fashionproof/CheckSafeBoot)
				* "I used this to see if an EDR is running in Safe Mode"
		* **Discovery (Network)**
			* [SharpStrike](https://github.com/iomoath/SharpStrike)
				* SharpStrike is a post-exploitation tool written in C# that uses either CIM or WMI to query remote systems. It can use provided credentials or the current user's session.
			* [SharpShares](https://github.com/mez-0/SharpShares)
				* The goal of SharpShares is to be able to parse different input types and run across a network(s) to find SMB services, authenticate, and pull the ACLs for each share.
		* **Dissasembly**
			* [Dis2Msil](https://github.com/Rhotav/Dis2Msil)
				* Disassemble bytecodes as MSIL
		* **DLLs**
			* [Unmanaged Exports - Robert Giesecke(2009)](https://sites.google.com/site/robertgiesecke/Home/uploads/unmanagedexports)
			* [Is is possible to export functions from a C# DLL like in VS C++? - Stackoverflow](https://stackoverflow.com/questions/4818850/is-is-possible-to-export-functions-from-a-c-sharp-dll-like-in-vs-c)		
			* [DllExport](https://github.com/3F/DllExport)
			* [Lunar](https://github.com/Dewera/Lunar)
				* A lightweight native DLL mapping library that supports mapping directly from memory
		* **Embedding**
			* [Resource-Reflector](https://github.com/Latency/Resource-Reflector)
				* A .NET application written in C# for viewing and extracting assembly resources.
		* **Evasion**
			* **Articles**
				* [Module Stomping in C# - RastaMouse(2020)](https://offensivedefence.co.uk/posts/module-stomping/)
				* [Ordinal Values, Windows Functions, and C# - FortyNorthSecurity(2021)](https://fortynorthsecurity.com/blog/ordinal-values-and-c/)
				* [Detection evasion in CLR and tips on how to detect such attacks - Alexander Rodchenko(2021)](https://securelist.com/detection-evasion-in-clr-and-tips-on-how-to-detect-such-attacks/104226/)
				* [Using a C# Shellcode Runner and ConfuserEx to Bypass UAC - Hausec(2020)](https://hausec.com/2020/10/30/using-a-c-shellcode-runner-and-confuserex-to-bypass-uac-while-evading-av/)
			* **Tools**
				* [amsi-tracer](https://github.com/manyfacedllama/amsi-tracer)
					* Leverage AMSI (Antimalware Scan Interface) technology to aid your analysis. This tool saves all buffers (scripts, .NET assemblies, etc) passed into AMSI during dynamic execution.
				* [SharpSelfDelete](https://github.com/klezVirus/SharpSelfDelete)
				* [SharpNukeEventLog](https://github.com/jfmaes/SharpNukeEventLog)	
					* nuke that event log using some epic dinvoke fu
				* [SyscallAmsiScanBufferBypass](https://github.com/S3cur3Th1sSh1t/SyscallAmsiScanBufferBypass)
					* AmsiScanBuffer Patch using D/Invoke.
				* [SwampThing](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/SwampThing)
					* "SwampThing lets you to spoof process command line args (x32/64). Essentially you create a process in a suspended state, rewrite the PEB, resume and finally revert the PEB. The end result is that logging infrastructure will record the fake command line args instead of the real ones."
				* [MaceTrap](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/MaceTrap)
					* MaceTrap is a proof-of-concept for time stomping using SetFileTime. MaceTrap allows you to set the CreationTime / LastAccessTime / LastWriteTime for arbitrary files and folders. 
				* [SharpLoadImage](https://github.com/b4rtik/SharpLoadImage)
					* Hide .Net assembly into png images
				* [BlockETW](https://github.com/Soledge/BlockEtw)
					* .Net Assembly to block ETW telemetry in current process
			- **AMSI**
				* [Bypass In-memory Integrity Checking - Rasta Mouse(2021)](https://rastamouse.me/bypass-in-memory-integrity-checking/)
			- **Log Evasion/Modification**
				- **CLR-Specific Logging**
					- **Articles/Blogposts/Writeups**
						* [Investigating .NET CLR Usage Log Tampering Techniques For EDR Evasion - BOHOPS(2021)](https://bohops.com/2021/03/16/investigating-net-clr-usage-log-tampering-techniques-for-edr-evasion/)
				- **ETW**
				- **EVTx**
			- **Timestomping**
				* [SharpStomp](https://github.com/kafkaesqu3/SharpStomp)
					* Timestomping module: overwrite file create/modify times in .NET (no pinvoke)
		* **Execution**
			* **Articles**
				* [Callback Function Techniques & Native Code Execution - DamonMohammadbagher(2021)](https://damonmohammadbagher.github.io/Posts/24_1mar2021x.html)
				* [Call/Invoke Async C# Method via Callback Function APIs - DamonMohammadbagher(2021)](https://damonmohammadbagher.github.io/Posts/29mar2021x.html)
				* [Remote Thread Injection + C# Async Method + CallBack Functions Technique (Changing Code Behavior) - DamonMohammadbagher(2021)](https://damonmohammadbagher.github.io/Posts/05may2021x.html)
				* [In Process Execute Assembly and Mail Slots - N4kedTurtle(2020)](https://teamhydra.blog/2020/10/12/in-process-execute-assembly-and-mail-slots/)
			- **DInvoke**
				* [Defeating EDR's using D/Invoke - Jean-Francois Maes(2021)](https://www.youtube.com/watch?v=d_Z_WV9fp9Q)
					* How can red team operators emulate covert operations and operate at the same level as a real threat group? EDR solutions can make the life of a red team operator significantly harder. Dynamic invocation (also known as D/Invoke) – a sub branch of the popular “Sharpsploit” project, can help with evading those pesky EDR’s and execute your payloads successfully. In this presentation, we will go over D/Invokes capabilities and how to leverage them in your red team operations.
				* [DInvoke Wiki](https://dinvoke.net/)
				* [DInvoke - RastaMouse Fork](https://github.com/rasta-mouse/DInvoke)
					* The aim of this project is to provide D/Invoke in a more minimalist form. It only contains the core DynamicInvoke and ManualMap functionality, without all the additional helper methods and delegates. This help keeps the packages small and lowers the detection surface for AV. The dinvoke.net Wiki contains a library of useful delegates that you can add to your projects.
			- **Fork-n-Run**
				* [Fork-n-Run](https://github.com/rasta-mouse/Fork-n-Run)
					* Experimenting with reusable components for fork n' run operations.
			- **Syscalls**
				- **Articles/Blogposts/Writeups**
					* [Red Team Tactics: Utilizing Syscalls in C# - Prerequisite Knowledge - Jack Halon(2020)](https://jhalon.github.io/utilizing-syscalls-in-csharp-1/)
					* [Using Syscalls to Inject Shellcode on Windows - SolomonSklaskh(2020)](https://www.solomonsklash.io/syscalls-for-shellcode-injection.html)
				- **Tools**
					* [SharpSploit](https://github.com/cobbr/SharpSploit)
						* SharpSploit is a .NET post-exploitation library written in C#
					* [Syscall-Example](https://github.com/exploitblizzard/Syscall-Example)
						* "Using syscall to load shellcode, Evasion techniques"
					* [SyscallsExample](https://github.com/m0rv4i/SyscallsExample)
						* Simple project using syscalls (via SysWhispers2) to execute MessageBox shellcode in a target process.
			- **Tools**
				* [RunDotNetDll](https://github.com/enkomio/RunDotNetDll)
					* RunDotNetDll allows to introspect a given .NET Assembly in order to list all the methods which are implemented in the Assembly and to invoke them. All this is done via pure Reflection using dnlib library.
				* [Lunar](https://github.com/Dewera/Lunar)
					* A lightweight native DLL mapping library that supports mapping directly from memory
				* [NativePayload_TiACBT](https://github.com/DamonMohammadbagher/NativePayload_TiACBT)
					* NativePayload_TiACBT (Remote Thread Injection + C# Async Method + CallBack Functions Technique)
		* **Exfiltration**
			* [SharpExfiltrate](https://github.com/Flangvik/SharpExfiltrate)
				* SharpExfiltrate is a tiny but modular C# framework to exfiltrate loot over secure and trusted channels. It supports both single-files and full-directory paths (recursively), file extension filtering, and file size filtering. Exfiltrated data will be compressed and encrypted before being uploaded. While exfiltrating a large amount of data will require the output stream to be cached on disk, smaller exfiltration operations can be done all in memory with the "memoryonly" option.
			* [SharpBox](https://github.com/P1CKLES/SharpBox)
		* **Firewall**
			* [FireEater](https://github.com/jamcut/FireEater)
				* FireEater allows a user to interact with the Windows firewall through .NET APIs. Requires Admin privs.
			* [WindowsFirewallHelper](https://github.com/falahati/WindowsFirewallHelper)
				* A class library to manage the Windows Firewall as well as adding your program to the Windows Firewall Exception list.
			* [sharpbysentinel](https://github.com/jfmaes/sharpbysentinel)
			* [SharpFirewall](https://github.com/latortuga71/SharpFirewall)
				* Add or delete firewall rules. With C#
		- **GUI/TUIs**
			- **GUI**
			- **TUI**
				* [Sharprompt](https://github.com/shibayan/Sharprompt)
					* Interactive command-line based application framework for C#
		- **Hooking**
			- **Articles/Blogposts/Writeups**
				* [EDR Evasion: Unhooking DLL's With C# - MakoSec(2021)](https://makosecblog.com/malware-dev/dll-unhooking-csharp/)
			- **Tools**
				
				* [HookLib](https://github.com/arsium/HookLib)
				* [HookDetection_Csharp](https://github.com/Kara-4search/HookDetection_CSharp)
				* [Dendrobate](https://github.com/xforcered/Dendrobate)
					* Managed code hooking template.
				* [SharpUnhooker](https://github.com/GetRektBoy724/SharpUnhooker)
					* C# Based Universal API Unhooker - Automatically Unhook API Hives (ntdll.dll, kernel32.dll, advapi32.dll, and kernelbase.dll). SharpUnhooker helps you to evades user-land monitoring done by AVs and/or EDRs by cleansing/refreshing API DLLs that loaded on the process (Offensive Side) or remove API hooks from user-land rootkit (Defensive Side). There is 3 technique of user-land API hooking that i know, Inline/hot-patch hooking, IAT hooking, and EAT hooking. For now, SharpUnhooker only unhooks inline/hot-patch hooks and EAT hooks. 
				* [AtomicBird](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/AtomicBird)
					* "AtmoicBird, is a crude POC to demo the use of EasyHook in .Net payloads combined with Costura to pack resources into a single module. AtomicBird has two functions, (1) Hook MessageBoxA => print to console / modify parameters => unhook and (2) Hook NtQuerySystemInformation->SystemProcessInformation, search the linked list of SYSTEM_PROCESS_INFORMATION Structs to find powershell processes and unlink them. The second function requires that you inject the .Net PE into a process that uses NtQuerySystemInformation (Process Explorer was used for testing), you can do that with execute-assembly or with donut by generating shellcode. AtmoicBird was only tested on x64 Win10."
				* [Dendrobate](https://github.com/xforcered/Dendrobate)
					* Managed code hooking template.
				* [MinHook.NET](https://github.com/CCob/MinHook.NET)
					* MinHook.NET is a pure managed C# port of the brilliant MinHook library by Tsuda Kageyu (https://github.com/TsudaKageyu/minhook). The library has the capability of inline hooking native API calls, utilising .NET delegates for both the detoured and original function that is commonly called with the detour.
		- **Injection**
			- **Info**
				* [.NET Internals and Code Injection](https://ntcore.com/files/netint_injection.htm)
					* This article is the obvious culmination of the previous effort of writing the Rebel.NET application and the first of a two series of articles about the .NET framework internals and the protections available for .NET assemblies. The next article will be about .NET native compiling. As the JIT inner workings haven't been analyzed yet, .NET protections are quite naļf nowadays. This situation will rapidly change as soon as the reverse engineering community will focus its attention on this technology. These two articles are aimed to raise the consiousness about the current state of .NET protections and what is possible to achieve but hasn't been done yet. In particular, the current article about .NET code injection represents, let's say, the present, whereas the next one about .NET native compiling represents the future. What I'm presenting in these two articles is new at the time I'm writing it, but I expect it to become obsolete in less than a year. Of course, this is obvious as I'm moving the first steps out from current .NET protections in the direction of better ones. But this article isn't really about protections: exploring the .NET framework internals can be useful for many purposes. So, talking about protections is just a means to an end.		
					* [Process Injection using DInvoke - RastaMouse](https://rastamouse.me/blog/process-injection-dinvoke/)
			* **Articles/Blogposts/Writeups**
				* [Shellcode Execution in .NET using MSIL-based JIT Overwrite - Matt Graeber(2013)](http://www.exploit-monday.com/2013/04/MSILbasedShellcodeExec.html)
				* [Module Stomping in C# - Rastamouse(2020)](https://offensivedefence.co.uk/posts/module-stomping/)
				* [Process Injection using DInvoke - Rastamouse(2020)](https://web.archive.org/web/20210601171512/https://rastamouse.me/blog/process-injection-dinvoke/)
				* [NET-Assembly-Inject-Remote](https://github.com/med0x2e/NET-Assembly-Inject-Remote)
					* PoC demonstrating some methods for .NET assembly local/remote loading/injection into memory using System.AppDomain.ExecuteAssembly() and System.Reflection.Assembly.LoadFrom() method (check "NetAssembly-Injection/AssemblyLoader.cs" methods documentation).
				* [RuralBishop](https://github.com/rasta-mouse/RuralBishop)
					* RuralBishop is practically a carbon copy of UrbanBishop by b33f, but all P/Invoke calls have been replaced with D/Invoke. This creates a local RW section in RuralBishop and then maps that section as RX into a remote process. Once the shared section has been established the shellcode is written to the local section which then automatically propagates to the remote process. For execution RuralBishop creates a remote suspended thread (start address is set to ntdll!RtlExitUserThread) and queues an APC on that thread. Once resumed with NtAlertResumeThread, the shellcode executes and the thread exits gracefully on completion.
				* [The Curious Case of QueueUserAPC - Dwight Hohnstein(2019)](https://posts.specterops.io/the-curious-case-of-queueuserapc-3f62e966d2cb)
				* [Staying # & Bringing Covert Injection Tradecraft to .NET - The Wover & Ruben Boonen(BlueHat IL 2020)](https://www.youtube.com/watch?v=FuxpMXTgV9s)
					* [Slides](https://raw.githubusercontent.com/FuzzySecurity/BlueHatIL-2020/master/Ruben%20Boonen%20%26%20TheWover%20-%20BHIL2020_Staying%23_v0.4.pdf)
					* [Code](https://github.com/FuzzySecurity/BlueHatIL-2020)
					* In our talk we will focus on explaining the fundamental tradecraft behind these new developments, the challenges and requirements associated with them, and how they can be adapted to suit your needs. Additionally, we will discuss how SharpSploit can be combined with other open-source projects to be integrated into a red team's tooling. As much as possible, we will also discuss how to counter and detect the techniques that we have developed. Finally, we will explain the community-focused development of these projects and how you too can contribute to advance open-source .NET tradecraft.
			- **Performing**
				* [DLL Injection via a Custom .NET Garbage Collector - @spotheplanet](https://ired.team/offensive-security/code-injection-process-injection/injecting-dll-via-custom-.net-garbage-collector-environment-variable-complus_gcname)
				* [Injecting .NET Assembly to an Unmanaged Process - @spotheplanet](https://www.ired.team/offensive-security/code-injection-process-injection/injecting-and-executing-.net-assemblies-to-unmanaged-process)
			- **PoCs** - Sort into proper categories of each
				* [Donut](https://github.com/TheWover/donut)
					* Generates x86, x64, or AMD64+x86 position-independent shellcode that loads .NET Assemblies, PE files, and other Windows payloads from memory and runs them with parameters 
				* [donutCS](https://github.com/n1xbyte/donutCS)
					* .NET Core version of donut shellcode generator.
				* [C# Memory Injection Examples](https://github.com/pwndizzle/c-sharp-memory-injection)
					* A set of scripts that demonstrate how to perform memory injection.
				* [Execute assembly via Meterpreter session](https://github.com/b4rtik/metasploit-execute-assembly)
					* Custom Metasploit post module to executing a .NET Assembly from Meterpreter session 
				* [TikiTorch](https://github.com/rasta-mouse/TikiTorch)
					* TikiTorch was named in homage to CACTUSTORCH by Vincent Yiu. The basic concept of CACTUSTORCH is that it spawns a new process, allocates a region of memory, then uses CreateRemoteThread to run the desired shellcode within that target process. Both the process and shellcode are specified by the user.
					* [TikiTorch - Rastamouse](https://rastamouse.me/blog/tikitorch/)
					* [TikiVader - Rastamouse](https://rastamouse.me/blog/tikivader/)
					* [The Return of Aggressor - Rastamouse](https://rastamouse.me/blog/tikigressor/)
					* [TikiService - Rastamouse](https://rastamouse.me/blog/tikiservice/)
					* [Lighting the path through EDRs using TikiTorch - RhythmStick(2019)](https://www.rythmstick.net/posts/tikitorch/)
				* [Managed Injector](https://github.com/enkomio/ManagedInjector)
					* This project implements a .NET Assembly injection library (it is inspired by the snoopwpf project). The remote process can be a managed or unmanaged one.
				* [MemorySharp](https://github.com/ZenLulz/MemorySharp)
					* MemorySharp is a C# based memory editing library targeting Windows applications, offering various functions to extract and inject data and codes into remote processes to allow interoperability.
				* [ManagedInjection](https://github.com/malcomvetter/ManagedInjection)
					* A proof of concept for dynamically loading .net assemblies at runtime with only a minimal convention pre-knowledge
				* [SharpNeedle](https://github.com/ChadSki/SharpNeedle)
					* A project for properly injecting C# dlls into other processes.
				* [ManagedInjection](https://github.com/malcomvetter/ManagedInjection)
					* A proof of concept for injecting a pre-compiled .net assembly in memory at runtime with zero pre-knowledge of its assembly namespace or type. All that is necessary is a convention for the initial method name which will be instantiated, or just have the assembly initialize via its Constructor for a true "zero knowledge" scenario.
				* [Remote AppDomainManager Injection - byt3bl33d3r](https://gist.github.com/byt3bl33d3r/de10408a2ac9e9ae6f76ffbe565456c3)
				* [DotNetDebug](https://github.com/xpn/DotNetDebug)
				* [DNCI - Dot Net Code Injector](https://github.com/guibacellar/DNCI)
					* DNCI allows the injection of .Net code (.exe or .dll) remotely in unmanaged processes in windows.	
				* [UrbanBishopLocal](https://github.com/slyd0g/UrbanBishopLocal)
					*  A port of FuzzySecurity's UrbanBishop project for inline shellcode execution 
				* [ProcessInjection](https://github.com/3xpl01tc0d3r/ProcessInjection)
					* The program is designed to perform process injection. Currently the tool supports 4 process injection techniques.
				* [clrinject](https://github.com/jonatan1024/clrinject)
					* Injects C# EXE or DLL Assembly into any CLR runtime and AppDomain of another process. The injected assembly can then access static instances of the injectee process's classes and therefore affect it's internal state.
				* [native-dotnet-code-injection](https://github.com/sunsided/native-dotnet-code-injection)
					* Injects a native bootstrap DLL into the target process by calling LoadLibrary as a remote thread and then calls the initialization method of the .NET runtime (hosting API). After that, a .NET assembly is loaded into the default application domain and executed.
				* [SharpNeedle](https://github.com/ChadSki/SharpNeedle)
					* A project for properly injecting C# dlls into other processes.(...but also walking the export address table and calling a method on your dll.)
				* [GhostLoader](https://github.com/TheWover/GhostLoader)
					* GhostLoader - AppDomainManager - Injection - 攻壳机动队
				* [Malwaria](https://github.com/nicholasmckinney/Malwaria)
				* [C# Memory Injection Examples](https://github.com/pwndizzle/c-sharp-memory-injection)
					* A set of scripts that demonstrate how to perform memory injection.
				* [MappingInjection_CSharp](https://github.com/Kara-4search/MappingInjection_CSharp)
				* [DesertNut](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/DesertNut)
					* DesertNut is a proof-of-concept for code injection using subclassed window callbacks (more commonly known as PROPagate).
				* [WindfarmDynamite](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/WindfarmDynamite)
					* WindfarmDynamite is a proof-of-concept for code injection using the Windows Notification Facility (WNF).
				* [UrbanBishop](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/UrbanBishop)
					* This POC creates a local RW section in UrbanBishop and then maps that section as RX into a remote process. Once the shared section has been established the shellcode is written to the local section which then automatically propagates to the remote process. For execution UrbanBishop creates a remote suspended thread (start address is set to ntdll!RtlExitUserThread) and queues and APC on that thread, once resumed with NtAlertResumeThread the shellcode executes and the thread exits gracefully on completion.
		- **Language Embeds**
			- **Python**
				* [Pyjion](https://github.com/tonybaloney/Pyjion)
					* Pyjion, a JIT extension for CPython that compiles your Python code into native CIL and executes it using the .NET CLR.
			- **Tools**
				* [Zolom](https://github.com/checkymander/Zolom)
    				* C# Executable with embedded Python that can be used reflectively to run python code on systems without Python installed
		- **Lateral Movement**
			- **SMB**
			- **SSH**
				* [SSHClient](https://github.com/skahwah/SSHClient)
			- **WinRM**
		- **LNKs**
			- **Tools**
				* [ShellLink](https://github.com/securifybv/ShellLink)
					* A .NET Class Library for processing ShellLink (LNK) files as documented in MS-SHLLINK. It allows for reading, creating and modifying ShellLink (LNK) files.
		- **Loaders/Stage0_or_1**
			- **Articles/Blogposts/Writeups**
				* [Welcome to the From zero to hero: creating a reflective loader in C#  workshop! - Jean Maes(2021)](https://jfmaes-1.gitbook.io/reflection-workshop/lab-0-setup)
					* [Video Presentation](https://www.youtube.com/watch?v=E6LOQQiNjj0)
			- **Talks/Presentations/Videos**
				* [Writing custom backdoor payloads using C# - Mauricio Velazco, Olindo Verrillo(Defcon27)](https://github.com/mvelazc0/defcon27_csharp_workshop)
				* [Reflective C# Assembly loading && Reflective PE-Injection - S3cur3Th1sSh1t(2021)](https://www.youtube.com/watch?v=oe11Q-3Akuk)
					* "In this stream I went through the process of C# source code modification, and reflective loading of C# Assemblies from Powershell. Afterwards, two public reflective PE-Loaders and the use-case with examples were shown. In the very end unhooking + ETW patching was added to our Syscall PE-Loader."
				* [Malware development workshop.](https://github.com/chr0n1k/AH2021Workshop)
					* Welcome to the Malware Development workshop for AfricaHackon 2021. In this interactive workshop, we will take a look at the C# language and how to write malware focused on droppers/loaders that will run shellcode on Windows 10 targets that give a meterpreter session back.
			- **Tools**
				* [MonkeyWorks](https://github.com/NetSPI/MonkeyWorks)
					* A C# library to facilitate the development of offensive tools against Windows systems.
			- **Samples/PoCs**
				* [DarkAgent](https://github.com/hackersql/DarkAgent)
				* [SharpMemshell](https://github.com/A-D-Team/SharpMemshell)
				* [ShellCodeLoader](https://github.com/arsium/ShellCodeLoaderCSharp)
					* A small shellcode loader library written in C#. This small library allows you to inject shellcode in memory of current launched file or any other processes using different techniques. Useful to use as red team or in a remote access tool. Works for 32 & 64 bit shellcode.
				* [Sharperner](https://github.com/aniqfakhrul/Sharperner)
					* "Sharperner is a tool written in CSharp that generate .NET dropper with AES and XOR obfuscated shellcode."
				* [SharpTransactedLoad](https://github.com/G0ldenGunSec/SharpTransactedLoad)
					* Load .net assemblies from memory while having them appear to be loaded from an on-disk location. Bypasses AMSI and expands the number of methods available for use in loading arbitrary assemblies while still avoiding dropping files to disk - some of which provide additional functionality over the traditional Assembly.Load call. Currently built for .net 4.5, but should be compatible with other versions.
				* [HellgateLoader_CSharp](https://github.com/Kara-4search/HellgateLoader_CSharp)
					* Load shelcode via HELLGATE, rewrite hellgate for learning purpose.
				* [DarkMelkor](https://github.com/thiagomayllart/DarkMelkor)
					* Modified Version of Melkor @FuzzySecurity capable of creating disposable AppDomains in injected processes. 
				* [ThirdEye](https://github.com/kyleavery/ThirdEye)
					* Weaponizing CLRvoyance for Post-Ex .NET Execution 
				* [DLLFromMemory.Net](https://github.com/schellingb/DLLFromMemory-net)
					* C# library to load a native DLL from memory without the need to allow unsafe code 
				* [dnLauncher](https://github.com/aaaddress1/dnLauncher)
					* "Automatically select .NET Framework to load .NET programs + dynamic instrumentation to hijack the compileMethod of the JIT engine to intercept MSIL codes" - autotranslated
				* [Mimikore](https://github.com/secdev-01/Mimikore)
					* .NET 5 Single file Application . Mimikatz or any Base64 PE Loader.
				* [RunPE](https://github.com/nettitude/RunPE)
					* C# Reflective loader for unmanaged binaries.
				* [MemoryLoader](https://github.com/reznok/MemoryLoader)
					* A .NET binary loader that bypasses AMSI checks. It will patch AMSI, download a remote binary, and execute it in memory without the binary ever hitting disk.
				* [DiscerningFinch](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/DiscerningFinch)
					* "DiscerningFinch is ... discerning! FinchGen lets you create an encrypted templated which you can copy/paste into DiscerningFinch. At runtime DiscerningFinch collects an array of OS specific string constants and then attempts to use those to brute-force decrypt the inner binary. If it succeeds it loads the inner binary into memory passing along any command line arguments that may exists. If it fails, it prints out a .NET-looking error message as feedback."
				* [OffensivePipeline](https://github.com/Aetsu/OffensivePipeline)
				* [SharpCradle](https://github.com/anthemtotheego/SharpCradle)
					* SharpCradle is a tool designed to help penetration testers or red teams download and execute .NET binaries into memory.
				* [RunShellcode](https://github.com/zerosum0x0/RunShellcode)
					* Simple GUI program when you just want to run some shellcode.
				* [CreateThread Example](https://github.com/djhohnstein/CSharpCreateThreadExample)
					* C# code to use CreateThread to run position independent code in the running process. This code is provided AS IS, and will not be supported.
				* [CSharp SetThreadContext](https://github.com/djhohnstein/CSharpSetThreadContext)
					* C# Shellcode Runner to execute shellcode via CreateRemoteThread and SetThreadContext to evade Get-InjectedThread
				* [EAPrimer](https://github.com/m8r0wn/EAPrimer)
					* EAPrimer can be used to load .Net assemblies from a filepath or URL. On startup, it will attempt to perform in-memory patching of AMSI to bypass detection. By default, output is written to the console, however, this can be directed to a file or even sent via HTTP POST request to a remote server.
				* [NativePayload_ReverseShell](https://github.com/DamonMohammadbagher/NativePayload_ReverseShell)
				* [Vinchuca](https://github.com/lontivero/vinchuca)
					* Vinchuca is a resilent peer-to-peer botnet agent developed in .NET for educational purposes only. It is released with some missing features and without control panel in order to prevent misuses. However, it includes several interesting features
				* [SharpShooter](https://github.com/mdsecactivebreach/SharpShooter)
					* SharpShooter is a payload creation framework for the retrieval and execution of arbitrary CSharp source code. SharpShooter is capable of creating payloads in a variety of formats, including HTA, JS, VBS and WSF. It leverages James Forshaw's DotNetToJavaScript tool to invoke methods from the SharpShooter DotNet serialised object. Payloads can be retrieved using Web or DNS delivery or both; SharpShooter is compatible with the MDSec ActiveBreach PowerDNS project. Alternatively, stageless payloads with embedded shellcode execution can also be generated for the same scripting formats.
				* [Vayne-RaT](https://github.com/TheM4hd1/Vayne-RaT)
					* An Advanced C# .NET Rat, It’s Stable and Contains Many Features.
				* [CIMplant](https://github.com/FortyNorthSecurity/CIMplant)
				* C# port of WMImplant which uses either CIM or WMI to query remote systems. It can use provided credentials or 	the current user's session.
				* [QuasarRAT](https://github.com/quasar/QuasarRAT)
					* Quasar is a fast and light-weight remote administration tool coded in C#. Providing high stability and an easy-to-use user interface, Quasar is the perfect remote administration solution for you.
				* [RedPeanut](https://github.com/b4rtik/RedPeanut)
					* RedPeanut is a small RAT developed in .Net Core 2 and its agent in .Net 3.5 / 4.0.
		* **Managed in UnManaged Code**
			* **Articles/Blogposts/Writeups**
				* [The .NET Inter-Operability Operation - James Forshaw(Derbycon2017)](https://www.irongeek.com/i.php?page=videos/derbycon7/s13-the-net-inter-operability-operation-james-forshaw)
					* One of the best features of the .NET runtime is its in-built ability to call native code, whether that's APIs exposed from dynamic libraries or remote COM objects. Adding this in-built functionality to an "type-safe" runtime has its drawbacks, not the least the introduction of security issues due to misuse. This presentation will go into depth on how the .NET runtime implements its various interop features, where the bodies are buried and how to use that to find issues ranging from novel code execution mechanisms, elevation of privilege up to remote code execution. The presentation will assume the attendee has some familiarity with .NET and how the runtime executes code.
				* [CLRvoyance: Loading managed code into unmanaged processes - Bryan Alexander, Josh Stone(2020)](https://www.accenture.com/us-en/blogs/cyber-defense/clrvoyance-loading-managed-code-into-unmanaged-processes)
				* [Weird Ways to Run Unmanaged Code in .NET - Adam Chester(2021)](https://blog.xpnsec.com/weird-ways-to-execute-dotnet/)
			* **Tools**
				* [CLRvoyance](https://github.com/Accenture/CLRvoyance)
					* CLRvoyance is a shellcode kit that supports bootstrapping managed assemblies into unmanaged (or managed) processes. It provides three different implementations of position independent shellcode for CLR hosting, as well as a generator script for quickly embedding a managed assembly in position independent shellcode.
				* [Nautilus Project](https://github.com/xpn/NautilusProject)
					* A collection of weird ways to execute unmanaged code in .NET
				* [HostingCLR](https://github.com/etormadiv/HostingCLR)
					* Executing a .NET Assembly from C++ in Memory (CLR Hosting)
				* [AllTheThingsExec](https://github.com/secdev-01/AllTheThingsExec)
					* Executes Blended Managed/Unmanged Exports
		* **Unmanaged in Managed**
			* [native-loader](https://github.com/netcore-jroger/native-loader)
				* A class library that loads unmanaged library.
			* [MemoryModule.net](https://github.com/Scavanger/MemoryModule.net)
				* Loading a native DLL in the memory.
		* **Network**
			- **Articles/Blogposts/Writeups**
				* [Lateral Movement 101 - Rasta Mouse(2021)](https://offensivedefence.co.uk/posts/lateral-movement-101/)
			- **Tools**
				- **Proxies**
					* [SharpSocks](https://github.com/nettitude/SharpSocks)
						* Tunnellable HTTP/HTTPS socks4a proxy written in C# and deployable via PowerShell
				- **Sockets**
					* [AsyncSockets](https://github.com/rasta-mouse/AsyncSockets)
				- **Network-Tools**
					* [sharpNetstat](https://github.com/evi1ox/sharpNetstat)
				- **Network-Protocols**
					* [SSHClient](https://github.com/skahwah/SSHClient)
				- **Servers**
					* [SharpRelay](https://github.com/pkb1s/SharpRelay)
					* [NVNC](https://github.com/T1T4N/NVNC)
						* The first open-source .NET VNC Server written entirely in the C# programming language.
		* **Obfuscation**
			- **Articles/Blogposts/Writeups**
				* [Building an Obfuscator to Evade Windows Defender - Samuel Wong(2020)](https://www.xanthus.io/building-an-obfuscator-to-evade-windows-defender/)
				* [Applying the Invisibility Cloak: Obfuscate C# Tools to Evade Signature-Based Detection - Brett Hawkins(2021)](https://securityintelligence.com/posts/invisibility-cloak-obfuscate-c-tools-evade-signature-based-detection/)
			- **Tools**
				* [.NET Obfuscator Lists](https://github.com/NotPrab/.NET-Obfuscator)
				* [Lists of .NET Deobfuscator / Unpacker (Open Source)](https://github.com/NotPrab/.NET-Deobfuscator)
				* [CallObfuscation](https://github.com/CursedLand/CallObfuscation)
					* External Calls Hiding Using Calli.
				* [RosFuscator](https://github.com/Flangvik/RosFuscator)
					* YouTube/Livestream project for obfuscating C# source code using Roslyn
				* [LoGiC.NET](https://github.com/AnErrupTion/LoGiC.NET)
					* A more advanced free and open .NET obfuscator using dnlib. 
				* [AsStrongAsFuck](https://github.com/Charterino/AsStrongAsFuck)
					* A console obfuscator for .NET assemblies. 
				* [ConfuserEx2](https://github.com/mkaring/ConfuserEx)
					* ConfuserEx 2 is a open-source protector for .NET applications. It is the successor of Confuser project and the ConfuserEx project.
				* [NeoConfuserEx](https://github.com/XenocodeRCE/neo-ConfuserEx)
					* Neo ConfuserEx is the successor of ConfuserEx project, an open source C# obfuscator which uses its own fork of dnlib for assembly manipulation. Neo ConfuserEx handles most of the dotnet app, supports all elligible .NET Frameworks and provide decent obfuscation on your file.
				* [MindLated](https://github.com/Sato-Isolated/MindLated)
					* .net obfuscator
		* **Packers**
			* [DotNetCompressor](https://github.com/TotalTechGeek/DotNetCompressor)
				* Compresses .NET executables and merges dlls into a standalone, smaller executable.
		* **Payload Sample**
			* **Articles/Blogposts/Writeups**
			* **Talks/Presentations/Videos**
				* [New Livestream Series (Creating a Metasploit Implant in C# from scratch) - OJ Reeves(2019)](https://buffered.io/posts/new-livestream-series/)
					* "We’re going to build a .NET implementation of Meterpreter live on stream. Together. From scratch. Read on for all the details!"
		* **Tools/PoCs**
			* [clr-meterpreter](https://github.com/OJ/clr-meterpreter)
				* The full story of the CLR implementation of Meterpreter
			* [DcRat](https://github.com/qwqdanchun/DcRat)
				* DcRat is a simple remote tool written in C#
		* **Persistence**
			* [SharPersist](https://github.com/mandiant/SharPersist)
			* [SharPersist: Windows Persistence Toolkit in C# - Brett Hawkins(Derbycon2019](https://www.irongeek.com/i.php?page=videos/derbycon9/stable-25-sharpersist-windows-persistence-toolkit-in-c-brett-hawkins)
				* PowerShell has been used by the offensive community for several years now. However, recent advances in the defensive security industry are causing offensive toolkits to migrate from PowerShell to reflective C# to evade modern security products. Some of these advancements include Script Block Logging, Antimalware Scripting Interface (AMSI) and the development of signatures for malicious PowerShell activity by third-party security vendors. Several public C# toolkits such as Seatbelt, SharpUp and SharpView have been released to assist with tasks in various phases of the attack lifecycle. One phase of the attack lifecycle that has been missing a C# toolkit is persistence. This talk will be on the public release of a Windows persistence toolkit written in C# called SharPersist.
			* [SharpStay](https://github.com/0xthirteen/SharpStay)
				* .NET project for installing Persistence
			* [SharpHide](https://github.com/outflanknl/SharpHide)
				* [Technique Whitepaper](https://github.com/ewhitehats/InvisiblePersistence/blob/master/InvisibleRegValues_Whitepaper.pdf)
				* Just a nice persistence trick to confuse DFIR investigation. Uses NtSetValueKey native API to create a hidden (null terminated) registry key. This works by adding a null byte in front of the UNICODE_STRING key valuename.
			* [Reg_Built](https://github.com/P1CKLES/Reg_Built)
			* C# Userland Registry RunKey persistence
		* **Polymorphism**
			* [Self-Morphing C# Binary](https://github.com/bytecode77/self-morphing-csharp-binary)
		* **Privilege Escalation**
			* [SharpUp](https://github.com/GhostPack/SharpUp)
				* SharpUp is a C# port of various PowerUp functionality. Currently, only the most common checks have been ported; no weaponization functions have yet been implemented.
			* [Watson](https://github.com/rasta-mouse/Watson)
				* Enumerate missing KBs and suggest exploits for useful Privilege Escalation vulnerabilities
			* [Net-GPPPassword](https://github.com/outflanknl/Net-GPPPassword)
				* .NET/C# implementation of Get-GPPPassword. Retrieves the plaintext password and other information for accounts pushed through Group Policy Preferences.
		* **Processes**
			* [C# Process Class Primer - Rastamouse(2021)](https://offensivedefence.co.uk/posts/csharp-process-class/)
			* [ProcessThis](https://github.com/jamcut/ProcessThis)
				* Small C# tool to call out AV/EDR processes running.
			* [CloneProcess](https://github.com/mobdk/CloneProcess)
				* Clone running process with ZwCreateProcess (syscall)
		* **PS in C#**
			* **Articles/Blogposts/Writeups**
				* [Executing PowerShell scripts from C# - doc.ms(2014)](https://docs.microsoft.com/en-us/archive/blogs/kebab/executing-powershell-scripts-from-c)
					* "In today’s post, I will demonstrate the basics of how to execute PowerShell scripts and code from within a C#/.NET applications. I will walk through how to setup your project prerequisites, populate the pipeline with script code and parameters, perform synchronous and asynchronous execution, capture output, and leverage shared namespaces."
				* [Using C# for post-PowerShell attacks - John Bergbom(2018)](https://www.forcepoint.com/blog/x-labs/using-c-post-powershell-attacks)
			* **Tools**
				* [NoPowerShell](https://github.com/bitsadmin/nopowershell)
					* NoPowerShell is a tool implemented in C# which supports executing PowerShell-like commands while remaining invisible to any PowerShell logging mechanisms. This .NET Framework 2 compatible binary can be loaded in Cobalt Strike to execute commands in-memory. No System.Management.Automation.dll is used; only native .NET libraries. An alternative usecase for NoPowerShell is to launch it as a DLL via rundll32.exe: rundll32 NoPowerShell.dll,main.
				* [p0wnedShell](https://github.com/Cn33liz/p0wnedShell)
					* PowerShell Runspace Post Exploitation Toolkit 
				* [p0wnedLoader](https://github.com/Cn33liz/p0wnedLoader)
				* [Smallp0wnedShell](https://github.com/3gstudent/Smallp0wnedShell)
					* Small modification version of PowerShell Runspace Post Exploitation Toolkit (p0wnedShell)
				* [CScriptShell](https://github.com/Cn33liz/CScriptShell)
				* [Stracciatella](https://github.com/mgeeky/Stracciatella)
					* OpSec-safe Powershell runspace from within C# (aka SharpPick) with AMSI, CLM and Script Block Logging disabled at startup
				* [SpaceRunner](https://github.com/Mr-B0b/SpaceRunner)
					* This tool enables the compilation of a C# program that will execute arbitrary PowerShell code, without launching PowerShell processes through the use of runspace.
		* **Recon (Host)**
			* [SeatBelt](https://github.com/GhostPack/Seatbelt)
				* Seatbelt is a C# project that performs a number of security oriented host-survey "safety checks" relevant from both offensive and defensive security perspectives. 
		* **Recon (Network)**
			* [SharpShares](https://github.com/mitchmoser/SharpShares)
				* Multithreaded C# .NET Assembly to enumerate accessible network shares in a domain
			* [Scout](https://github.com/jaredhaight/scout)
				* Scout is a .NET assembly used to perform recon on hosts during a pentest. Specifically, this was created as a way to check a host before laterally moving to it.
		* **Reflection**
		    * [Reflection (C#) - docs.ms](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/reflection)
	    		* Reflection provides objects (of type Type) that describe assemblies, modules, and types. You can use reflection to dynamically create an instance of a type, bind the type to an existing object, or get the type from an existing object and invoke its methods or access its fields and properties. If you are using attributes in your code, reflection enables you to access them. For more information, see Attributes.
	    	* [How C# Reflection Works With Code Examples - stackify](https://stackify.com/what-is-c-reflection/)
	    	* [Reflection in .NET - keesari_anjaiah(2010)](https://www.codeproject.com/Articles/55710/Reflection-in-NET)
	    	* [What is Reflection in C#? - geeksforgeeks(2019)](https://www.geeksforgeeks.org/what-is-reflection-in-c-sharp/)
		* **Registry (Windows)**
			* [RegistryStrikesBack](https://github.com/mdsecactivebreach/RegistryStrikesBack)
				* RegistryStrikesBack allows a red team operator to export valid .reg files for portions of the Windows Registry via a .NET assembly that should run as a standard user.
			* [Registry](https://github.com/EricZimmerman/Registry)
				* Full featured, offline Registry parser in C#.
		* **Resource Embedding**
			* [Single File Executable - docs.ms](https://docs.microsoft.com/en-us/dotnet/core/whats-new/dotnet-core-3-0#single-file-executables)
			* [Assembly Linking - docs.ms](https://docs.microsoft.com/en-us/dotnet/core/whats-new/dotnet-core-3-0#assembly-linking)
			* [Embedding .NET Assemblies inside .NET Assemblies - Denham Coder(2018)](https://denhamcoder.net/2018/08/25/embedding-net-assemblies-inside-net-assemblies/)
			* [Fody](https://github.com/Fody/Home/#endofbacking)
				* The Home repository is the starting point for people to learn about Fody, the project.
			* [Fody Engine](https://github.com/Fody/Fody)
				* Extensible tool for weaving .net assemblies. Manipulating the IL of an assembly as part of a build requires a significant amount of plumbing code. This plumbing code involves knowledge of both the MSBuild and Visual Studio APIs. Fody attempts to eliminate that plumbing code through an extensible add-in model.
			* [Costura](https://github.com/Fody/Costura)
				* Embed references as resources
		* **Scheduled Tasks**
			* **Articles/Blogposts/Writeups**
				* [Creating Scheduled Tasks(C#) - StackOverflow](https://stackoverflow.com/questions/7394806/creating-scheduled-tasks)
				* [Creating a Task Using NewWorkItem Example - docs.ms](https://docs.microsoft.com/en-us/windows/win32/taskschd/creating-a-task-using-newworkitem-example)
			* **Tools**
				* [Task Scheduler](https://github.com/dahall/taskscheduler)
					* Provides a .NET wrapper for the Windows Task Scheduler. It aggregates the multiple versions, provides an editor and allows for localization.
				* [ScheduleRunner](https://github.com/netero1010/ScheduleRunner)
					* A C# tool with more flexibility to customize scheduled task for both persistence and lateral movement in red team operation
		- **Service(Windows)**
			* [WindowsService](https://github.com/faisal5170/WindowsService)
				* How to create windows service in c# 
		* **Symbolic Links**
			* [SharpLink](https://github.com/usdAG/SharpLink)
				* Create file system symbolic links from low privileged user accounts within PowerShell
		* **Serialization**
			* **Gadget2Jscript**
				* [GadgetToJScript - RastaMouse(2020)](https://rastamouse.me/blog/gadgettojscript/)
					* [Github](https://github.com/rasta-mouse/GadgetToJScript)
				* [GadgetToJScript - 3gstudent](https://3gstudent.github.io/3gstudent.github.io/GadgetToJScript%E5%88%A9%E7%94%A8%E5%88%86%E6%9E%90/)
				* [GadgetToJScript](https://github.com/med0x2e/GadgetToJScript)
					* A tool for generating .NET serialized gadgets that can trigger .NET assembly load/execution when deserialized using BinaryFormatter from JS/VBS based scripts. The gadget being used triggers a call to Assembly.Load when deserialized via jscript/vbscript, this means it can be used in the same way to trigger in-memory load of your own shellcode loader at runtime. Lastly, the tool was created mainly for automating WSH scripts weaponization for RT engagements (LT, Persistence, Initial Compromise), the shellcode loader which was used for PoC is removed and replaced by an example assembly implemented in the "TestAssemblyLoader.cs" class for PoC purpose.
				* [GadgetToJScript, Covenant, Donut - 3xpl01tc0d3r](https://3xpl01tc0d3r.blogspot.com/2020/02/gadgettojscript-covenant-donut.html)
			* **Tools**
				* [DotNetDeserializationScanner](https://github.com/leechristensen/DotNetDeserializationScanner)
					* Scans for .NET Deserialization Bugs in .NET Assemblies 
		* **Syscalls**
			* [Red Team Tactics: Utilizing Syscalls in C# - Prerequisite Knowledge - Jack Halon(2020)](https://jhalon.github.io/utilizing-syscalls-in-csharp-1/)
				* [Part2: Writing The Code](https://jhalon.github.io/utilizing-syscalls-in-csharp-2/)
			* **Tools**
				* [An example of using Syscalls in C# to get a meterpreter shell.](https://github.com/plackyhacker/Sys-Calls)
				* [TripleS - Extracting Syscall Stub, Modernized](https://github.com/GetRektBoy724/TripleS)
					* "TripleS or 3S is short for Syscall Stub Stealer. It freshly "steal" syscall stub straight from the disk. You can use TripleS for evading userland hooks from EDRs/AVs.TripleS doesnt invoke any unmanaged API, its all .NET's managed function. I cant say that its better than D/Invoke's GetSyscallStub, but in my opinion, its better. Anyway, I suck at making description, so if you have any question,you can DM me on Discord."
				* [SysCallTables](https://github.com/hfiref0x/SyscallTables)		
				* [SharpCall](https://github.com/jhalon/SharpCall)
					* Simple proof of concept code that allows you to execute direct system calls in C# by utilizing unmanaged code to bypass EDR and API Hooking.
		* **User Simulation**
			* [Sim](https://github.com/IceMoonHSV/Sim)
				* Sim is a C# application that ingests an XML file and performs tasks based on the provided XML. It is meant to resemble user actions on a system. The goal of this is to help facilitate training and education by providing a more realistic environment to practice.
		* **Web Server**
			* [SharpWebServer](https://github.com/mgeeky/SharpWebServer)
				* A Red Team oriented simple HTTP & WebDAV server written in C# with functionality to capture Net-NTLM hashes. To be used for serving payloads on compromised machines for lateral movement purposes.
		* **Windows Services**
			* [Using Parameters With InstallUtil - ip3lee](https://diaryofadeveloper.wordpress.com/2012/04/26/using-paramters-with-installutil/)
			* [SharpSC](https://github.com/djhohnstein/SharpSC)
				* Simple .NET assembly to interact with services.
		* **WinAPI Access**
			* **Articles/Blogposts/Writeups**
				* [Offensive P/Invoke: Leveraging the Win32 API from Managed Code - Matt Hand](https://posts.specterops.io/offensive-p-invoke-leveraging-the-win32-api-from-managed-code-7eef4fdef16d)
				* [SharpSploit.Execution.DynamicInvoke](https://github.com/cobbr/SharpSploit/blob/master/SharpSploit/SharpSploit%20-%20Quick%20Command%20Reference.md#sharpsploitexecutiondynamicinvoke)
			* **DInvoke**
				* **Articles/Blogposts/Writeups**
					* [Emulating Covert Operations - Dynamic Invocation (Avoiding PInvoke & API Hooks) - thewover(2020)](https://thewover.github.io/Dynamic-Invoke/)
					* [D/Invoke & GadgetToJScript - Rasta Mouse(2021)](https://rastamouse.me/d-invoke-gadgettojscript/)
				* **Tools**
					* [DInvoke](https://github.com/TheWover/DInvoke)
						* Dynamic replacement for PInvoke on Windows. DInvoke contains powerful primitives that may be combined intelligently to dynamically invoke unmanaged code from disk or from memory with careful precision. This may be used for many purposes such as PE parsing, intelligent dynamic API resolution, dynamically loading PE plugins at runtime, process injection, and avoiding API hooks.
					* [Reprobate](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/Reprobate)
						* "Reprobate consists of two cs files which contain all of the DynamicInvoke functionality and are meant to be plug-and-play for your C# projects. This can be preferable to using a nuget package or whole-sale including SharpSploit. Eventually I will integrate bubble-sort Syscall ID identification as well to avoid manual ntdll mapping/enumeration."
			* **PInvoke**
				* **Articles/Blogposts/Writeups**
					* [Platform Invoke (P/Invoke) - docs.ms](https://docs.microsoft.com/en-us/dotnet/standard/native-interop/pinvoke)
					* [How to: Call Native DLLs from Managed Code Using PInvoke - docs.ms](https://docs.microsoft.com/en-us/cpp/dotnet/how-to-call-native-dlls-from-managed-code-using-pinvoke?view=msvc-160)
					* [pinvoke](https://github.com/dotnet/pinvoke)
						* A library containing all P/Invoke code so you don't have to import it every time. Maintained and updated to support the latest Windows OS. 
						* [pinvoke.net](https://www.pinvoke.net/)
				* **Tools**
			* **Tools**
				* [Vanara](https://github.com/dahall/Vanara)
					* This project contains various .NET assemblies that contain P/Invoke functions, interfaces, enums and structures from Windows libraries. Each assembly is associated with one or a few tightly related libraries. For example, Shlwapi.dll has all the exported functions from shlwapi.lib; Kernel32.dll has all for both kernel32.lib and kernelbase.lib.
				* [ManagedWindows](https://github.com/zodiacon/ManagedWindows)
					* Managed wrappers around the Windows API and some Native API
				* [taskkill](https://github.com/malcomvetter/taskkill)
					* This is a reference example for how to call the Windows API to enumerate and kill a process similar to taskkill.exe. This is based on (incomplete) MSDN example code. Proof of concept or pattern only.
				* [DnsCache](https://github.com/malcomvetter/DnsCache)
					* This is a reference example for how to call the Windows API to enumerate cached DNS records in the Windows resolver. Proof of concept or pattern only.
				* [GetAPISetMapping](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/GetAPISetMapping)
					* This project parses the PEB to match Windows API Set DLL's to their host DLL.
				* [SystemProcessAndThreadsInformation](https://github.com/FuzzySecurity/Sharp-Suite/tree/master/SystemProcessAndThreadsInformation)
	- **Go**<a name="gopay"></a>
		* **Articles/Blogposts**
			* [Antidebug Golang binary on Windoze ☯ - @lfm3773](https://acmpxyz.com/go_antidebug.html)
		* **Talks/Presentations**
			* [Concurrency is not parallelism - Andrew Gerrand(2013)](https://blog.golang.org/waza-talk)
			* [Hack like a Gopher - Kent Gruber(BSides Detroit2018)](https://www.irongeek.com/i.php?page=videos/bsidesdetroit2018/bsides-detroit-2018-104-hack-like-a-gohper-kent-gruber)
				* The Go programming language is fast, statically typed, and compiled but it feels that feels like a dynamically typed, interpreted language. What does that mean; and what does that do for you? Demonstrating the qualities of Golang from an attack and defense perspective we will explore some of the benefits of using Go to build fast, cross-platform applications.
		* **Crypter/Obfuscation**
			* **Articles/Blogposts**
				* [Encrypt And Decrypt Data In A Golang Application With The Crypto Packages - Nic Raboy(2019)](https://www.thepolyglotdeveloper.com/2018/02/encrypt-decrypt-data-golang-application-crypto-packages/)
				* [A Trinity of Shellcode, AES & Golang - Syscall59 — Alan Vivona(2019)](https://medium.com/syscall59/a-trinity-of-shellcode-aes-go-f6cec854f992)
			* **Tools/Libraries**
				* [gobfuscate](https://github.com/unixpickle/gobfuscate)
					* Currently, gobfuscate manipulates package names, global variable and function names, type names, method names, and strings.
		* **Fileystem**
			* [Pandoras Box](https://github.com/capnspacehook/pandorasbox)
				* "pandorasbox is a Go package that allows for simple use of both a host's filesystem, and a virtual filesystem."
		* **Libraries**
			* [Coldfire](https://github.com/redcode-labs/Coldfire)
				* Golang malware development framework
			* [SSDEEP](https://github.com/glaslos/ssdeep)
				* SSDEEP hash lib in Golang
			* [Robotgo](https://github.com/go-vgo/robotgo)
				* Golang Desktop Automation. Control the mouse, keyboard, bitmap, read the screen, Window Handle and global event listener.
			* [The Universal Loader](https://github.com/Binject/universal)
				* This loader provides a unified Go interface for loading shared libraries from memory on Windows, OSX, and Linux. Also included is a cross-platform `Call()` implementation that lets you call into exported symbols from those libraries without stress.
		* **OLE(Windows)**
			* [go-ole](https://github.com/go-ole/go-ole)
		* **Samples/Examples**
			* [RendevousRat](https://github.com/rvrsh3ll/RendezvousRAT)
				* This repository contains two minimal proof-of-concept RAT's utilizing GO, based on the examples found at go-libp2p-examples
			* [Doge-Loader](https://github.com/timwhitez/Doge-Loader)
				* Cobalt Strike Shellcode Loader by Golang 
			* [C2](https://github.com/averagesecurityguy/c2)
				* The C2 repository seeks to provide a practical implementation of the ideas contained in the Red Team Infrastructure Wike at https://github.com/bluscreenofjeff/Red-Team-Infrastructure-Wiki. In particular, this repository provides two Go packages one for beaconers and another for downloaders. In addition, the repository provides sample implants that use these beaconers and downloaders. Finally, the repository contains backend DNS and HTTP servers for C2 and configuration information for building front-end redirector servers.
			* [GrayStorm](https://github.com/GrayKernel/GrayStorm)
				* GrayStorm is an in memory attack platform that targets the .NET Framework and is injectable by utilizing GrayFrost.
			* [GrayFrost](https://github.com/graykernel/GrayFrost)
				* GrayFrost is a C++ DLL delivery system for C# payloads. Once compiled, GrayFrost can be injected into .NET applications using any DLL injection technique you wish!
			* [CHAOS](https://github.com/tiagorlampert/CHAOS)
				* Windows payload generator in go
			* [gscript](https://github.com/gen0cide/gscript)
				* Gscript is a framework for building multi-tenant executors for several implants in a stager. The engine works by embedding runtime logic (powered by the V8 Javascript Virtual Machine) for each persistence technique. This logic gets run at deploy time on the victim machine, in parallel for every implant contained with the stager. The Gscript engine leverages the multi-platform support of Golang to produce final stage one binaries for Windows, Mac, and Linux.
			* [Payload Delivery for DevOps : Building a Cross-Platform Dropper Using the Genesis Framework, Metasploit and Docker - khastex(2020)](https://khast3x.club/posts/2020-06-27-Cross-Platform-Dropper/)
		* **Shellcode**
			* [go-shellcode](https://github.com/brimstone/go-shellcode)
				* This is a program to run shellcode as its own process, all from memory. This was written to defeat anti-virus detection.
		* **Tradecraft**
			* **Articles/Blogposts**
				* [Malware Development Pt. 1: Dynamic Module Loading in Go - Dwight Hohnstein(2020)](https://posts.specterops.io/malware-development-pt-1-dynamic-module-loading-in-go-1121f07f3a5a)
				* [Trimming the fat from a Golang binary - Ben E C Boyter(2020)](https://web.archive.org/web/20210214140418/https://boyter.org/posts/trimming-golang-binary-fat/)
				* [Shrink your Go binaries with this one weird trick - Filippo Valsorda(2016)](https://blog.filippo.io/shrink-your-go-binaries-with-this-one-weird-trick/)
				* [Golang Offensive Tools with C-Sto and capnspacehook - awgh(2019)](https://www.symbolcrash.com/podcast/golang-offensive-tools-with-c-sto-and-capnspacehook/)
				* [Encrypted-at-Rest Virtual File-System in Go - awgh(2019)](https://www.symbolcrash.com/2019/07/22/encrypted-at-rest-virtual-file-system-in-go/)
			* **Talks/Presentations/Videos**
				* [(P|G)Ohst Exploitation - Carl Vincent(2016)](https://archive.org/details/P-G_Ohst_Exploitation)
					* This talk focuses on showcasing examples of the GO programming language being utilized to rapidly prototype, and ultimately maintain software designed to perform common or useful post-exploitation tasks. Source code for each feature will be provided, and is intended to exaggerate the limited amount of code and code familiarity required to construct relatively complex payloads capable of performing offensive security tasks fully either in an automated, or fully antonymous context.
		* **Tools**
			* [Geacon](https://github.com/darkr4y/geacon)
				* Using Go to implement CobaltStrike's Beacon
	* **Haskell**<a name="haskell"></a>
		* [Hacking with Haskell - Max Harley(2021)](https://itnext.io/hacking-with-haskell-28887c1f2d06)
	* **Janet**<a name="janet"></a>
		* [Janet](https://github.com/janet-lang/janet)
			* Janet is a functional and imperative programming language and bytecode interpreter. It is a lisp-like language, but lists are replaced by other data structures (arrays, tables (hash table), struct (immutable hash table), tuples). The language also supports bridging to native code written in C, meta-programming with macros, and bytecode assembly.
	* **Java**<a name="java"></a>
		* [Java RATS: Not even your Macs are safe - Anthony Kasza(Derbycon2016)](https://www.irongeek.com/i.php?page=videos/derbycon6/318-java-rats-not-even-your-macs-are-safe-anthony-kasza)
			* Java's 'write once, run anywhere' features make it a popular cross-platform vector for attackers of all skill levels. This talk will perform a deep examination of historic and trending Java malware families, their capabilities and indicators, and will reveal uncommon analysis techniques to immediately help you with investigations.
	* **.NET**<a name=".net"></a>
		* **101**
			* [A tour of the C# language - docs.ms](https://docs.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/)
				* C# (pronounced "See Sharp") is a modern, object-oriented, and type-safe programming language. C# has its roots in the C family of languages and will be immediately familiar to C, C++, Java, and JavaScript programmers. This tour provides an overview of the major components of the language in C# 8 and earlier. 
			* [Inside a C# program - docs.ms](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/)
				* The section discusses the general structure of a C# program, and includes the standard "Hello, World!" example.
			* [AppDomain Class - docs.ms](https://docs.microsoft.com/en-us/dotnet/api/system.appdomain?view=netcore-3.1)
				* Represents an application domain, which is an isolated environment where applications execute. This class cannot be inherited.
			* [Assemblies in .NET - docs.ms](https://docs.microsoft.com/en-us/dotnet/standard/assembly/)
				* Assemblies form the fundamental units of deployment, version control, reuse, activation scoping, and security permissions for .NET-based applications. An assembly is a collection of types and resources that are built to work together and form a logical unit of functionality. Assemblies take the form of executable (.exe) or dynamic link library (.dll) files, and are the building blocks of .NET applications. They provide the common language runtime with the information it needs to be aware of type implementations.
			* [An Introduction to Writing .NET Executables for Pentesters - PEEW.PW](https://www.peew.pw/blog/2017/11/24/an-introduction-to-writing-net-executables-for-pentesters)
		* **Non-101**
			* [.NET Malware Threat: Internals and Reversing - Alexandre Borges(Defcon2019)](http://www.blackstormsecurity.com/docs/ALEXANDREBORGES_DEFCON_2019.pdf)
			* [Hiding your .NET - COMPlus_ETWEnabled - Adam Chester(2020)](https://blog.xpnsec.com/hiding-your-dotnet-complus-etwenabled/)
			* [Building the CLR Meterpreter - OJ Reeves(2020)](https://www.youtube.com/playlist?list=PLYovnhafVaw-wGlLtQw1N0dHjxkkvc62o)
			* [clr-meterpreter](https://github.com/OJ/clr-meterpreter)
				* The full story of the CLR implementation of Meterpreter
			* [SharpC2 Development Series - Rastamouse](https://www.youtube.com/playlist?list=PLFeVmEN0T_KeOxXfCAtJ14TZ_Nk2qa9Ll)
			* [.NET Core for Malware – Ryan Cobb (SO-CON 2020)](https://www.youtube.com/watch?v=woRfx5D2Y9Y&list=PLJK0fZNGiFU-2vFpjnt96j_VSuQVTkAnO&index=11)
				* .NET Core is the future of .NET. The Windows-only .NET Framework is on it's way out, and the cross-platform .NET Core is Microsoft's new flagship framework for building software. As red teamers, it's time to go back to the well of .NET as a host for implants and post-exploitation. In this talk, we will analyze the opportunities presented by the new .NET Core platform and practical examples to take advantage of them.
		* **Bring-Your-Own-Compiler/Compiler Stacking**
			* [Red Team Level over 9000! Fusing the powah of .NET with a scripting language of your choosing: introducing BYOI (Bring Your own Interpreter) payloads. - Marcello Salvati(Derbycon2019)](https://www.irongeek.com/i.php?page=videos/derbycon9/1-17-red-team-level-over-9000-fusing-the-powah-of-net-with-a-scripting-language-of-your-choosing-introducing-byoi-bring-your-own-interpreter-payloads-marcello-salvati)
				* With all of the defenses Microsoft has implemented in the PowerShell run-time over the past few years Red Teamers & APT groups have started too shy away from using PowerShell based payloads/delivery mechanisms and migrate over to C#. However, C# is a compiled language, operationally this has a few major downsides: we can?t be as ?flexible? as we could be with scripting languages, setting up a proper development environment has overhead, things need to be compiled etc... in this talk, I will be covering my approach to solving these operational problems by using some of the (possibly?) lesser known features of the .NET framework and introducing BYOI (Bring Your Own Interpreter) payloads which allow you to embed a scripting language of your choosing into any .NET language!
			* [Zolom](https://github.com/checkymander/Zolom)
    			* C# Executable with embedded Python that can be used reflectively to run python code on systems without Python installed
			* [Inception-Framework](https://github.com/two06/Inception)
				* Inception provides In-memory compilation and reflective loading of C# apps for AV evasion. Payloads are AES encrypted before transmission and are decrypted in memory. The payload server ensures that payloads can only be fetched a pre-determined number of times. Once decrypted, Roslyn is used to build the C# payload in memory, which is then executed using reflection.
		* **Crypter/Obfuscation**
			* [NET-Obfuscate](https://github.com/BinaryScary/NET-Obfuscate)
				* Obfuscate ECMA CIL (.NET IL) assemblies to evade Windows Defender AMSI.
		* **Injection/Shellcode/In-Memory**
			* [Red Team Tradecraft: Loading Encrypted C# Assemblies In Memory - mike gualtieri(2020)](https://www.mike-gualtieri.com/posts/red-team-tradecraft-loading-encrypted-c-sharp-assemblies-in-memory)
			* [ManagedInjection](https://github.com/malcomvetter/ManagedInjection)
				* A proof of concept for injecting a pre-compiled .net assembly in memory at runtime with zero pre-knowledge of its assembly namespace or type. All that is necessary is a convention for the initial method name which will be instantiated, or just have the assembly initialize via its Constructor for a true "zero knowledge" scenario.
			* [TikiTorch](https://github.com/rasta-mouse/TikiTorch)
				* TikiTorch was named in homage to CACTUSTORCH by Vincent Yiu. The basic concept of CACTUSTORCH is that it spawns a new process, allocates a region of memory, then uses CreateRemoteThread to run the desired shellcode within that target process. Both the process and shellcode are specified by the user.
				* [TikiTorch - Rastamouse](https://rastamouse.me/blog/tikitorch/)
				* [TikiVader - Rastamouse](https://rastamouse.me/blog/tikivader/)
				* [The Return of Aggressor - Rastamouse](https://rastamouse.me/blog/tikigressor/)
				* [TikiService - Rastamouse](https://rastamouse.me/blog/tikiservice/)
				* [Lighting the path through EDRs using TikiTorch - RhythmStick(2019)](https://www.rythmstick.net/posts/tikitorch/)
			* [Red Team Tradecraft: Loading Encrypted C# Assemblies In Memory - mike gualtieri(2020)](https://www.mike-gualtieri.com/posts/red-team-tradecraft-loading-encrypted-c-sharp-assemblies-in-memory)
		* **Networking**
		* **PE32**
			* [Conari](https://github.com/3F/Conari)
				* Conari engine represents powerful platform for work with unmanaged memory, pe-modules, related PInvoke features, and more for: Libraries, Executable Modules, enjoying of the unmanaged native C/C++ in .NET world, and other raw binary data. Even accessing to complex types like structures without their declaration at all.
			* [LuNari](https://github.com/3F/LuNari)
				* LuNari is Lua for .NET on Conari engine
			* [.NET DllExport](https://github.com/3F/DllExport)
				* .NET DllExport with .NET Core support (aka 3F/DllExport)
		* **Publishing**
		* **Examples/Samples**
			* [AsyncRAT-VB.NET](https://github.com/TheWover/AsyncRAT-VB.NET)
				* Remote Administration Tool For Windows VB.NET 
			* [OffensiveDLR](https://github.com/byt3bl33d3r/OffensiveDLR)
				* Toolbox containing research notes & PoC code for weaponizing .NET's DLR
		* **WebServer**
		* **Other**
			* [Unstoppable Service](https://github.com/malcomvetter/UnstoppableService)
				* A pattern for a self-installing Windows service in C# with the unstoppable attributes in C#.		
		* **Talks/Presentations/Videos**
			* [.NET Malware Threats: Internals And Reversing - Alexandre Borges(Defcon27)](https://www.youtube.com/watch?v=UB3pVTO5izU)
				* .NET malware is well-known by security analysts, but even existing many tools such as dnSpy,.NET Reflector, de4dot and so on to make the analysis easier, most professionals have used them as a black box tool, without concerning to .NET internals, structures, MSIL coding and details. In critical cases, it is necessary have enough knowledge about internal mechanisms and to debug these .NET threats using WinDbg.  Unfortunately, .NET malware samples have become very challenger because it is so complicated to deobfuscated associated resources, as unpacking and dumping them from memory. Furthermore, most GUI debugging tools does an inside view of mechanisms such as CRL Loader, Managed Heap, Synchronization issues and Garbage Collection.  In the other side, .NET malware threats are incredibly interesting when analyzed from the MSIL instruction code, which allows to see code injections using .MSIL and attempts to compromise .NET Runtime keep being a real concern.  The purpose of this presentation is to help professionals to understand .NET malware threats and techniques by explaining concepts about .NET internals, mechanisms and few reversing techniques.
	- **Nim**<a name="nimlang"></a>
		* **Articles/Blogposts**
			* [Bypassing Windows protection mechanisms & Playing with OffensiveNim - s3cur3th1ssh1t(2020)](https://s3cur3th1ssh1t.github.io/Playing-with-OffensiveNim/)
			* [Implant Roulette Part 1: Nimplant - NotoriousRebel(2020)](https://secbytes.net/implant-roulette-part-1:-nimplant/)
			* [Мета-программирование Nim и обфускация - Rel(2020)](https://wasm.in/blogs/meta-programmirovanie-nim-i-obfuskacija.706)
		* **Malware/APT Samples**
			* [Linux.Cephei: a Nim virus - Guilherme Thomazi(2017)](https://www.guitmz.com/linux-cephei-a-nim-virus/)
			* [Zebrocy’s Multilanguage Malware Salad - Global Research & Analysis Team, Kaspersky Lab(2019)](https://securelist.com/zebrocys-multilanguage-malware-salad/90680/)
			* [Nimar Loader - https://medium.com/walmartglobaltech/nimar-loader-4f61c090c49e(2021)](https://medium.com/walmartglobaltech/nimar-loader-4f61c090c49e)
			* [Investigation into the state of Nim malware - Jason Reaves, Joshua Platt(2021)](https://medium.com/walmartglobaltech/investigation-into-the-state-of-nim-malware-14cc543af811)
		* **Config**
			* [Using NimScript as a configuration language (Embedding NimScript pt. 1) - peterme.net](https://peterme.net/using-nimscript-as-a-configuration-language-embedding-nimscript-pt-1.html)
		* **Crypter/Obfuscation**
			* [denim](https://github.com/moloch--/denim)
				* Automated compiler obfuscation for nim 
			* [steganography](https://github.com/treeform/steganography)
				* Image stego library
		* **Examples**
			* [Nimplant](https://github.com/MythicAgents/Nimplant)
				* Nimplant is a cross-platform (Linux & Windows) implant written in Nim as a fun project to learn about Nim and see what it can bring to the table for red team tool development. Currently, Nimplant lacks extensive evasive tradecraft; however, overtime Nimplant will become much more sophisticated.
			* [NimExamples](https://github.com/ajpc500/NimExamples)
			* [Linux.Cephei](https://github.com/guitmz/nim-cephei)
				* Probably the first ELF binary infector ever created in Nim.
		* **Injection**
		* **Networking**
			* [nim-libp2p](https://github.com/status-im/nim-libp2p)
				* libp2p implementation in Nim
			* [Nim-SMBExec](https://github.com/elddy/Nim-SMBExec)
				* SMBExec implementation in Nim - SMBv2 using NTLM Authentication with Pass-The-Hash technique
			* [NimScan](https://github.com/elddy/NimScan)
				* Really fast port scanner (With filtered option - Windows support only)
			* [iputils](https://github.com/rockcavera/nim-iputils)
				* Utilities for use with IP. It has functions for IPv4, IPv6 and CIDR.
			* [nim-socks5](https://github.com/FedericoCeratto/nim-socks5)
				* Nim Socks5 library
			* [backoff](https://github.com/CORDEA/backoff)
				* Implementation of exponential backoff for nim. 
		* **PE32**
		* **Publishing**
		* **Injection/Shellcode**
			* [Shellcode Injection using Nim and Syscalls - ajpc500](https://ajpc500.github.io/nim/Shellcode-Injection-using-Nim-and-Syscalls/)
		* **Syscalls**
			* [nim-syscall](https://github.com/def-/nim-syscall)
				* Raw system calls for Nim [Linux]
			* [NimlineWhispers](https://github.com/ajpc500/NimlineWhispers)
				* A very proof-of-concept port of InlineWhispers for using syscalls in Nim projects. 
		* **Tradecraft**
			* [OffensiveNim](https://github.com/byt3bl33d3r/OffensiveNim)
				* "My experiments in weaponizing Nim for implant development and general offensive operations."
			* [c2nim](https://github.com/nim-lang/c2nim)
				*  c2nim is a tool to translate Ansi C code to Nim. The output is human-readable Nim code that is meant to be tweaked by hand before and after the translation process.
		* **Utilities**
			* [zippy](https://github.com/guzba/zippy)
				* Pure Nim implementation of deflate, zlib, gzip and zip. 
			* [nim-registry](https://github.com/miere43/nim-registry)
				* Deal with Windows Registry from Nim.
			* [nim-daemon](https://github.com/status-im/nim-daemon)
				* This closs-platform library is used to daemonize processes: that is, make them run in the background and independently of the terminal. The library is used to develop Unix daemons and background processes on Windows.
		* **Web(Server)**
			* [jester](https://github.com/dom96/jester)
				* A sinatra-like web framework for Nim.
			* [Karax](https://github.com/pragmagic/karax)
				* Single page applications for Nim.
			* [Neel](https://github.com/Niminem/Neel)
				* A Nim library for making Electron-like HTML/JS GUI apps, with full access to Nim capabilities. 
			* [ws](https://github.com/treeform/ws)
				* Simple WebSocket library for nim.
		* **Other**				
			* [libkeepass](https://github.com/PMunch/libkeepass)
				* Library for reading KeePass files and decrypt the passwords within it 
	* **PowerShell**<a name="powershell"></a>
		- **Stage0/1 Loaders/Droppers**
			* [PowerAssembly](https://github.com/DarkCoderSc/PowerAssembly)
				* Map in current PowerShell Instance Memory .NET Assemblies from remote web server.
		* [Invoke-BSOD](https://github.com/peewpw/Invoke-BSOD)
			* A PowerShell script to induce a Blue Screen of Death (BSOD) without admin privileges. Also enumerates Windows crash 	dump settings. This is a standalone script, it does not depend on any other files.
		* [PowerDropper](https://github.com/gigajew/PowerDropper)
			* App that generates PowerShell dropper scripts for .NET executables
		* [PowerStager](https://github.com/z0noxz/powerstager)
			* This script creates an executable stager that downloads a selected powershell payload, loads it into memory and executes it using obfuscated EC methods. The script will also encrypt the stager for dynamic signatures and some additional obfuscation. This enables the actual payload to be executed indirectly without the victim downloading it, only by executing the stager. The attacker can then for example implement evasion techniques on the web server, hosting the payload, instead of in the stager itself.
	- **Python**<a name="python"></a>
		* **Binaries**
			* [LIEF](https://github.com/lief-project/LIEF)
				* LIEF - Library to Instrument Executable Formats. The purpose of this project is to provide a cross platform library which can parse, modify and abstract ELF, PE and MachO formats.
		* **Crypter/Obfuscator**
		* **Embedding into Other Langs**
			* [Random thoughts about embedding python into your application - rewolf(2011)](http://blog.rewolf.pl/blog/?p=259)
				* In this post I want to share some of my thoughts about embedding python into C/C++ applications. It will not be yet another python tutorial, but just my personal feelings about some of the mechanisms that I’ve encountered during my work on dirtyJOE.
		* **GUI**
			* [Gooey](https://github.com/chriskiehl/Gooey)
				* Turn (almost) any Python 2 or 3 Console Program into a GUI application with one line
		* **Injection/Shellcode**
		* **Networking**
		* **PE32**
		* **Publishing**
		* **WebServer**
		* **Other**
			* [Inline C](https://github.com/georgek42/inlinec)
				* Effortlessly write inline C functions in Python
			* [Making Raw Syscalls on Windows From Python - Spencer(2017)](https://warroom.rsmus.com/making-syscalls-python/)
		* **Examples**
			* [Ares](https://github.com/sweetsoftware/Ares)
				* Ares is a Python Remote Access Tool.
			* [Pupy](https://github.com/n1nj4sec/pupy)
				* Pupy is an opensource, cross-platform (Windows, Linux, OSX, Android) remote administration and post-exploitation tool mainly written in python
			* [covertutils - A framework for Backdoor development!](https://github.com/operatorequals/covertutils)
				* This Python package is used to create Agent/Handler backdoors, like metasploit's meterpreter, empire's empire agent, cobalt strike's beacon and so on... It automatically handles all communication channel options, like encryption, chunking, steganography, sessions, etc. With a recent package addition (httpimport), staging from pure Python2/3 is finally possible! With all those set with a few lines of code, a programmer can spend time creating the actual payloads, persistense mechanisms, shellcodes and generally more creative stuff!! The security programmers can stop re-inventing the wheel by implementing encryption mechanisms both Agent-side and Handler-side to spend their time developing more versatile Agents, and generally feature-rich shells!
			* [RedSails](https://github.com/BeetleChunks/redsails)
				* Python based post-exploitation project aimed at bypassing host based security monitoring and logging. [DerbyCon 2017 Talk](https://www.youtube.com/watch?v=Ul8uPvlOsug)
			* [stupid_malware](https://github.com/andrew-morris/stupid_malware)
				* Python malware for pentesters that bypasses most antivirus (signature and heuristics) and IPS using sheer stupidity
			* [Stitch](https://github.com/nathanlopez/Stitch)
				* This is a cross platform python framework which allows you to build custom payloads for Windows, Mac OSX and Linux as well. You are able to select whether the payload binds to a specific IP and port, listens for a connection on a port, option to send an email of system info when the system boots, and option to start keylogger on boot. Payloads created can only run on the OS that they were created on.
			* [WEASEL](https://github.com/facebookincubator/WEASEL)
				* WEASEL is a small in-memory implant using Python 3 with no dependencies. The beacon client sends a small amount of identifying information about its host to a DNS zone you control. WEASEL server can task clients to execute pre-baked or arbitrary commands. WEASEL is a stage 1 payload, meant to be difficult to detect and useful for regaining access when your noisy full-featured stages are caught.
	- **Rust**<a name="rust"></a>
		* **Tradecraft**
		- **CLI**
			* https://github.com/clap-rs/clap
		* **Crypter/Obfuscator**
		* **Injection/Shellcode**
			* [asm - The Rust RFC Book](https://rust-lang.github.io/rfcs/2873-inline-asm.html)
				* "This RFC specifies a new syntax for inline assembly which is suitable for eventual stabilization."
		* **Networking**
		* **PE32**
			* [goblin](https://github.com/m4b/goblin)
				* An impish, cross-platform binary parsing crate, written in Rust
		* **Publishing**
 			* [Minimizing Rust Binary Size](https://github.com/johnthagen/min-sized-rust)
				* This repository demonstrates how to minimize the size of a Rust binary.
		* **WebServer**
		* **Other**
		* **Examples**
		* **macOS Specific**
			* [core-foundation-rs](https://github.com/servo/core-foundation-rs)
				* Rust bindings to Core Foundation and other low level libraries on Mac OS X and iOS 
		* **Windows-Specific**
			* [Rust for Windows - Kenny Kerr(2021)](https://kennykerr.ca/2021/01/21/rust-for-windows/)
			* [Rust for Windows](https://github.com/microsoft/windows-rs)
				* The windows crate lets you call any Windows API past, present, and future using code generated on the fly directly from the metadata describing the API and right into your Rust package where you can call them as if they were just another Rust module.
			* [tinywin](https://github.com/janiorca/tinywin)
				* A very small but functional Win32 apps in Rust using no_std
- **Linux Specific**<a name="linspec"></a>
	- **ELF Injection**
		* [ELFun File Injector - pico(2016)](https://0x00sec.org/t/elfun-file-injector/410)
	- **Unsorted**
		* [Zombie Ant Farm: Practical Tips for Playing Hide and Seek with Linux EDRs.](https://github.com/dsnezhkov/zombieant)
			* Zombie Ant Farm: Primitives and Offensive Tooling for Linux EDR evasion
- **macOS Specific**<a name="macspec"></a>
	- See the 'Lambert' Family of Malware for Nation-State opinions on how to do it.
	- **Articles/Blogposts**
		* [My Journey Writing A Post Exploitation Tool for macOS - Cedric Owens(2019)](https://medium.com/red-teaming-with-a-blue-team-mentaility/my-journey-writing-a-post-exploitation-tool-for-macos-d8293d51244f)
	- **Obfuscation**
		- **Tools**
			* [MachObfuscator](https://github.com/kam800/MachObfuscator)
				* MachObfuscator is a programming-language-agnostic Mach-O apps obfuscator for Apple platforms.
- **Windows Specific**<a name="winspec"></a>
	* [awesome-windows-kernel-security-development](https://github.com/ExpLife0011/awesome-windows-kernel-security-development)
	* **Hooking**
		* [Hook_API](https://github.com/EgeBalci/Hook_API)
			* Assembly block for hooking windows API functions. 
	* **IAT**
		* [IAT_API](https://github.com/EgeBalci/IAT_API)
			* Assembly block for finding and calling the windows API functions inside import address table(IAT) of the running PE file.
	* **In-Memory**
		* [Memory Resident Implants Code injection is alive and well - Luke Jennings(BlueHatv18)](https://www.youtube.com/watch?v=02fL2xpR7IM)
			* [Slides](https://www.slideshare.net/MSbluehat/bluehat-v18-memory-resident-implants-code-injection-is-alive-and-well)
		* [Hunting for Memory Resident Malware - Joe Desimone(Derbycon7)](https://archive.org/details/DerbyCon7/S21-Hunting-for-Memory-Resident-Malware-Joe-Desimone.mp4)
		* [Masking Malicious Memory Artifacts – Part I: Phantom DLL Hollowing - Forrest Orr(2019)](https://www.forrest-orr.net/post/malicious-memory-artifacts-part-i-dll-hollowing)
			* [Part 2](https://www.forrest-orr.net/post/masking-malicious-memory-artifacts-part-ii-insights-from-moneta)
		* [Moneta](https://github.com/forrest-orr/moneta)
			* Moneta is a live usermode memory analysis tool for Windows with the capability to detect malware IOCs 
	* **Installation & Update**
		* [Squirrel](https://github.com/Squirrel/Squirrel.Windows)
			* Squirrel is both a set of tools and a library, to completely manage both installation and updating your Desktop Windows application, written in either C# or any other language (i.e., Squirrel can manage native C++ applications).
	- **Obfuscation/ors**
		- **Articles/Blogposts/Writeups**
			* [Building an Obfuscator to Evade Windows Defender - Samuel Wong(2020)](https://www.xanthus.io/post/building-an-obfuscator-to-evade-windows-defender)
		- **Talks/Presentations/Videos**
			* [Evading Detection: A Beginner's Guide to Obfuscation](https://github.com/BC-SECURITY/Beginners-Guide-to-Obfuscation)
				* "This is a hands-on class to learn the methodology behind malware delivery and avoiding detection. This workshop explores the inner workings of Microsoft's Antimalware Scan Interface (AMSI), Windows Defender, and Event Tracing for Windows (ETW). We will learn how to employ obfuscated malware using Visual Basic (VB), PowerShell, and C# to avoid Microsoft's defenses. Students will learn to build AMSI bypass techniques, obfuscate payloads from dynamic and static signature detection methods, and learn about alternative network evasion methods."
		- **Tools**
	* **PE32**
		* [tinyPE](https://github.com/rcx/tinyPE)
			* Smallest possible PE files. Artisanal, hand-crafted with love and care.
		* [PE-Packer](https://github.com/czs108/PE-Packer)
			* A simple Windows x86 PE file packer written in C & Microsoft Assembly.
		* [αcτµαlly pδrταblε εxεcµταblε - Justine Alexandra Roberts Tunney(2020)](https://raw.githubusercontent.com/jart/cosmopolitan/37a4c70c3634862d8d005955c032b5a2fa8737c5/ape/ape.S)
			* [Link](https://justine.lol/ape.html)
		* [Generating Custom Cobalt Strike Artifacts with PEzor - phra(2021)](https://iwantmore.pizza/posts/PEzor3.html)
	* **Shellcode**
		* [Write Windows Shellcode in Rust](https://github.com/b1tg/rust-windows-shellcode)
			* Windows shellcode development in Rust 
		* [Writing Optimized Windows Shellcode in C - Matt Graeber(2013)](http://www.exploit-monday.com/2013/08/writing-optimized-windows-shellcode-in-c.html)
	* **Tradecraft**
		* [DLL Proxy Loading Your Favourite C# Implant - Flangvik(2020)](https://redteaming.co.uk/2020/07/12/dll-proxy-loading-your-favorite-c-implant/)
		* [Red Team Tactics: Hiding Windows Services - Joshua Wright(2020)](https://www.sans.org/blog/red-team-tactics-hiding-windows-services/)
		* [Runtime symbol resolution - Federico Lagrasta(2020)](https://offnotes.notso.pro/malware-development/function-call-obfuscation/runtime-symbol-resolution)
			* Using LoadLibraryW and GetProcAddress to avoid suspicious imports
		* [Preventing 3rd Party DLLs from Injecting into your Malware - @spottheplanet](https://www.ired.team/offensive-security/defense-evasion/preventing-3rd-party-dlls-from-injecting-into-your-processes)
		* [Hindering Threat Hunting, a tale of evasion in a restricted environment - Borja Merino(2020)](https://www.blackarrow.net/hindering-threat-hunting-a-tale-of-evasion-in-a-restricted-environment/)
		* [Fat Free Guide To Process Hollowing and Droppers - Sneakidia(2020)](https://sneakidia.blogspot.com/2020/10/fat-free-guide-to-process-hollowing-and.html)
		* [Hiding execution of unsigned code in system threads - drew(2021)](https://secret.club/2021/01/12/callout.html)
		* [dearg-thread-ipc-stealth](https://github.com/LloydLabs/dearg-thread-ipc-stealth)
			* A novel technique to communicate between threads using the standard ETHREAD structure
		* [Hiding your process from sysinternals](https://riscybusiness.wordpress.com/2017/10/07/hiding-your-process-from-sysinternals/)
		* [Universal Unhooking: Blinding Security Software - Jeffrey Tang](https://threatvector.cylance.com/en_us/home/universal-unhooking-blinding-security-software.html)
		* [You're Off the Hook: Blinding Security Software - Alex Matrosov, Jeff Tang](https://www.slideshare.net/cylance_inc/youre-off-the-hook-blinding-security-software)
		* [hide-and-seek](https://github.com/reversinghub/hide-and-seek)
			* PoC for hiding processes from Windows Task Manager by manipulating the graphic interface
	* **WinAPI**
		* **Articles/Blogposts**
			* [The Inner Workings Of Railgun - Spencer](https://warroom.rsmus.com/inner-workings-railgun/)
		* **Talks/Presentations/Videos**
			* [How Malware Can Resolve APIs By Hash - AGDC Services](https://www.youtube.com/watch?v=q8of74upT_g)
				* In this video, we will learn how to recognize a common obfuscation technique malware uses; resolving APIs by hash at run time. This technique is often used in shellcode, packers, and to thwart AV vendors. Learning to quickly recognize the technique and understand how to deal with it is an important technique to know to advance your malware analysis skills.
		* **Tools**
			* [CsWin32](https://github.com/microsoft/CsWin32)
				* A source generator to add a user-defined set of Win32 P/Invoke methods and supporting types to a C# project. 
			* [cppwin32](https://github.com/microsoft/cppwin32)
				* A modern C++ projection for the Win32 SDK	
			* [Windows-API-Hashing](https://github.com/LloydLabs/Windows-API-Hashing)
				* Windows API resolution via hashing
			* [IAT API](https://github.com/EgeBalci/IAT_API)
				* Assembly block for finding and calling the windows API functions inside import address table(IAT) of the running PE file.
			* [WinAPI-Tricks](https://github.com/vxunderground/WinAPI-Tricks)
				* Collection of various WINAPI tricks / features used or abused by Malware 			
			* [Modular Windows.h Header File](https://github.com/Leandros/WindowsHModular)
				* The Windows.h header file for the Win32 API is a behemoth of include file, adding hundreds of thousands of new macros, structs and functions. This project aims to modularize the Windows.h file, to only include what you require.
		* **WinAPI Sample collections**
			* [win32api-practice](https://github.com/EddieIvan01/win32api-practice)
				* Offensive tools written for practice purposes
			* [Random Windows API code snippets - stmxcsr](https://stmxcsr.com/micro/winapi-snippets.html)
	* **Samples of**
		* [delete-self-poc](https://github.com/LloydLabs/delete-self-poc)
			* (Windows)A way to delete a locked file, or current running executable, on disk.
		* [WSAAcceptBackdoor](https://github.com/EgeBalci/WSAAcceptBackdoor)
			* This project is a POC implementation for a DLL implant that acts as a backdoor for accept Winsock API calls. Once the DLL is injected into the target process, every accept call is intercepted using the Microsoft's detour library and redirected into the BackdooredAccept function. When a socket connection with a pre-defined special source port is establised, BackdooredAccept function launches a cmd.exe process and binds the accepted socket to the process STD(OUT/IN) using a named pipe.
	* **Examples**
		* [Windows classic samples](https://github.com/microsoft/Windows-classic-samples)	
			* This repo contains samples that demonstrate the API used in Windows classic desktop applications.
		* [WinPwnage](https://github.com/rootm0s/WinPwnage)
			* The meaning of this repo is to study the techniques. Techniques are found online, on different blogs and repos here on GitHub. I do not take credit for any of the findings, thanks to all the researchers.
* **Configurations**
	* **JSON**
		* [Jsonnet](https://jsonnet.org/)
			* A data templating language for app and tool developers. A simple extension of JSON
* **Delivery & Staging**<a name="pds"></a>
	* **Articles/Blogposts/Writeups**
		* [Windows oneliners to download remote payload and execute arbitrary code](https://arno0x0x.wordpress.com/2017/11/20/windows-oneliners-to-download-remote-payload-and-execute-arbitrary-code/)
		* [Staging over HTTPS and DNS simultaneously with Cobalt Strike and Shellter - HunnicCyber](https://blog.hunniccyber.com/staging-over-https-and-dns-simultaneously-with-cobalt-strike-2/)
			* This blog post is about how to create a binary that mimics an original signed binary, injected with both DNS and HTTPs Cobalt Strike stager shellcode, and then to deliver it via a Word Macro that uses domain fronting to request the binary from a legitimate Microsoft domain.
		* [Mark-of-the-Web from a red team's perspective - Stan Hegt](https://outflank.nl/blog/2020/03/30/mark-of-the-web-from-a-red-teams-perspective/)
		* [GospelRoom: Data Storage in UEFI NVRAM Variables](https://gist.github.com/jthuraisamy/e602d5d870230df3ce00178001f9ac16)
	* **Tools**
		* [DNSlivery](https://github.com/no0be/DNSlivery)
			* Easy files and payloads delivery over DNS.
		* [go-deliver](https://github.com/0x09AL/go-deliver)
			* Go-deliver is a payload delivery tool coded in Go.
		* [Pwndrop](https://github.com/kgretzky/pwndrop)
			*  Self-deployable file hosting service for red teamers, allowing to easily upload and share payloads over HTTP and WebDAV. 
			* [Pwndrop - Self-hosting Your Red Team Payloads - Kuba Gretzky(2020)](https://breakdev.org/pwndrop/)
		* [Satellite](https://github.com/t94j0/satellite)
			* Satellite is an web payload hosting service which filters requests to ensure the correct target is getting a payload. This can also be a useful service for hosting files that should be only accessed in very specific circumstances.
			* [Blogpost](https://posts.specterops.io/satellite-a-payload-and-proxy-service-for-red-team-operations-aa4500d3d970)
	* **File smuggling**<a name="fsm"></a>
		* **Articles/Blogposts/Writeups**
			* [Generic bypass of next-gen intrusion / threat / breach detection systems - Zoltan Balazs(2015)](https://www.mrg-effitas.com/research/generic-bypass-of-next-gen-intrusion-threat-breach-detection-systems/)
			* [HTML smuggling explained - Stan Hegt(2018)](https://outflank.nl/blog/2018/08/14/html-smuggling-explained/)
			* [Smuggling HTA files in Internet Explorer/Edge - Richard Warren(2017)](https://www.nccgroup.com/us/about-us/newsroom-and-events/blog/2017/august/smuggling-hta-files-in-internet-exploreredge/)
			* [File Smuggling with HTML and JavaScript - @spottheplanet](https://ired.team/offensive-security/defense-evasion/file-smuggling-with-html-and-javascript)
			* [Strange Bits: HTML Smuggling and GitHub Hosted Malware - Karsten Hahn(2019)](https://www.gdatasoftware.com/blog/2019/05/31695-strange-bits-smuggling-malware-github)
		* **Tools**	
			* [IronSquirrel](https://github.com/MRGEffitas/Ironsquirrel)
				* https://github.com/MRGEffitas/Ironsquirrel
			* [EmbedInHTML](https://github.com/Arno0x/EmbedInHTML)
				* What this tool does is taking a file (any type of file), encrypt it, and embed it into an HTML file as resource, along with an automatic download routine simulating a user clicking on the embedded ressource. Then, when the user browses the HTML file, the embedded file is decrypted on the fly, saved in a temporary folder, and the file is then presented to the user as if it was being downloaded from the remote site. Depending on the user's browser and the file type presented, the file can be automatically opened by the browser.
* **Keying**<a name="keying"></a>
	* **Keying**
		* **Articles**
			* [Mesh design pattern: hash-and-decrypt - rdist(2007)](https://web.archive.org/web/20200727221946/https://rdist.root.org/2007/04/09/mesh-design-pattern-hash-and-decrypt/)
			* [Bradley, hash-and-decrypt, Gauss ... a brief history of armored malware and malicious crypto - Fred Raynal(2012)](https://blog.quarkslab.com/bradley-hash-and-decrypt-gauss-a-brief-history-of-armored-malware-and-malicious-crypto.html)
			* [Keying Payloads for Scripting Languages - @leoloobeek(2017)](https://adapt-and-attack.com/2017/11/15/keying-payloads-for-scripting-languages/)
		* **Talks/Presentations/Videos**
			* [Context-Keyed Payload Encoding: Fighting The Next Generation of IDS - Dimitris Glynos(AthCon2010)](https://www.youtube.com/watch?v=mHMULvGynSU)
				* [Slides](https://census-labs.com/media/context-keying-slides.pdf)
				* [Paper](http://census.gr/media/context-keying-whitepaper.pdf)
				* Exploit payload encoding allows hiding maliciouspayloads from modern Intrusion Detection Systems (IDS). Although metamorphic and polymorphic encoding allow such payloads to be hidden from signature-based and anomaly-based IDS,these techniques fall short when the payload is being examined by IDS that can trace the execution of malicious code. Context-keyed encodingis a technique that allows the attacker to encrypt the malicious payload in such a way, that it canonly be executed in an environment (context) withspecific characteristics. By selecting an environment characteristic that will not be present during the IDS trace (but will be present on the target host), the attacker may evade detection by advanced IDS. This paper focuses on the current research in context-keyed payload encoding and proposes a novel encoder that surpasses many of the limitations found in its predecessors.
			* [Advanced Payload Strategies: “What is new, what works and what is hoax?”](https://www.troopers.de/events/troopers09/220_advanced_payload_strategies_what_is_new_what_works_and_what_is_hoax/)
				* This talk focuses on the shellcode perspective and it’s evolution. From the simplest {shell}code to the polymorphism to bypass filters and I{D|P}S (which has lots of new ideas, like application-specific decoders, decoders based on architecture-instructions, and many others), passing through syscall proxying and injection, this talk will explain how it works and how effective they are against the new evolving technologies like network code emulation, with live demonstrations. There is long time since the first paper was released about shellcoding. Most of modern text just tries to explain the assembly structure and many new ideas have just been released as code, never been detailed or explained. The talk will try to fix this gap, also showing some new ideas and considering different architectures.
			* [Genetic Malware: Designing Payloads for Specific Targets - Travis Morrow, Josh Pitts(2016)](https://www.youtube.com/watch?v=WI8Y24jTTlw)
				* [Slides](https://raw.githubusercontent.com/Genetic-Malware/Ebowla/master/Eko_2016_Morrow_Pitts_Master.pdf)
				* [Ebowla @ Infiltrate](https://downloads.immunityinc.com/infiltrate-archives/Genetic_Malware_Travis_Morrow_Josh_Pitts.pdf)
			* [Protect Your Payloads Modern Keying Techniques - Leo Loobeek(Derybcon2018)](https://www.youtube.com/watch?v=MHc3XP3XC4I)
				* Our payloads are at risk! Incident responders, threat hunters, and automated software solutions are eager to pick apart your new custom dropper and send you back to square one. One answer to this problem is encrypting your payload with key derivation functions ("keying") which leverages a variety of local and remote resources to build the decryption key. Throughout this talk I will present modern keying techniques and demo some tools to help along the way. I will start with showing how easy it is to discover attacker infrastructure or techniques in the payloads we commonly use every day. I will then quickly review how keying helps and the considerations when generating keyed payloads. Throughout the presentation many practical examples of keying techniques will be provided which can be used for typical pentests or full red team operations. Finally I will introduce KeyServer, a new piece to add to your red team infrastructure which handles advanced HTTP and DNS keying. Using unprotected payloads during ops should be a thing of the past. Let’s regain control of our malicious code and make it harder on defenders! This talk is based on the original research of environmental keying by Josh Pitts and Travis Morrow.
		* **Papers**
			* [Environmental Key Generation towards Clueless Agents - J. Riordan and B. Schneier(1998)](https://www.schneier.com/academic/archives/1998/06/environmental_key_ge.html)
				* In this paper, we introduce a collection of cryptographic key constructions built from environmental data that are resistant to adversarial analysis and deceit. We expound upon their properties and discuss some possible applications; the primary envisioned use of these constructions is in the creation of mobile agents whose analysis does not reveal their exact purpose.
			* [Strong Cryptography Armoured Computer VirusesForbidding Code Analysis: the bradley virusEric Filiol(2004)](https://hal.inria.fr/inria-00070748/document)
				* Imagining what the nature of future viral attacks might look like is the key to successfully protecting against them. This paper discusses how cryptography and key management techniques may definitively checkmate antiviral analysis and mechanisms. We present a generic virus, denoted bradley which protects its code with a very secure, ultra-fast symmetric encryption. Since the main drawback of using encryption in that case lies on the existence of the secret key or information about it within the viral code, we show how to bypass this limitation by using suitable key management techniques. Finally, we show that the complexity of the bradley code analysis is at least as high as that of the cryptanalysis of its underlying encryption algorithm.
			* [Foundations and applications for secure triggers - Ariel Futoransky, Emiliano  Kargieman, Carlos Sarraute, Ariel  Waissbein(2006)](https://dl.acm.org/doi/10.1145/1127345.1127349)
				* Imagine there is certain content we want to maintain private until some particular event occurs, when we want to have it automatically disclosed. Suppose, furthermore, that we want this done in a (possibly) malicious host. Say the confidential content is a piece of code belonging to a computer program that should remain ciphered and then “be triggered” (i.e., deciphered and executed) when the underlying system satisfies a preselected condition, which must remain secret after code inspection. In this work we present different solutions for problems of this sort, using different “declassification” criteria, based on a primitive we call secure triggers. We establish the notion of secure triggers in the universally composable security framework of Canetti [2001] and introduce several examples. Our examples demonstrate that a new sort of obfuscation is possible. Finally, we motivate its use with applications in realistic scenarios.
			* [Context-keyed Payload Encoding: Preventing Payload Disclosure via Context - 	druid@caughq.org(2008)](http://www.uninformed.org/?v=9&a=3)
			* [Malicious cryptography. . . reloaded - Eric Filiol, Fr'ed'eric Raynal(CanSecWest2008)](https://cansecwest.com/csw08/csw08-raynal.pdf)
			* [Context-keyed Payload Encoding:Fighting the Next Generation of IDS - Dimitrios A. Glynos(2010)](http://census.gr/media/context-keying-whitepaper.pdf)
			* [Impeding Automated Malware Analysis with Environment-sensitive Malware - Chengyu Song, Paul Royal, Wenke Lee(2012)](https://www.usenix.org/conference/hotsec12/workshop-program/presentation/song)
				* To solve the scalability problem introduced by the exponential growth of malware, numerous automated malware analysis techniques have been developed. Unfortunately, all of these approaches make previously unaddressed assumptions that manifest as weaknesses to the tenability of the automated malware analysis process. To highlight this concern, we developed two obfuscation techniques that make the successful execution of a malware sample dependent on the unique properties of the original host it infects. To reinforce the potential for malware authors to leverage this type of analysis resistance, we discuss the Flashback botnet’s use of a similar technique to prevent the automated analysis of its samples.
			* [Hot Knives Through Butter: Evading File-based Sandboxes - Abhishek Singh, Zheng Bu(2014)](https://www.fireeye.com/content/dam/fireeye-www/current-threats/pdfs/pf/file/fireeye-hot-knives-through-butter.pdf)
				* This report details the following categories of sandbox-evasion techniques: Human interaction—mouse clicks and dialog boxes; Configuration-specific—sleep calls, time triggers, process hiding, malicious downloaders, execution name of the analyzed files, volume information, and execution after reboot; Environment-specific—version, embedded iframes (in flash, swf, jpg files), embedded executable in an image file, and DLL loaders; VMware-specific—system-service lists, unique files, and the VMX Port
			* [Sleeping Your Way out of theSandbox - Hassan  Mourad(2015)](https://www.sans.org/reading-room/whitepapers/malicious/sleeping-sandbox-35797)
				* In recent years,the security landscape has witnessed the rise of a new breed of malware, Advanced Persistence Threat, or APT for short. With all traditional security solutions failing to address this new threat, a demand was created for new solutions that are capable of addressing the advanced capabilities of APT. One of the offeredsolutions was file-based sandboxes,asolution that dynamically analyzes files and judgestheir threat levelsbased on their behavior in an emulated/virtual environment. But security is a cat and mouse game, and malware authors are always trying to detect/bypass such measures. Some of the common techniques used by malware for sandbox evasionwill be discussed in this paper. This paperwill also analyze how to turn somecountermeasuresused by sandboxes against it. Finally, it will introduce some new ideas for sandbox evasion along with recommendationsto address them.
		* **Tools**
			* **Metasploit**
				* [Hostname-based Context Keyed Payload Encoder - Metasploit Module](https://github.com/rapid7/metasploit-framework/blob/master//modules/encoders/x64/xor_context.rb)
					* 'Context-Keyed Payload Encoder based on hostname and x64 XOR encoder.'	
			* [EBOWLA](https://github.com/Genetic-Malware/Ebowla)
				* Framework for Making Environmental Keyed Payloads
			* [keyring](https://github.com/leoloobeek/keyring)
				* KeyRing was written to make key derivation functions (keying) more approachable and easier to quickly develop during pentesting and red team operations. Keying is the idea of encrypting your original payload with local and remote resources, so it will only decrypt on the target system or under other situations.
			* [satellite](https://github.com/t94j0/satellite)
				* [Satellite: A Payload and Proxy Service for Red Team Operations - Max Harley](https://posts.specterops.io/satellite-a-payload-and-proxy-service-for-red-team-operations-aa4500d3d970)
				* Satellite is an web payload hosting service which filters requests to ensure the correct target is getting a payload. This can also be a useful service for hosting files that should be only accessed in very specific circumstances.
			* [GoGreen](https://github.com/leoloobeek/GoGreen)
				* This project was created to bring environmental (and HTTP) keying to scripting languages. As its common place to use PowerShell/JScript/VBScript as an initial vector of code execution, as a result of phishing or lateral movement, I see value of the techniques for these languages.
			* [keyserver](keyserver)
				* Easily serve HTTP and DNS keys for proper payload protection
			* [Keyring](https://github.com/leoloobeek/keyring)
				* Proper Payload Protection Prevents Poor Performance. KeyRing was written to make key derivation functions (keying) more approachable and easier to quickly develop during pentesting and red team operations. Keying is the idea of encrypting your original payload with local and remote resources, so it will only decrypt on the target system or under other situations.
			* [Spotter](https://github.com/matterpreter/spotter)
				* Spotter is a tool to wrap payloads in environmentally-keyed, AES256-encrypted launchers. These keyed launchers provide a way to ensure your payload is running on its intended target, as well as provide a level of protection for the launcher itself.
* **Storage**<a name="pstorage"></a>
	* [Cross-Site Phishing - ](https://blog.obscuritylabs.com/merging-web-apps-and-red-teams/)
	* [Windows Event Log to the Dark Side — Storing Payloads and Configurations - Mustafa(2018)](https://medium.com/@5yx/windows-event-log-to-the-dark-side-storing-payloads-and-configurations-9c8ad92637f2)
	* [Offensive Encrypted Data Storage](http://www.harmj0y.net/blog/redteaming/offensive-encrypted-data-storage/)
	* [Offensive Encrypted Data Storage (DPAPI edition)](https://posts.specterops.io/offensive-encrypted-data-storage-dpapi-edition-adda90e212ab)
* **Other(unsorted)**
	* [Virus Exchange](https://github.com/am0nsec/vx)
		* "This repository will contain the code associated with papers I'm release either on my blog or at VX-Underground."
------------------------------------------------------------------------------------------------------------------------------














































------------------------------------------------------------------------------------------------------------------------------
### <a name="simtools"></a> Simulation Tools
* **Articles/Blogposts/Writeups**<a name="sta"></a>
	* [Invoke-Adversary – Simulating Adversary Operations - Moti Bani](https://blogs.technet.microsoft.com/motiba/2018/04/09/invoke-adversary-simulating-adversary-operations/)
	* [Advanced Threat Analytics Attack Simulation Playbook - Microsoft](https://gallery.technet.microsoft.com/Advanced-Threat-Analytics-8b0a86bc)
* **Talks/Presentations/Videos**<a name="stpv"></a>
	* [Quantify Your Hunt: Not Your Parents’ Red Team - Devon Kerr, Roberto Rodriguez(2018)](https://www.youtube.com/watch?v=u_RaWTzB1wA)
		* The security marketplace is saturated with product claims of detection coverage that have been almost impossible to evaluate, all while intrusions continue to make headlines. To help organizations better understand the detection provided by a commercial or open-source technology platform, a framework is necessary to measure depth and breadth of coverage. This presentation builds on the MITRE ATT&CK framework by explaining how to measure the coverage and quality of ATT&CK, while demonstrating open-source Red Team tools and automation that generate artifacts of post-exploitation.
	* [Automated Adversary Emulation - David Hunt(BSidesCharm2019)](https://www.youtube.com/watch?v=gTGnHXgqZCo)
		* CALDERA is an open-source application designed to automate adversary emulation. With CALDERA, blue teams can create adversary profiles based on ATT&CK, unleashing them on their networks to test their vulnerability to specific techniques. Learn how to use and configure CALDERA to run a variety of tests, ranging from small scoped and heavily scripted, to AI-driven fully automated operations.
* **Adversary Simulation Tools**<a name="sast"></a>
	* **Self-Contained**
		* [Caldera](https://github.com/mitre/caldera)
			* CALDERA is an automated adversary emulation system that performs post-compromise adversarial behavior within enterprise networks. It generates plans during operation using a planning system and a pre-configured adversary model based on the Adversarial Tactics, Techniques & Common Knowledge (ATT&CK™) project. These features allow CALDERA to dynamically operate over a set of systems using variable behavior, which better represents how human adversaries perform operations than systems that follow prescribed sequences of actions.
		* [DumpsterFire](https://github.com/TryCatchHCF/DumpsterFire)
			* [Slides](https://github.com/TryCatchHCF/DumpsterFire/raw/master/CactusCon_2017_Presentation/DumpsterFire_CactusCon_2017_Slides.pdf)
			* The DumpsterFire Toolset is a modular, menu-driven, cross-platform tool for building repeatable, time-delayed, distributed security events. Easily create custom event chains for Blue Team drills and sensor / alert mapping. Red Teams can create decoy incidents, distractions, and lures to support and scale their operations. Turn paper tabletop exercises into controlled "live fire" range events. Build event sequences ("narratives") to simulate realistic scenarios and generate corresponding network and filesystem artifacts.
		* [Metta](https://github.com/uber-common/metta)
			* An information security preparedness tool to do adversarial simulation. This project uses Redis/Celery, python, and vagrant with virtualbox to do adversarial simulation. This allows you to test (mostly) your host based instrumentation but may also allow you to test any network based detection and controls depending on how you set up your vagrants. The project parses yaml files with actions and uses celery to queue these actions up and run them one at a time without interaction.
		* [Invoke-Apex](https://github.com/securemode/Invoke-Apex)
			* Invoke-Apex is a PowerShell-based toolkit consisting of a collection of techniques and tradecraft for use in red team, post-exploitation, adversary simulation, or other offensive security tasks. It can also be useful in identifying lapses in "malicious" activity detection processes for defenders as well.
		* [Red Team Automation (RTA)](https://github.com/endgameinc/RTA)
			* RTA provides a framework of scripts designed to allow blue teams to test their detection capabilities against malicious tradecraft, modeled after MITRE ATT&CK. RTA is composed of python scripts that generate evidence of over 50 different ATT&CK tactics, as well as a compiled binary application that performs activities such as file timestopping, process injections, and beacon simulation as needed.
		* [ezEmu](https://github.com/jwillyamz/ezEmu)
			* ezEmu enables users to test adversary behaviors via various execution techniques. Sort of like an "offensive framework for blue teamers", ezEmu does not have any networking/C2 capabilities and rather focuses on creating local test telemetry.
		* [PurpleSharp](https://github.com/mvelazc0/PurpleSharp)
			* PurpleSharp is a C# adversary simulation tool that executes adversary techniques with the purpose of generating attack telemetry in monitored Windows environments. Detection engineering teams can leverage this telemetry to identify gaps in visibility as well as test the resilience, improve existing and build new detection analytics.
		* [PurpleSpray](https://github.com/mvelazc0/PurpleSpray)
			* PurpleSpray is an adversary simulation tool that executes password spray behavior under different scenarios and conditions with the purpose of generating attack telemetry in properly monitored Windows enterprise environments. Blue teams can leverage PurpleSpray to identify gaps in visibility as well as test the resilience, improve existing and build new detection analytics for password spraying attacks.
		* [Leonidas](https://github.com/FSecureLABS/leonidas)
			* This is the repository containing Leonidas, a framework for executing attacker actions in the cloud. It provides a YAML-based format for defining cloud attacker tactics, techniques and procedures (TTPs) and their associated detection properties.
	* **Tooling Automation**
		* [AutoTTP](https://github.com/jymcheong/AutoTTP)
			* Automated Tactics Techniques & Procedures. Re-running complex sequences manually for regression tests, product evaluations, generate data for researchers & so on can be tedious. I toyed with the idea of making it easier to script Empire (or any frameworks/products/toolkits that provide APIs like Metasploit (RPC), Cobalt-Strike & so on) using IDE like Visual Studio Code (or equivalent). So I started to design AutoTTP. This is still very much work in progress. Test with Empire 2.2.
		* [Purple Team ATT&CK Automation](https://github.com/praetorian-code/purple-team-attack-automation)
			* Praetorian's public release of our Metasploit automation of MITRE ATT&CK™ TTPs
------------------------------------------------------------------------------------------------------------------------------



























----------------------------------------------------------------------------------------------------------------------------------
### <a name="tacticsandstats"></a> Tactics/Strategies/Methodologies
* **101**
* **Lessons Learned**<a name="vll"></a>
	* [Hillbilly Storytime - Pentest Fails - Adam Compton](https://www.youtube.com/watch?v=GSbKeTPv2TU)
		* Whether or not you are just starting in InfoSec, it is always important to remember that mistakes happen, even to the best and most seasoned of analysts. The key is to learn from your mistakes and keep going. So, if you have a few minutes and want to talk a load off for a bit, come and join in as a hillbilly spins a yarn about a group unfortunate pentesters and their misadventures. All stories and events are true (but the names have been be changed to prevent embarrassment).
	* [The hidden horrors that 3 years of global red-teaming, Jos van der Peet](https://www.youtube.com/watch?v=7z63HrEiQUY&index=10&list=PLwZycuzv10iLBFwRIWNAR-s4iuuUMRuEB)
		* My last 3 years of global reteaming in small and large organisations has shown me that there still are a lot of misconceptions about security. We all know the ‘onion’ model for layered security. While useful for the ‘defence in depth’ principle, this talk will show that in reality, rather than an onion, security is more like a pyramid. The basis is the hardware people work on (laptops etc.) and the top your business applications. In between is everything else. Operating system, network components, proxies, shares, servers and their software stack. Like any hi-rise structure, the top cannot be secure if the base is not secure. Defence in depth matters, but it can be quite trivial for attackers to sidestep certain controls to get to the data they want. Just securing your ‘crown-jewels’ is insufficient. This talk will revolve around how we have defeated security controls on various levels, ranging from the systems your end-users work on, all the way through to 2FA and 4-eye principles on critical business assets. It will talk about common misconceptions which lull companies into a false sense of security, while making life far too easy for attackers. For example the fallacy of focussing security efforts only/mostly on ‘crown jewels’ and how misunderstanding of why certain controls are put in place jeopardize corporate and client data. The talk will be supported by real-life examples
	* [Purple Team FAIL! - Jason Morrow - Derbycon2017](https://www.irongeek.com/i.php?page=videos/derbycon7/s16-purple-team-fail-jason-morrow)
		* What went wrong with the introduction of a red team discipline into fortune 1 and how the teams came together to course correct. The result has been a successful purple team that has driven the security posture forward at the world's leading retailer. This will cover some basic do's and don'ts along with new rules of engagement when integrating blue and red. 
	* [A  Year In The Red by Dominic Chell and Vincent Yiu - BSides Manchester2017](https://www.youtube.com/watch?v=-FQgWGktYtw&list=PLcgqQkap1lNrOBNCXqpPqpPAqckxv0XhP&index=23)
	* [Tips, Tricks, and Cheats Gathered from Red vs. Blue Team-Based Training - Ed Skoudis, Joshua Wright](https://www.sans.org/webcasts/tips-tricks-cheats-gathered-red-vs-blue-team-based-training-111505/success)
	* [Liar, Liar: a first-timer "red-teaming" under unusual restrictions. - Mike Loss(Kawaiicon2019)](https://www.youtube.com/watch?v=ASSjkkr4OCg)
	* [One Hundred Red Team Operations A Year - Ryan O'Horo](https://www.youtube.com/watch?v=44LMdSFmmJw&list=PLEJJRQNh3v_PF6cecq0ES2w25JtoG631g&index=6&t=0s)
	* [Adversarial Emulation - Bryson Bort(WWHF19)](https://www.youtube.com/watch?v=3lQTvQlBddw&list=PLXF21PFPPXTNXEgkUEBbRgvraxWP3c4Hr&index=4)
	* [Common Assessment Mistakes Pen Testers and Clients Should Avoid - Brent White, Tim Roberts](https://www.irongeek.com/i.php?page=videos/derbycon7/t211-common-assessment-mistakes-pen-testers-and-clients-should-avoid-brent-white-tim-roberts)
		* Penetration assessments can be a stressful time for those involved. It’s a moment where the network admins find out if the network they manage, or maybe even helped to build, holds up against simulated attacks. Or, it’s a moment as a pen tester where you can help the client and strengthen their security posture, or screw things up by making a mistake - potentially losing a client and giving your company a black eye. However, this shouldn’t be a stressful time. As a client, it is important to understand why the test is taking place and how this helps. As a pentester it is important that you know what you are doing, need to ask for and aren’t just going in blind or throwing the kitchen sink at the network. This talk is to highlight common issues that we’ve either encountered or have have been vented to about from both the penetration tester’s side of the assessment as well as the client’s side. We’d like to bring these issues to light to hopefully help ensure a more smooth assessment “experience” for all parties involved.
* **Tactics**<a name="ttactics"></a>
	* **Articles/Blogposts/Writeups**
		* [Nakatomi Space - Geoff Manaugh(2010)](https://www.bldgblog.com/2010/01/nakatomi-space/)
		* [Left and Right of Boom - Tim Malcomvetter(2019)](https://malcomvetter.medium.com/left-and-right-of-boom-ef230ed3eae3)
		* [Buying Internal Domain Access Again - Scot Berner(2019)](https://www.trustedsec.com/blog/buying-internal-domain-access-again/)
		* [Summary of Tactics, Techniques and Procedures Used to Target Australian Networks - Australian Cyber Security Center(ACSC)](https://www.cyber.gov.au/acsc/view-all-content/advisories/summary-tactics-techniques-and-procedures-used-target-australian-networks)
			* Summary of Tradecraft Trends for 2019-20 The Australian Cyber Security Centre (ACSC) investigated and responded to numerous cyber security incidents during 2019 and 2020 so far.
		* [Beware of the Shadowbunny - Using virtual machines to persist and evade detections - wunderwuzzi(2020)](https://embracethered.com/blog/shadowbunny.html)
		* [Attacking SIEM with Fake Logs - letsdefend.io(2020)](https://letsdefend.io/blog/attacking-siem-with-fake-logs/)
		* [Software Distribution Malware Infection Vector](https://dl.packetstormsecurity.net/papers/general/Software.Distribution.Malware.Infection.Vector.pdf)
		* [7DaysofRed](https://github.com/jsecu/7DaysofRed)
			* "The Purpose of 7daysofRed is for Blue Teamers to recognize common TTPs that attackers can be using and create IOCs or Yara Rules to prevent and harden their systems.Understanding the technology and understanding what an attacker may be doing to get into your network are the first steps to prevention. It is also meant for Red Teamers to learn what TTPs their tools may be using and relay them to their client or internal Blue Team to promote collabration and hardening of their networks."
	* **Talks/Presentations/Videos**
		* [88MPH Digital tricks to bypass Physical security - ZaCon4 - Andrew MacPherson(ZACon2013](https://vimeo.com/52865794)
		* [Meta-Post Exploitation: Using Old, Lost, Forgotten Knowledge - Val Smith, Colin Ames(Defcon16)](https://www.youtube.com/watch?v=swCNI1qWVCQ)
			* [Slides](https://www.defcon.org/images/defcon-16/dc16-presentations/defcon-16-valsmith_ames.pdf)
		* [Red Teaming Back and Forth 5ever - Fuzzynop(DerbyconIV)](https://www.youtube.com/watch?v=FTiBwFJQg64)
			* Whether you are on the red team, the blue team, or aspiring to either, you probably know that when it comes to penetrating a network, the scope of the engagement is non existent. I'm talking no-holds-barred penetration. No rules, no time limits, no prisoners. This talk discusses what happens when blue team meets red team and the tools, techniques, and methodology used when you don't have to play by the rules. Additional topics include 'why is red team?' and 'how many does 5ever take?'
		* [Operating in the Shadows Carlos Perez - Derbycon5](https://www.youtube.com/watch?v=NXTr4bomAxk)
		* [Passing the Torch: Old School Red Teaming, New School Tactics? - Dave McGuire, Will Schroeder(Derbycon 2014](https://www.slideshare.net/harmj0y/derbycon-passing-the-torch)
		* [Attacking EvilCorp: Anatomy of a Corporate Hack - Sean Metcalf, Will Schroeder(Derbycon2016)](http://www.irongeek.com/i.php?page=videos/derbycon6/111-attacking-evilcorp-anatomy-of-a-corporate-hack-sean-metcalf-will-schroeder)
			* With the millions of dollars invested in defensive solutions, how are attackers still effective? Why do defensive techniques seem to rarely stop or slow down even mid-tier adversaries? And is there anything the underfunded admin can do to stop the carnage? Join us in a shift to ?assume breach? and see how an attacker can easily move from a single machine compromise to a complete domain take over. Instead of "death by PowerPoint," see first-hand how a fictional corporation suffers "death by a thousand cuts." The fictional EvilCorp presents their top defensive tools and practically dares someone to attack the network. The battle of Red vs. Blue unfolds showing EvilCorp's network submit to the unrelenting attacks by an experienced adversary. When the dust settles, the Red Team looks victorious. But what, if anything, could have tipped the scales in the other direction? In this demo-heavy session (several demos are shown to demonstrate modern attack effectiveness), we showcase the latest attack techniques and ineffective defenses still used to protect companies. Defense evasion tools and techniques are detailed as well as attack detection methods. Effective mitigation strategies are highlighted and the Blue Team is provided a roadmap to properly shore up defenses that can stop all but the most determined attacker.
		* [Advanced Red Teaming: All Your Badges Are Belong To Us - DEF CON 22 - Eric Smith and Josh Perrymon](https://www.youtube.com/watch?v=EEGxifOAk48)
		* [GameOver Zeus: Badguys And Backends - Elliott Peterson, Michael Sandee, Tillmann Werner(BHUSA2015)](https://www.youtube.com/watch?v=KkEVwswqIBs)
			* This presentation will detail many of the individuals responsible for GameOver Zeus and Cryptolocker, summarize the law enforcement investigation, and highlight the novel legal processes used to wrest control of the botnet from its operators.  GameOver Zeus represents one of the most complex, and successful, law enforcement operations against cyber crime to date. The talk will highlight extensive industry and government partnerships, the many international agencies that played a part, and discuss some of the methods used by private industry and law enforcement personnel to track and identify those responsible for the malware. The investigation resulted in the highest ever reward offered for a cyber criminal: $3,000,000 for Evgeniy Bogachev.
		* [Looping Surveillance Cameras through Live Editing - Van Albert and Banks - Defcon23](https://www.youtube.com/watch?v=RoOqznZUClI)
			* This project consists of the hardware and software necessary to hijack wired network communications. The hardware allows an attacker to splice into live network cabling without ever breaking the physical connection. This allows the traffic on the line to be passively tapped and examined. Once the attacker has gained enough knowledge about the data being sent, the device switches to an active tap topology, where data in both directions can be modified on the fly. Through our custom implementation of the network stack, we can accurately mimic the two devices across almost all OSI layers. We have developed several applications for this technology. Most notable is the editing of live video streams to produce a “camera loop,” that is, hijacking the feed from an Ethernet surveillance camera so that the same footage repeats over and over again. More advanced video transformations can be applied if necessary. This attack can be executed and activated with practically no interruption in service, and when deactivated, is completely transparent.
		* [RAT Reusing Adversary Tradecraft - Alexander Rymdeko Harvey(BSides Augusta2016)](https://www.youtube.com/watch?v=v2jU8EsJMVc)
		* ['Red Team: How to Succeed By Thinking Like the Enemy' - Council on Foreign Relations - Micah Zenko(2016)](https://www.youtube.com/watch?v=BM2wYbu4EFY)
			* In "Red Team," CFR Senior Fellow Micah Zenko draws on little-known case studies and unprecedented access to red teamers to reveal the best practices, common pitfalls, and winning strategies of these modern-day Devil’s Advocates. The book shows how policymakers, business leaders, and curious minds alike, can succeed by thinking like the enemy.
		* [Detect Me If You Can Ben Ten - Derbycon7](https://www.youtube.com/watch?v=AF3arWoKfKg&index=23&list=PLNhlcxQZJSm-PKUZTYe1C94ymf0omysM3)
		* [Full Contact Recon int0x80 of Dual Core savant - Derbycon7](https://www.youtube.com/watch?v=XBqmvpzrNfs)
		* [Stupid RedTeamer Tricks - Laurent Desaulniers(NorthSec 2017)](https://www.youtube.com/watch?v=2g_8oHM0nwA&list=PLuUtcRxSUZUpv2An-RNhjuZSJ5fjY7ghe&index=11)
			* Who said that you need to be elite to be a good red teamer?  This presentation focuses on simple, easy hacks that can change the result of a red team assessment.  The 30 minute talk will cover improvements on the age old classic of dropping usb keys (35% increase in payload delivery!); how to reduce your C&C discoverabiltiy; techniques for leveraging Outlook against your victim to improve social engineering and other very simple tricks. By the end of the presentation, audience should be inspired to build upon techniques discussed in the talk and feel more confident in doing red team engagements.
		* [Modern Evasion Techniques Jason Lang - Derbycon7](https://www.irongeek.com/i.php?page=videos/derbycon7/t110-modern-evasion-techniques-jason-lang)
			* As pentesters, we are often in need of working around security controls. In this talk, we will reveal ways that we bypass in-line network defenses, spam filters (in line and cloud based), as well as current endpoint solutions. Some techniques are old, some are new, but all work in helping to get a foothold established. Defenders: might want to come to this one.
		* [Game On! Using Red Team to Rapidly Evolve Your Defenses - Joff Thyer, Pete Petersen(Derbycon7 2017)](https://www.irongeek.com/i.php?page=videos/derbycon7/t315-game-on-using-red-team-to-rapidly-evolve-your-defenses-joff-thyer-pete-petersen)
			* This talk will be an enjoyable conversation with good beer, great bourbon, and terrific friends who are reliving the journey of infosec maturity from the perspective of both a penetration testing company and their client over a three year period. Details of various engagements will be discussed along with post-mortem analysis, lessons learned, as well as resulting mitigation tactics and defensive strategies. We will discuss the outcomes at each stage of rendered service and how both client and vendor adjusted their approach to re-engage again and again. The engagement culminates in Red Team exercises that clearly demonstrate the infosec evolution of the client. The talk will leave the defensive audience with a sense of hope, a list of achievable goals, and several tactics. The red team with get a glimpse into the maw of the blue future and the value of their tradecraft. Special brief guest appearances and commentary are expected from others in the community that assisted the client along the way as well.
		* [Red Teaming Windows: Building a better Windows by hacking it - MS Ignite2017](https://www.youtube.com/watch?v=CClpjtgaJVI)
		* [Breaking Red - Understanding Threats through Red Teaming - Joe Vest, James Tubberville(2017)](https://www.youtube.com/watch?v=QPmgV1SRTJY)
		* [Abusing Webhooks for Command and Control - Dimitry Snezhkov(NorthSec2017)](https://www.youtube.com/watch?v=1d3QCA2cR8o&list=PLuUtcRxSUZUpv2An-RNhjuZSJ5fjY7ghe&index=12)
			* You are on the inside of the perimeter. And maybe you want to exfiltrate data, download a tool, or execute commands on your command and control server (C2). Problem is – the first leg of connectivity to your C2 is denied. Your DNS and ICMP traffic is being monitored. Access to your cloud drives is restricted. You’ve implemented domain fronting for your C2 only to discover it is ranked low by the content proxy, which is only allowing access to a handful of business related websites on the outside.  We have all been there, seeing frustrating proxy denies or triggering security alarms making our presence known. Having more choices when it comes to outbound network connectivity helps. In this talk we’ll present a technique to establish such connectivity with the help of HTTP callbacks (webhooks). We will walk you through what webhooks are, how they are used by organizations. We will then discuss how you can use approved sites as brokers of your communication, perform data transfers, establish almost real-time asynchronous command execution, and even create a command-and-control communication over them, bypassing strict defensive proxies, and even avoiding attribution.
		* [Your Voice is My Passport - delta zero, Azeem Aqil(Defcon26)](https://www.youtube.com/watch?v=2uoOkIUB43Q)
			* Financial institutions, home automation products, and offices near universal cryptographic decoders have increasingly used voice fingerprinting as a method for authentication. Recent advances in machine learning and text-to-speech have shown that synthetic, high-quality audio of subjects can be generated using transcripted speech from the target. Are current techniques for audio generation enough to spoof voice authentication algorithms? We demonstrate, using freely available machine learning models and limited budget, that standard speaker recognition and voice authentication systems are indeed fooled by targeted text-to-speech attacks. We further show a method which reduces data required to perform such an attack, demonstrating that more people are at risk for voice impersonation than previously thought.
		* [Detecting Blue Team Research Through Targeted Ads - 0x200b(Defcon26)](https://www.youtube.com/watch?v=wlKqyuefE1E)
			* When my implant gets discovered how will I know? Did the implant stop responding for some benign reason or is the IR team responding? With any luck they'll upload the sample somewhere public so I can find it, but what if I can find out if they start looking for specific bread crumbles in public data sources? At some point without any internal data all blue teams turn to OSINT which puts their searches within view of the advertising industry. In this talk I will detail how I was able to use online advertising to detect when a blue team is hot on my trail.
		* [Red Team Techniques for Evading, Bypassing, and Disabling MS Advanced Threat Protection and Advanced Threat Analytics - Chris Thompson(BHEU2017](https://www.youtube.com/watch?v=2HNuzUuVyv0&app=desktop)
			* [Slides](https://www.blackhat.com/docs/eu-17/materials/eu-17-Thompson-Red-Team-Techniques-For-Evading-Bypassing-And-Disabling-MS-Advanced-Threat-Protection-And-Advanced-Threat-Analytics.pdf)
			* Windows Defender Advanced Threat Protection is now available for all Blue Teams to utilize within Windows 10 Enterprise and Server 2012/16, which includes detection of post breach tools, tactics and techniques commonly used by Red Teams, as well as behavior analytics.
		* [Sniffing Sunlight - Erik Kamerling - ANYCON2017](http://www.irongeek.com/i.php?page=videos/anycon2017/102-sniffing-sunlight-erik-kamerling)
			* Laser listening devices (laser microphones) are a well understood technology. They have historically been used in the surreptitious surveillance of protected spaces. Using such a device, an attacker bounces an infrared laser off of a reflective surface, and receives the ricocheted beam with a photoreceptor. If the beam is reflected from a surface that is vibrating due to sound (his a typical background target), that sound is subsequently modulated into the beam and can be demodulated at the receptor. This is a known attack method and will be briefly discussed. However, does this principle also hold for non-amplified or naturally concentrated light sources? Can one retrieve modulated audio from reflected sunlight? The idea of modulating voice with sunlight was pioneered by Alexander Graham Bell in 1880 with an invention called the Photophone. A Photophone uses the audio modulation concept now used in laser microphones, but relied on a concentrated beam of sunlight rather than a laser to communicate at distance. Considering that Bell proved that intentionally concentrated sunlight can be used to modulate voice, we will explore under what natural conditions modulated audio can be found in reflected ambient light. Using off the shelf solar-cells and handmade amplifiers, Erik will demonstrate the use of the receiver side of a historic Photophone to identify instances of modulated audio in reflected light under common conditions.
		* [Attack Tactics 5: Zero to Hero Attack - Jordan Drysdale, Kent Ickler, John Strand(BHIS)](https://www.youtube.com/watch?v=kiMD0JFFheI)
			* Ever want to see a full attack from no access on the outside to domain takeover? Ever want to see that in under an hour?; OWA? Password Sprays? Yup!; VPNs? Remote account takeover? Yup!; Fully documented command and tool usage? Yup!; MailSniper? Absolutely!; Nmap? Obviously!; Crackmapexec? Definitely!; Cobalt Strike HTA phishing? This is the one I am most worried about :D - but we'll try anyway. So what? What's different about this webcast? We'll cover the zero (external, no access) to hero (internal, domain admin).
		* [Using blue team techniques in red team ops - Mark Bergman & Marc Smeets(BruCON 0x0A 2018)](https://www.youtube.com/watch?v=OjtftdPts4g)
			* When performing multi-month, multi-C2teamserver and multi-scenario red team operations, you are working with an infrastructure that becomes very large quickly. This makes it harder to keep track of what is happening on it. Coupled with the ever-increasing maturity of blue teams, this makes it more likely the blue team is somewhere analysing parts of your infra and/or artefacts. In this presentation we’ll show you how you can use that to your advantage. We’ll present different ways to keep track of the blue team’s analyses and detections, and to dynamically adjust your infra to fool the blue team. We will first set the scene by explaining common and lesser known components of red teaming infrastructures, e.g. dynamic redirectors, domain fronting revisited, decoy websites, html-smuggling, etc. Secondly, we’ll show how to centralize all your infrastructure’s and ops’ information to an ELK stack, leaving it open for intelligent querying across the entire infrastructure and operation. This will also help with better feedback to the blue team at the end of the engagement. Lastly, we’ll dive into novel ways of detecting a blue team’s investigation and we’ll give examples on how to react to these actions, for example by creating honeypots for the blue team.
		* [How to test Network Investigative Techniques(NITs) used by the FBI - Dr. Matthew Miller(Derbycon2018)](https://www.irongeek.com/i.php?page=videos/derbycon8/track-1-09-how-to-test-network-investigative-techniquesnits-used-by-the-fbi-dr-matthew-miller)
			* Network Investigative Techniques are used to investigate cyber criminal activities. These techniques have been used to unmask users of TOR whom are downloading illegal content from the Tor network. This talk will discuss such techniques, discuss ethical and legal issues and describe a methodology to test and verify such techniques.			
		* [Stress and Hacking: Understanding Cognitive Stress in Tactical Cyber Ops - Celeste Paul, Josiah Dkystra(BHUSA2018)](https://www.youtube.com/watch?v=YPc05_L4vf8)
			* [Slides](https://i.blackhat.com/us-18/Wed-August-8/us-18-Paul-Stress-and-Hacking.pdf)
			* [Paper](https://www.nsa.gov/portals/75/documents/news-features/news-stories/2018/measuring-stress-in-a-high-risk-environment/usenix_cybersecurity_ops_stress.pdf)
			* Hacking is a high-risk, high-reward, with a high-cost to human capital. In this session, we will talk about the effects of human factors in cyber operations and why you should care about them.
		* [Modern Red Team Tradecraft - Sajal Thomas(RedTeam VillageDefcon28)](https://www.youtube.com/watch?v=-f7B-N7yHm8)
			* "Modern attacks against complex network infrastructure highlight a massive gap between state-affiliated cyber espionage attacks and Red Teams. As Red Teams face challenges that real-world attackers do not, replicating the sophisticated threat groups becomes all the more challenging with tight engagement deadlines and report submissions. The talk aims to bridge this gap by providing insights into modern tradecraft employed by the apex predators as well as the coin-miners and ransomware authors. The talk will also discuss the unique relationship between speed and stealth during Red Team operations. Sometimes ""speed is the new stealth"" but with evolved defensive technologies that baseline behaviour of endpoints on the host and network level, slow and steady may be the way to go instead. Additionally, the talk will walk through publicly-known implant design considerations to defeat mature host and network defenses. Bleeding-edge credential harvesting techniques and the evolution of running Invoke-Mimikatz.ps1 to digging deep into C/C++ and Win32 API programming will be featured. Lastly, the evolution of a modern Red Team operator/developer/both will be discussed. The skills and mindset required to successfully complete objectives and evade defenses have changed over time. A Red Teamer must evolve to be able to inform defense better."
		* [King of the hill: nation-state counterintelligence for victim deconfliction - Juan Andres Guerrero-Saade(VirusBulletin2019)](https://www.youtube.com/watch?v=Yg2m9Y5w4MU)
			* [Paper](https://raw.githubusercontent.com/juanandresgs/papers/master/VB2019-Guerrero-Saade.pdf)
			* Cyber situational awareness is the ultimate outcome of mature threat intelligence. Though we normally think of threat intelligence as a defender’s practice, extensive study of advanced cyberespionage operations reveals that attackers are engaged in a similar activity. Defenders apply threat intelligence insights to ensure that attackers don’t gain persistent access to their enterprise machines. Similarly, attackers monitor for the presence of other threat actors to ensure that they’re the sole owners of a given victim box. While allied organizations engage in a bureaucratic process of victim deconfliction, it turns out that adversarial organizations have turned to embedding anti-virus-like techniques into their malware in order to do the same. This paper will focus on in-the-wild examples of these techniques and provide a conceptual framework for understanding adversarial deconfliction and its ramifications.
		* [Staying Off the Land: A Threat Actor Methodology - CrowdStrike(2020)](https://www.crowdstrike.com/blog/staying-off-the-land-methodology/)
		* [Red Team Tales - A short adventure into some interesting techniques - Aaron Dobie(2020)](https://www.youtube.com/watch?v=1p29rcq9DAE)
			* Aaron Dobie from KPMG presents a variety of red team techniques he has been working on over the past 6 months. This has included investigating and producing a DLL hijacking teams implant, migration of macro guardrails from the endpoint to block reverse engineering, and some basic hardware hacking.
		* [Red Team Handcuffs - Caleb McGary(BSides Seattle(2020)](https://www.youtube.com/watch?v=49hvmOAQwv4)
			* Microsoft Red Teams try and emulate attackers as much as possible with how we do our activities, aiming to provide our respective Blue Teams with an adversary that emulates a real attacker well enough to earn a name on our periodic table. For the most part this is achievable, however there are some tactics and techniques that attackers can do (and do use) that CDG SERPENT has challenges emulating. We will share what these attacks and challenges are, how we work around them, and what we are considering doing for the future. This will cover items like: Supply chain attacks that include a third-party compromise; Compromises where the blast radius cannot be controlled; Product compromises that would reach public consumers; Attacks that would cause an extended service outage; Etc.; This talk will offer specific examples of each type of attack that we wanted to do from the public space and how we replicated (or attempted to replicate) that attack internally. We will explain our thought process, how we made decisions, and what trade-offs we had to accept in the end to achieve our goals.
		* [Intelligence-led Red Teaming - Benjamin Lim(2020)](https://limbenjamin.com/articles/intelligence-led-red-teaming.html)
		* [RF for Red Team - David Switzer(BSides Tampa2020)](https://www.irongeek.com/i.php?page=videos/bsidestampa2020/track-b-03-rf-for-red-team-david-switzer)
			* "This would be an overview of RF related detections / monitoring and attacks. This would go over current Wifi attacks (both attacking clients and networks), as well as wireless attacks on mice/keyboards (both the old ""mousejack"" and more modern "Logitacker" style attacks), as well as monitoring other systems for physical attacks, such as IoT/smart devices, alarm systems and power meters. - Wifi - General overview - Network attacks - Client attacks - PMKID cracking - Mousejacking and derivatives - IoT / Smart devices - Popular Comm - Cell - Pagers - Misc - Alarm systems - Power meters" 
		* [Hacking Dumberly Redux - More Dumberer - Tim Medin(WWHF Hackin' Cast 2020)](https://www.youtube.com/watch?v=PYTm4F5AT38)
			* Tim Medin discusses the dumbest red team tricks and hacks encountered over the years. We are going to take the A out of APT (again), because so few attackers really need to use advanced techniques. We'll also discuss the simple defenses that make an attacker's life much more difficult.
		* [The 10 (Unexpected) Ways I Pwned You! - Steve Campbell(DEFCon401 2020)](https://www.youtube.com/watch?v=MYII6Zyds-c)
			* This presentation is about my experiences finding vulnerabilities on client pentests which were typically not found by vulnerability scanners and other pentesters, or were not remediated from previous assessments due to a lack of understanding the potential impact.
		* [Buckle It Up (Or Shells Die!) – Will Schroeder & Lee Christensen (SO-CON 2020)](https://www.youtube.com/watch?v=JC4_JypohcI&list=PLJK0fZNGiFU-2vFpjnt96j_VSuQVTkAnO&index=8)
			* One of the most overlooked, but we argue most important, phases of an offensive engagement is host situational awareness. The data you initially collect from a compromised host can mean the difference between detection or achieving your goal. “Everything is stealthy until someone is looking for it” - any action you take on a host is a detectable risk. The more data you’re able to gather during your situational awareness phase the better risk-based decisions you can make as the engagement progresses. In addition, situation awareness details the target environment’s landscape. This informs attackers what capabilities/techniques they can use in the environment and informs their attack strategy and plans. This talk will cover data of interest (from defensive configurations  to event log mining), methods of collection, and the interpretation of these data sources. Come strap on your Seatbelt and learn how to up your tradecraft game through data you may have been overlooking on operations.
		* [Introduction To Red Team Tooling And Opsec - Marwan El-Gendi(2022)](https://www.youtube.com/watch?app=desktop&v=ijOKZznamXM)
	* **Papers**
		* [ShadowMove: A Stealthy Lateral Movement Strategy - Amirreza Niakanlahiji, Jinpeng Wei, Rabbi Alam, Qingyang Wang, Bei-Tsei Chu(2020)](https://www.usenix.org/system/files/sec20summer_niakanlahiji_prepub.pdf)
			* Advanced Persistence Threat (APT) attacks use variousstrategies and techniques to move laterally within an enter-prise environment; however, the existing strategies and tech-niques have limitations such as requiring elevated permissions,creating new connections, performing new authentications, orrequiring process injections. Based on these characteristics,many host and network-based solutions have been proposedto prevent or detect such lateral movement attempts. In thispaper, we present a novel stealthy lateral movement strategy,ShadowMove, in which only established connections betweensystems in an enterprise network are misused for lateral move-ments. It has a set of unique features such as requiring noelevated privilege, no new connection, no extra authentication,and no process injection, which makes it stealthy against state-of-the-art detection mechanisms. ShadowMove is enabled bya novelsocket duplicationapproach that allows a maliciousprocess to silently abuse TCP connections established by be-nign processes. We design and implementShadowMoveforcurrent Windows and Linux operating systems. To validatethe feasibility of ShadowMove, we build several prototypesthat successfully hijack three kinds of enterprise protocols,FTP, Microsoft SQL, and Window Remote Management, toperform lateral movement actions such as copying malware tothe next target machine and launching malware on the targetmachine. We also confirm that our prototypes cannot be de-tected by existing host and network-based solutions, such asfive top-notch anti-virus products (McAfee, Norton, Webroot,Bitdefender, and Windows Defender), four IDSes (Snort, OS-SEC, Osquery, and Wazuh), and two Endpoint Detection andResponse systems (CrowdStrike Falcon Prevent and CiscoAMP).
* **Strategies**<a name="tstrats"></a>
	* **Articles/Blogposts/Writeups**
		* [Why Nation-State Malwares Target Telco Networks: Dissecting Technical Capabilities of Regin and Its Counterparts – Ömer Coşkun(Infiltrate2016)](https://infocon.org/cons/Infiltrate/Infiltrate%202016/slides/InfiltrateCon16-Why_NationState_Malware_Target_Telco_OmerCoskun.pdf)
	* **Talks/Presentations/Videos**
		* [Tactical Exploiation - H.D. Moore, Valsmith(Defcon15)](https://www.youtube.com/watch?v=DPwY5FylZfQ)
		* [Meta-Post Exploitation: Using Old, Lost, Forgotten Knowledge - Val Smith, Colin Ames(Defcon16)](https://www.youtube.com/watch?v=swCNI1qWVCQ)
			* [Slides](https://www.defcon.org/images/defcon-16/dc16-presentations/defcon-16-valsmith_ames.pdf)
		* [Breaking Extreme Networks WingOS: How to own millions of devices running on Aircrafts, Government, Smart cities and more - Josep Pi Rodriguez](https://www.youtube.com/watch?v=fo88O1i-Z3M)
			* Extreme network's embedded WingOS (Originally created by Motorola) is an operating system used in several wireless devices such as access points and controllers. This OS is being used in Motorola devices, Zebra devices and Extreme network's devices. This research started focusing in an access point widely used in many Aircrafts by several worldwide airlines but ended up in something bigger in terms of devices affected as this embedded operating system is not only used in AP's for Aircrafts but also in Healthcare, Government, Transportation, Smart cities, small to big enterprises... and more. Based on public information, we will see how vulnerable devices are actively used (outdoors) in big cities around the world. But also in Universities, Hotels,Casinos, Big companies, Mines, Hospitals and provides the Wi-Fi access for places such as the New york City Subway. In this presentation we will show with technical details how several critical vulnerabilities were found in this embedded OS. First we will introduce some internals and details about the OS and then we will show the techniques used to reverse engineering the mipsN32 ABI code for the Cavium Octeon processor. It will be discussed how some code was emulated to detect how a dynamic password is generated with a cryptographic algorithm for a root shell backdoor. Besides, it will be shown how some protocols used by some services were reverse engineered to find unauthenticated heap and stack overflow vulnerabilities that could be exploitable trough Wireless or Ethernet connection.
	* **Breaching the Perimeter**
		* **Talks/Presentations/Videos**
			* [Cracking The Perimeter: How Red Teams Penetrate - Dominic Chell(BSidesMCR 2018)](https://www.youtube.com/watch?v=u-MHX9-O890)
			* [Hacking Corporate Em@il Systems - Nate Power](http://www.irongeek.com/i.php?page=videos/bsidescolumbus2016/offense04-hacking-corporate-emil-systems-nate-power)
				* In this talk we will discuss current email system attack vectors and how these systems can be abused and leveraged to break into corporate networks. A penetration testing methodology will be discussed and technical demonstrations of attacks will be shown. Phases of this methodology include information gathering, network mapping, vulnerability identification, penetration, privilege escalation, and maintaining access. Methods for organizations to better protect systems will also be discussed.
			* [Traversing The Kill-Chain: The New Shiny In 2018 - Vincent Yiu - HITBGSEC 2018](https://www.youtube.com/watch?v=w1fNGOKkeSg&feature=youtu.be)
				* Long gone are the days of easy command shells through PowerShell. Defenders are catching more than ever, forcing red teamers to up their game in new and innovative ways. This presentation will explore several new OSINT sources, techniques, and tools developed to accelerate and assist in target asset discovery and profiling. We will discover how some new advances in EDR has changed the general landscape of more mature organisations, and how red team tactics and procedures have been modified to bypass certain obstacles faced. Relevant techniques will be revised, modified and made great again.
			* [Cracking the Perimeter with SharpShooter - D. Chell(HIP19)](https://www.youtube.com/watch?v=z89xNXLsXLU)
				* This talk walks through the steps of profiling an organisation to obtain the information required to create an effective SharpShooter payload, how to circumvent static analysis both on disk, in-memory and across the network, how to key payloads to evade sandboxing and a number of novel techniques for scriptlet execution using XML stylesheets, COM and application whitelisting bypasses.
* **Skills Improvement**<a name="vskill"></a>
	* [Baselining Behavior Tradecraft through Simulations - Dave Kennedy(WWHF19)](https://www.youtube.com/watch?v=DgxZ8ssuI_o)
		* With the adoption of endpoint detection and response tools as well as a higher focus on behavior detection within organizations, when simulating an adversary it's important to understand the systems you are targeting. This talk will focus on the next evolution of red teaming and how defeating defenders will take more work and effort. This is a good thing! It's also proof that working together (red and blue) collectively, we can make our security programs more robust in defending against attacks. This talk will dive into actual simulations where defenders have caught us as well as ways that we have circumvented even some of the best detection programs out there today. Let's dive into baselining behavior and refining our tradecraft to evade detection and how we can use that to make blue better.
	* [Finding Diamonds in the Rough- Parsing for Pentesters](https://bluescreenofjeff.com/2016-07-26-finding-diamonds-in-the-rough-parsing-for-pentesters/)
	* [Skills for a Red Teamer - Brent White & Tim Roberts - NolaCon 2018](https://www.youtube.com/watch?reload=9&v=Abr4HgSV9pc)
		* Want to incorporate hybrid security assessments into your testing methodology? What does going above and beyond look like for these types of assessments? How do you provide the best value with the resources and scope provided? What do some of these toolkits encompass? If you’re interested in what skills are needed for a Red-Teamer, or taking your red teaming assessments to the next level, here’s the basic info to get you started. We’ll discuss items of importance, methodology, gear, stories and even some tactics used to help give you an edge.
	* [Rethink, Repurpose, Reuse... Rain Hell - Michael Zupo](https://www.irongeek.com/i.php?page=videos/bsideslasvegas2015/cg10-rethink-repurpose-reuse-rain-hell-michael-zupo)
		* What Hacker doesn’t like james bond type gadgets? Like the all in one, one in all tool that can get you out of (or into) all sorts of jams, and is just plain cool to tinker with. Like Glitch from reboot! Well chances are you have several already at your fingertips, there are countless out there with more powerful ones arriving daily. The pace at which new wireless devices are released is blistering fast, leaving many perfectly good “legacy” devices around for testing. This talk will walk you through and further the discussion of modding these devices with readily available tools to quickly turn them into mobile hack platforms. Think PwnPad but without the $900 price tag. Going into whats worth your time and what's not. The possibilities are there if you so choose! Need all the power of your desktop or maybe just a few specific tools? Whatever your aim, this talk will point it further in the right direction
	* [Cons and Conjurers Lessons for Infiltration - Paul Blonsky(BSides Cleveland2016)](https://www.youtube.com/watch?v=jRgOVCBg_Q4)
		*  I will examine how the techniques of con artists and magicians are relevant to physical penetration testing, social engineering and infiltration. Focus is on some classic cons and basics of stage magic deception. 
	* [Red vs Blue: The Untold Chapter - Aaron Herndon, Thomas Somerville(GRRCon2018)](http://www.irongeek.com/i.php?page=videos/grrcon2018/grrcon-2018-lovelace10-red-vs-blue-the-untold-chapter-aaron-herndon-thomas-somerville)
		* This talk focuses on a single attack chain within a simulated network, jumping back and forth between teh thought process ofa  Red Teamer (Aaron) and the Blue Teamer (Tom).
	* [Red Teaming in the EDR age - Will Burgess - WWF HackFest 2018](https://www.youtube.com/watch?v=l8nkXCOYQC4)
	* [Red Team Operating in a Modern Environment: Learning to Live Off the Land - Und3rf10w](https://owasp.org/www-pdf-archive/Red_Team_Operating_in_a_Modern_Environment.pdf)
	* [Red Team Operating in a Modern Environment: Learning to Live Off the Land - und3rf10w](https://owasp.org/www-pdf-archive/Red_Team_Operating_in_a_Modern_Environment.pdf)
* **Methodologies**<a name="tmethods"></a>
	* **Articles/Blogposts/Writeups**
	* **Talks/Presentations/Videos**
		* [A Journey Into a Red Team - Charles Hamilton(2018)](https://ringzer0team.com/d/A-Journey-Into-a-RedTeam-2018.pdf)
		* [Red Team Methodology A Naked Look Jason Lang(Derbycon2019)](https://www.youtube.com/watch?v=kf829-tm0VM)
			* [Slides](https://www.slideshare.net/JasonLang1/red-team-methodology-a-naked-look-169879355)
----------------------------------------------------------------------------------------------------------------------------------

	










-------------------------------------------------------------------------------------------------------------------
### <a name="pentest"></a> Penetration Testing
* **Penetration Testing Engagements**
	* **Assumed Breach**
		* **Talks/Presentations/Videos**
			* [Assumed Breach: A Better Model for Penetration Testing - Mike Saunders(Derbycon2019)](https://www.irongeek.com/i.php?page=videos/derbycon9/3-08-assumed-breach-a-better-model-for-penetration-testing-mike-saunders)
				* The current model for penetration testing is broken. The typical scan and exploit model doesn?t reflect how real attackers operate after establishing a foothold. At the same time, most organizations aren?t mature enough to need a proper red team assessment. It?s time to start adopting the assumed breach model. In this talk, I?ll discuss techniques for assumed breach assessments that provide a better model for emulating the techniques attackers use once they?re they?ve established a foothold inside a typical network.
			* [Assumed Breach Testing - Brendan Oconnor(BSides Columbus Ohio2019)](https://www.irongeek.com/i.php?page=videos/bsidescolumbus2019/bsidescmh2019-2-04-assumed-breach-testing-brendan-oconnor)
				* OPM, Marriot, Equifax - horrible breaches made that much worse due to dwell time. Bad actors spending months or years on an organizations network without anyone noticing a thing. The controls at some of these organizations were in place, defense in depth, layered security, security awareness training - and they still to failed to protect them. The modern wisdom seems to be, despite the fact that you have a responsibility to try your best, the bad guys will always win.
			* [Assumed Breach: The Better Pen Test w/ Tim Medin - SANS HackFest & Ranges Summit 2020](https://www.youtube.com/watch?v=rgkjDHgAOVo&list=PLdVJWiil7RxoW8rBeKc0flY8bRuD3M68L&index=16)
				* Traditional penetration testing often concedes internal access to the tester, but then the tester does a lot of scanning and poking around. This is not representative of most breaches. Most breaches start with a phish and adversary effectively starts with access as one of your users on one of your systems. Are you prepared to defend? In this talk, Tim Medin will discuss the shortcomings of the traditional penetration test, and talk you through ways to deliver (and receive) a higher value penetration test.
			* [Assumed Breach:A Better Model for Pen Testing - Mike Saunders(2019)](https://www.redsiege.com/wp-content/uploads/2019/12/AssumedBreach-ABMv1.1-1.pdf)
-------------------------------------------------------------------------------------------------------------------




-------------------------------------------------------------------------------------------------------------------
### <a name="penx"></a> Pentesting X
* **AIX<a name="aix"></a>
	* **General**
		* [AIX for Penetration Testers 2017 thevivi.net](https://thevivi.net/2017/03/19/aix-for-penetration-testers/)
		* [Hunting Bugs in AIX : Pentesting writeup](https://rhinosecuritylabs.com/2016/11/03/unix-nostalgia-hunting-zeroday-vulnerabilities-ibm-aix/)
		* [Penetration Testing Trends John Strand - Derbycon6](https://www.youtube.com/watch?v=QyxdUe1iMNk)
* **Embedded<a name="embedded"></a>
	* **General**
		* [War Stories on Embedded Security Pentesting IoT Building Managers and how to do Better Dr Jared - Derbycon7](https://www.youtube.com/watch?v=bnTWysHT0I4&index=8&list=PLNhlcxQZJSm-PKUZTYe1C94ymf0omysM3)
* **Faxes, Printers, Other**
	* **Talks/Presentations/Videos**
		* [Why You Should Fear Your "mundane" Office Equipment - Daniel Romero, Mario Rivas(Defcon27)](https://www.youtube.com/watch?v=3X-ZnlyGuWc)
			*  In this talk we walk through the entire research engagement, from initial phases such as threat modelling to understand printer attack surfaces to the development of attack methodologies and fuzzing tools used to target printer-specific protocols and functions. Besides of remarking important vulnerabilities found and their respective CVE’s, proof of concept exploits showing how it is possible to gain full control of printers and all of the data they manage will be presented. This will show how to use enterprise printers as a method of persistence on a network, perhaps to exfiltrate sensitive data or support C2 persistence on Red Team engagements. We also address a number of challenges that researchers can face when performing vulnerability research on devices such as printers and how we used different techniques to overcome these challenges, working with limited to no debugging and triage capabilities. We also present mitigations that printer manufacturers can implement in order to reduce printer attack surfaces and render exploitation more difficult.
* **IBM Lotus**
	* [Domi-Owned](https://github.com/coldfusion39/domi-owned)
		* Domi-Owned is a tool used for compromising IBM/Lotus Domino servers.
* **MainFrames** <a name="main"></a>
	* [Soldier of Fortran Tumblr](https://mainframed767.tumblr.com/)
	* [Internet Mainframe Project](https://mainframesproject.tumblr.com/)
	* **101**
		* [Introduction to z/OS and IBM mainframes world and security](https://www.whitewinterwolf.com/posts/2017/10/01/introduction-to-zos-and-ibm-mainframes-world-and-security/)
		* [mainframed767 - tumblr(Soldier of Fortran)](https://mainframed767.tumblr.com/post/43170687339/shmoocon-presentation-links?is_related_post=1)
		* [Everything you wanted to know about mainframe security, pen testing and vulnerability scanning .. But were  too afraid to ask!](http://www.newera.com/INFO/SEC_12_17_2015.pdf)
		* [Introduction to the New Mainframe z/OS Basics](https://www.redbooks.ibm.com/redbooks/pdfs/sg246366.pdf)
		* [Learning the Mainframe - Kurt's Blog](https://kurthaeusler.wordpress.com/2016/11/16/learning-the-mainframe/)
		* [So, you want your own mainframe? // Hercules z/Architecture Emulator Tutorial](https://modernmainframer.com/2017/01/30/so-you-want-your-own-mainframe-hercules-zarchitecture-emulator-tutorial/)
		* [Master the Mainframe - IBM](https://www.ibm.com/it-infrastructure/z/education/master-the-mainframe)
	* **Reference**
		* [MVS Commands](http://hansen-family.com/mvs/MVS%20Commands.htm)
		* [Command reference](https://www.redbooks.ibm.com/tips/TIPS0091/tips0091.pdf)
			* This summary lists many of the commonly used commands (with  brief descriptions) for FTP and TCP/IP, as well as related z/OS,  z/VM, VSE, Linux, and VTAM commands. 
		* [TimeShare400](http://www.timeshare400.com/products/individual-accounts/)
	* **Articles/Writeups**
		* [2017 - A New Look at Mainframe Hacking and Penetration Testing v2.2](https://www.slideshare.net/rmfeio/2017-a-new-look-at-mainframe-hacking-and-penetration-testing-v22)
			* Sequel to above link
			* [Re: PenTest for Mainframe - Seclists](http://seclists.org/basics/2012/Aug/26)
		* [Reduce Risk and Improve Security on IBM Mainframes: Volume 1 Architecture and Platform Security](https://www.redbooks.ibm.com/redbooks/pdfs/sg247803.pdf)
	* **Talks/Videos/Slides**
		* [Hacking Mainframes; Vulnerabilities in applications exposed over TN3270 - Dominic White](http://www.irongeek.com/i.php?page=videos/derbycon4/t217-hacking-mainframes-vulnerabilities-in-applications-exposed-over-tn3270-dominic-white)
			* IBM System Z Mainframes are in regular use in Fortune 500 companies. Far from being legacy these systems are running an actively maintained operating system (z/OS). Applications on these often occupy roles critical to the business processes they underpin, with much of the later technology built around them, rather than replacing them. However, these systems are often bypassed by security testing due to worried of availability or assumptions about legacy. This talk will introduce you to assessing mainframe applications, which turn out to be quite similar to web applications. For this purpose we built a tool, Big Iron Recon & Pwnage (BIRP), to assist with performing such assessments. Importantly, our research uncovered a family of mainframe application vulnerabilities introduced by the TN3270 protocol. We found numerous applications, but not all, vulnerable to these flaws. Applications running within the two most popular transaction managers (CICS and IMS) as well as one of IBM’s own applications. The tool released assists with the exploitation of these flaws.
		* [From root to SPECIAL: Pwning IBM Mainframes - Philip “Soldier of Fortran” Young(Defcon22)](https://www.youtube.com/watch?v=Xfl4spvM5DI)
			* [Slides](https://www.defcon.org/images/defcon-22/dc-22-presentations/Young/DEFCON-22-Philip-Young-From-root-to-SPECIAL-Hacking-IBM-Mainframes-Updated.pdf)
			* This talk will demonstrate how to go from meeting an IBM, zSeries z/OS mainframe, getting root and eventually getting system SPECIAL, using tools that exist currently and newly written scripts. It will also show you how you can get access to a mainframe to help develop your own tools and techniques. This talk will teach you the ‘now what’ after you've encountered a mainframe, returning the balance from the ‘computing mystics’ who run the mainframe back to the community.
		* [Security Necromancy: Further Adventures in Mainframe Hacking - Soldier of Fortran and BigEndianSmalls((Defcon23))](https://www.youtube.com/watch?v=LgmqiugpVyU&feature=youtu.be)
			* [Slides](https://www.slideshare.net/bigendiansmalls/security-necromancy-publish)
			* You thought they were dead didn't you? You thought "I haven't seen a mainframe since the 90s, no one uses those anymore." Well you're wrong. Dead wrong. If you flew or drove to DEF CON your information was hitting a mainframe. Did you use credit or cash at the hotel? Doesn't matter, still a mainframe. Did you pay taxes, or perhaps call 911? What about going to the doctor? All using mainframes. At multiple points throughout the day, even if you don't do anything, your data is going through some mainframe, somewhere. 1984? Yeah right, man. That's a typo. Orwell is here now. He's livin' large. So why is no one talking about them?  SoF & Bigendian Smalls, aka 'the insane chown posse', will dazzle and amaze with feats of hackery never before seen on the mainframe. From fully breaking network job entry (NJE) and their concept of trusted nodes, to showing you what happens when you design security in the 80s and never update your frameworks. We'll demonstrate that, yes Charlie Brown, you can in fact overflow a buffer on the mainframe. New tools will be released! Things like SET'n'3270 (SET, but for mainframes!) and VTAM walker (profiling VTAM applications). Updates to current tools will be released (nmap script galore!) everything from accurate version profiling to application ID brute forcing and beyond. You'll also learn how to navigate IBM so you can get access to your very own mainframe and help continue the research that we've started!  All of your paychecks rely on mainframes in one form or another, so maybe we should be talking about it.
		* [Smashing the Mainframe for Fun and Prison Time - Phillip Young - Hacktivity2014](https://www.youtube.com/watch?v=SjtyifWTqmc)
		* [How to Embrace Hacker Culture For z/OS | Phil Young at SHARE in Seattle2015](https://www.youtube.com/watch?v=5Ra4Ehmifh4)
		* [Hacking Mainframes Vulnerabilities in applications exposed over TN3270 - Dominic White - Derbycon4](https://www.youtube.com/watch?v=3HFiv7NvWrM)
		* [Mainframes - Mopeds and Mischief; A PenTesters Year in Review - Tyler Wrightson(Derbycon4)](http://www.irongeek.com/i.php?page=videos/derbycon4/t203-mainframes-mopeds-and-mischief-a-pentesters-year-in-review-tyler-wrightson)
			* In this talk Tyler discusses the highlights from another year of penetration testing. This includes the most direct challenge he has ever received when a CSO told him ‘You wont be able to hack our mainframe’ and the steps he took to gain root access to said mainframe. Tyler will discuss several tools written during the year as well as make public releases of the unpublished tools. Tyler will also discuss the surprising failures he had and what can be learned from those failures. Filled with war stories of social engineering, physical infiltration, internal and external network penetration tests and more this talk will not only be educational but very entertaining.
		* [Learning Mainframe Hacking: Where the hell did all my free time go? - Chad Rikansrud - Derbycon5](https://www.irongeek.com/i.php?page=videos/derbycon5/stable31-learning-mainframe-hacking-where-the-hell-did-all-my-free-time-go-chad-rikansrud)
		* [Why You Should (But Don't) Care About Mainframe Security - Northsec2015 - Phillip Young](https://www.youtube.com/watch?v=YLxvrklh2tM)
		* [From root to SPECIAL - Pwning IBM Mainframes - Defcon22 - Philip Young](https://www.youtube.com/watch?v=MZDIblU9pBw)
		* [Mainframed - The Forgotten Fortress - Philip Young - BSidesLV2012](https://www.youtube.com/watch?v=tjYlXW2Dldc)
		* [Mainframed: The Secrets Inside that Black Box [Shmoocon 2013] - Philip Young](https://www.youtube.com/watch?v=KIavTQeQqSw)
		* [We hacked the gibson now what - Philip Young - Philip Young(BSidesLV2014)](https://www.youtube.com/watch?v=n_sXG0Ff2oM)
			* IBM has been touting the security of the mainframe for over 30 years. So much so, that the cult of mainframers believes that the platform is impenetrable. Just try showing how your new attack vector works and you'll be met with 101 reasons why it wouldn't work (until you prove them wrong of course). This talk will take direct aim at the cultist! Previous talks about mainframe security only got you to the front door. Leaving many asking 'great, I got a userid/password, now what?!'. That's what this talk is about: the ‘Now what’. You'll learn a few new techniques to penetrate the mainframe (without a userid/password) and then a bunch of attacks, tricks and mischief you can do to further maintain that access, find important files and really go after the mainframe. During this very Demo Heavy talk you'll learn how to take advantage of APF files, SSL key management, cgi-bin in TYooL 2014, what NJE is and why it's bad, why REXX and SETUID are dangerous and how simple backdoors still work (and will likely go undetected). 
		* [Hack the Legacy: IBM I aka AS400 Revealed - Bart Kulach(Defcon23)](https://www.youtube.com/watch?v=JsqUZ3xGdLc)
			* [Slides](https://media.defcon.org/DEF%20CON%2023/DEF%20CON%2023%20presentations/DEF%20CON%2023%20-%20Bart-Kulach-Hack-the-Legacy-IBMi-revealed.pdf)
			* Have you ever heard about the famous "green screen"? No, it's not a screensaver... Believe me, it still does exist! In many industries, although the front-end systems are all new and shiny, in the back-end they still rely on well-known, proven IBM i (aka AS/400) technology for their back-office, core systems. Surprisingly, nobody truly seems to care about the security. Even if these nice IBM heavy black boxes are directly connected to the Internet... The aim of the talk is to give you more insight in a number of techniques for performing a security test of / securing an IBM i system from perspective of an external and internal intruder. Methods like privilege escalation by nested user switching, getting full system access via JDBC or bypassing the "green screen" (5250) limitations will be presented.
		* [Not Just Evil: Hacking Mainframes with Network Job Entry - Philip Young(WWHF 2020 Virtual)](https://www.youtube.com/watch?v=gKjH7LK_rBo&list=PLXF21PFPPXTPwX8mccVIQB5THhU_paWmN&index=8)
			* The year was 2015 and i just watched a developer submit a job on a test LPAR and run the job in production. I was flabbergasted, how could one submit a job and have it run on another mainframe with out authentication? I was informed it was Network Job Entry and since that moment I made it my mission to completely understand this protocol and how you can use it to break mainframes.  Network Job Entry is how mainframes talk to one another and submit jobs between each other. You can use to manage other mainframes or submit jobs and transfer files. But what if we can pretend to be a mainframe with python? This talk will go in to a deep dive about the protocol, vulnerabilities within it, how you can use it to attack your own mainframes and how IBM is a bunch of tricky tricksters who change protocols silently so your nmap script stop working (true story). This talk will cover JES2, JCL, SNA, Network Job Entry, vulnerabilities, and how you can secure your setup. A python library will be discussed and multiple new tools using that library will be released.
	* **Tools**
		* [The Hercules System/370, ESA/390, and z/Architecture Emulator](http://www.hercules-390.org/)
			* Hercules is an open source software implementation of the mainframe System/370 and ESA/390 architectures, in addition to the new 64-bit z/Architecture
		* [Privilege escalation on z/OS](https://github.com/ayoul3/Privesc)
			* Privilege escalation tools on Mainframe
		* [Nmap Mainframe Scripts](https://github.com/zedsec390/NMAP)
			* NMAP scripts for TN3270 interaction as well as NJE. Most notably TSO User Enumeration and Brute Force. CICS transaction ID enumeration and NJE node name brute forcing.
		* [shells-payloads - Source code for SystemZ Shells / Payloads](https://github.com/zedsec390/shells-payloads)
		* [TN3270 Python Library](https://github.com/zedsec390/tn3270lib)
			* This library is a pure python implemnation of a TN3270e emulator. To test this library you can issue the command python tn3270lib.py <hostname> <port>.
		* [REXX-tools](https://github.com/zedsec390/REXX-tools)
			* Various tools in REXX
		* [NJElib](https://github.com/zedsec390/NJElib)
			* z/OS (mainframe) Network Job Entry (NJE) python library and example scripts.
		* [Privilege escalation on z/OSINT - ayoul3 github](https://github.com/ayoul3/Privesc)
			* Some scripts to quickly escalate on z/OS given certain misconfigurations.
		* [REX_Scripts](https://github.com/ayoul3/Rexx_scripts)
			* A collection of interesting REXX scripts to ease the life a mainframe pentester
* **SAP** <a name="sap"></a>
	* **101**
		* [mySapAdventures](https://github.com/shipcod3/mySapAdventures)
			* A quick methodology on testing/hacking SAP Applications for n00bz and bug bounty hunters
	* **Articles/Papers/Talks/Writeups**
		* [Perfect SAP Penetration testing. Part 3: The Scope of Vulnerability Search](https://erpscan.com/press-center/blog/perfect-sap-penetration-testing-part-3-scope-vulnerability-search/)
		* [SAP NetWeaver ABAP security configuration part 3: Default passwords for access to the application](https://erpscan.com/press-center/blog/sap-netweaver-abap-security-configuration-part-2-default-passwords-for-access-to-the-application/)
		* [List of ABAP-transaction codes related to SAP security](https://wiki.scn.sap.com/wiki/display/Security/List+of+ABAP-transaction+codes+related+to+SAP+security)
		* [Breaking SAP Portal](https://erpscan.com/wp-content/uploads/presentations/2012-HackerHalted-Breaking-SAP-Portal.pdf)
		* [Top 10 most interesting SAP vulnerabilities and attacks](https://erpscan.com/wp-content/uploads/presentations/2012-Kuwait-InfoSecurity-Top-10-most-interesting-vulnerabilities-and-attacks-in-SAP.pdf)
		* [SAP Penetration Testing Using Metasploit](http://information.rapid7.com/rs/rapid7/images/SAP%20Penetration%20Testing%20Using%20Metasploit%20Final.pdf)
		* [Assessing the security of SAP ecosystems with bizploit: Discovery](https://www.onapsis.com/blog/assessing-security-sap-ecosystems-bizploit-discovery)
	* **Exploits**
		* [SAP_exploit](https://github.com/vah13/SAP_exploit)
			* CVE-2016-2386 SQL injection; CVE-2016-2388 Information disclosure; CVE-2016-1910 Crypto issue
	* **Tools**
		* [PowerSAP](https://github.com/airbus-seclab/powersap)
			* PowerSAP is a simple powershell re-implementation of popular & effective techniques of all public tools such as Bizploit, Metasploit auxiliary modules, or python scripts available on the Internet. This re-implementation does not contain any new or undisclosed vulnerability.
		* [RFCpwn](https://github.com/icryo/RFCpwn)
			* An SAP enumeration and exploitation toolkit using SAP RFC calls
	* **Miscellaneous**
		* [pysap](https://github.com/CoreSecurity/pysap)
			* This Python library provides modules for crafting and sending packets using SAP's NI, Message Server, Router, RFC, SNC, Enqueue and Diag protocols.
* **SCADA/PLCs** <a name="scada"></a>
	* See [SCADA.md](./SCADA.md)
* **Virtual Appliances** <a name="va"></a>
	* **General**
		* [Hacking Virtual Appliances - Jeremy Brown - Derbycon2015](https://www.irongeek.com/i.php?page=videos/derbycon5/fix-me08-hacking-virtual-appliances-jeremy-brown)
			* Virtual Appliances have become very prevalent these days as virtualization is ubiquitous and hypervisors commonplace. More and more of the major vendors are providing literally virtual clones for many of their once physical-only products. Like IoT and the CAN bus, it's early in the game and vendors are late as usual. One thing that it catching these vendors off guard is the huge additional attack surface, ripe with vulnerabilities, added in the process. Also, many vendors see software appliances as an opportunity for the customer to easily evaluate the product before buying the physical one, making these editions more accessible and debuggable by utilizing features of the platform on which it runs. During this talk, I will provide real case studies for various vulnerabilities created by mistakes that many of the major players made when shipping their appliances. You'll learn how to find these bugs yourself and how the vendors went about fixing them, if at all. By the end of this talk, you should have a firm grasp of how one goes about getting remotes on these appliances.
		* [External Enumeration and Exploitation of Email and Web Security Solutions - Ben Williams](https://www.blackhat.com/docs/us-14/materials/us-14-Williams-I-Know-Your-Filtering-Policy-Better-Than-You-Do.pdf)
		* [Hacking Appliances: Ironic Exploitation Of Security Products - Ben Williams - BHEU 2013](https://www.youtube.com/watch?v=rrjSEkSwwOQ)
			* [Slides](https://www.blackhat.com/docs/webcast/07182013-Hacking-Appliances-Ironic-exploits-in-security-products.pdf)
* **Misc Tools**
	* [WinPwn](https://github.com/S3cur3Th1sSh1t/WinPwn)
		* Automation for internal Windows Penetrationtest / AD-Security 
	* [Portia](https://github.com/milo2012/portia)
		* Portia aims to automate a number of techniques commonly performed on internal network penetration tests after a low privileged account has been compromised. Portia performs privilege escalation as well as lateral movement automatically in the network

* **Sort**
	* **Routers**
		* [ASUS Router infosvr UDP Broadcast root Command Execution](https://github.com/jduck/asus-cmd)




### Unsorted
- 
	* [You’re Probably Not Red Teaming... And Usually I’m Not, Either [SANS ICS 2018] - Deviant Ollam](https://www.youtube.com/watch?v=mj2iSdBw4-0&feature=youtu.be)
* **Nation-State**
	* [Cyber crime and warfare charting dangerous waters - ifach lan amit(Defcon18)](https://www.youtube.com/watch?v=fP96-jzslco&list=UUhGDEluRG9r5kCecRAQTx_Q&index=2301)
		* [Slides](https://www.defcon.org/images/defcon-18/dc-18-presentations/Amit/DEFCON-18-Amit-Cyber-Crime.pdf)
		* [Paper](https://www.defcon.org/images/defcon-18/dc-18-presentations/Amit/DEFCON-18-Amit-Cyber-Crime-WP.pdf)
	* ["I Am Walking Through a City Made of Glass and I Have a Bag Full of Rocks" (Dispelling the Myths and Discussing the Facts of Global Cyber-Warfare) - Brucon(2009)](http://2009.brucon.org/material/infowar_Brucon09.pdf)
		* [Defcon17 Slides](https://www.defcon.org/images/defcon-17/dc-17-presentations/defcon-17-jayson_e_street-dispelling_myths_cyber-warfare.pdf)
		* There is a war being raged right now. It is being fought in your living room, in your dorm room even in your board room. The weapons are your network and computers and even though it is bytes not bullets whizzing by that does not make the casualties less real. We will follow the time line of Informational Warfare and its impact today. We will go deeper past the media hype and common misconceptions to the true facts of whats happening on the Internet landscape. You will learn how the war is fought and who is fighting and who is waiting on the sidelines for the dust to settle before they attack.
	* [Kim Jong-il and Me: How to Build a Cyber Army to Defeat the U.S. - Charlie Miller(Defcon18)](https://www.youtube.com/watch?v=IxSrn4wmjxM)
		* [Slides](https://www.defcon.org/images/defcon-18/dc-18-presentations/Miller/DEFCON-18-Miller-Cyberwar.pdf)
	* [Victor or Victim Strategies for Avoiding an InfoSec Cold War - Jason Lang, Stuart McIntosh(Derbycon 2018)](https://www.youtube.com/watch?v=9_cZ5xn-huc)
	* [Hacks Lies Nation States - Mario DiNatale](https://www.youtube.com/watch?v=nyh_ORq1Qwk)
	* [How to overthrow a Government - Chris Rock(Defcon24)](https://www.youtube.com/watch?v=m1lhGqNCZlA)
		* Direct from the mind of the guy who bought you the "I will kill you" presentation at DEF CON 23, is another mind bending, entertaining talk. This time it’s bigger and badder than before. Are you sick and tired of your government? Can’t wait another 4 years for an election? Or do you want to be like the CIA and overthrow a government overseas for profit or fun? If you answered yes to one or more of these questions than this talk is for you! Why not create your own cyber mercenary unit and invoke a regime change to get the government you want installed? After all, if you want the job done right, sometimes you have to do it yourself. Find out how over the last 60 years, governments and resource companies have been directly involved in architecting regime changes around world using clandestine mercenaries to ensure deniability. This has been achieved by destabilizing the ruling government, providing military equipment, assassinations, financing, training rebel groups and using government agencies like the CIA, Mossad and MI-5 or using foreign private mercenaries such as Executive Order and Sandline. Working with Simon Mann an elite ex SAS soldier turned coup architect who overthrew governments in Africa, Chris Rock will show you how mercenary coup tactics directly applied to digital mercenaries to cause regime changes as the next generation of "Cyber Dogs of War".
- **Supply Chain**
	* [Infecting The Embedded Supply Chain - Zach Miller, Alex Kissinger(Defcon26)](https://www.youtube.com/watch?v=XeiET4FuGjE)
		* With a surge in the production of internet of things (IoT) devices, embedded development tools are becoming commonplace and the software they run on is often trusted to run in escalated modes. However, some of the embedded development tools on the market contain serious vulnerabilities that put users at risk. In this talk we discuss the various attack vectors that these embedded development tools expose users to, and why users should not blindly trust their tools. This talk will detail a variety reverse engineering, fuzzing, exploit development and protocol analysis techniques that we used to analyze and exploit the security of a common embedded debugger.
- **Educational**<a name="vedu"></a>
	* [Playing Through the Pain? - The Impact of Secrets and Dark Knowledge - Richard Thieme(Defcon24)](https://www.youtube.com/watch?v=yGrcHhfUZDk)
		* Dismissing or laughing off concerns about what it does to a person to know critical secrets does not lessen the impact when those secrets build a different map of reality than "normals" use and one has to calibrate narratives to what another believes. The cognitive dissonance that inevitably causes is managed by some with denial who live as if refusing to feel the pain makes it disappear. But as Philip K. Dick said, reality is that which, when you no longer believe in it, refuses to go away. And when cognitive dissonance evolves into symptoms of traumatic stress, one ignores those symptoms at one's peril. But the constraints of one's work often make it impossible to speak aloud about those symptoms, because that might threaten one's clearances, work, and career. The real cost of security work and professional intelligence goes beyond dollars. It is measured in family life, relationships, and mental and physical well-being.   The divorce rate is as high among intelligence professionals as it is among medical professionals, for good reason - how can relationships be based on openness and trust when one's primary commitments make truth-telling and disclosure impossible?
	* [The Impact of Dark Knowledge and Secrets on Security and Intelligence Professionals - Richard Thieme(NSEC2017)](https://www.youtube.com/watch?v=0MzcPBAj88A&list=PLuUtcRxSUZUpv2An-RNhjuZSJ5fjY7ghe)
		* Dismissing or laughing off concerns about what it does to a person to know critical secrets does not lessen the impact on life, work, and relationships of building a different map of reality than “normal people” use. One has to calibrate narratives to what another believes. One has to live defensively, warily. This causes at the least cognitive dissonance which some manage by denial. But refusing to feel the pain does not make it go away. It just intensifies the consequences when they erupt. Philip K. Dick said, reality is that which, when you no longer believe in it, does not go away. When cognitive dissonance evolves into symptoms of traumatic stress, one ignores those symptoms at one’s peril. But the very constraints of one’s work often make it impossible to speak aloud about those symptoms, because that might threaten one’s clearances, work, and career. And whistle blower protection is often non-existent.	
	* [Manufactorum Terminatus - The attack and defense of industrial manufacturers - Noah Beddome(Derbycon2015)](https://www.irongeek.com/i.php?page=videos/derbycon5/fix-me03-manufactorum-terminatus-the-attack-and-defense-of-industrial-manufacturers-noah-beddome)
		* In the evolving threat land scape where the lines between informational and physical warfare have begun to blur, industrial manufacturers are beginning to find themselves in the cross hairs as targets of opportunity and great reward. With a large amount of industrial equipment now part of the "internet of things" its time to examine the practical concepts of attacking, assessing, and defending these entities. This talk will discuss the methods of attack, common vulnerabilities, and areas of opportunity for security improvement within industrial manufacturer technical security environment.
	* [Confessions of Really Bad SysAdmins - Andy Thompson(ShowMeCon2019](https://www.irongeek.com/i.php?page=videos/showmecon2019/showmecon-2019-07-confessions-of-really-bad-sysadmins-andy-thompson)
		* It's a common belief that SysAdmins make great Infosec professionals. Many believe this is due to their wide knowledge of software and technologies. In reality, it's because THEY KNOW WHERE THE DEAD BODIES ARE! That's right. Learn from the mistakes of real sysadmins. Witness and learn the mistakes and confessions of current and former Systems Admins.These stories were collected from my 23 years of in the trenches, handed down from one generation of sysadmin to the next, and from Twitter. :). We'll cover topics like misconfiguration of applications, circumvention of controls, and plain-old laziness have introduced countless amounts of risk to organizations . Most importantly, we'll talk about how controls can be introduced to counter Inside Risk such as this and why sharing these confessions is actually a good thing.
