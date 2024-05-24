# BSides

12-13/abril/2024

## A backdoor into my heart

Speaker Michael, hendler v3ga

Outdated technology is still being used. The people that made it are dead.

He is a threat actor, not a pentester. Pentesting stops where the threat starts. He emulates an adversary. He proves concepts by simulating the adversary.

Using AI to assist in the solution of a CVE is good but understand it is a double edged sword. You should only use it on small snippets of code that you can 100% understand.

Not exactly how he said it: "Windows by itself, when its off its fine, but when you turn it on that's when it becomes a problem."

### Interesting Concepts

Un pana con something that looks like the DIY laptop LTT made a video on.
- Dynamic Proxy 
Dynamic proxy for undetected access?
- SBOM - Software Bill Of Materials
The SBOM does not accuarately convey anything. The materials listed do not help in identifying threats, vulnerabilities or modifications/tuning.
- Bash Bunny
Used to recover/crack passwords.
- LLMNR
- PCI card connected to motherboard for direct access to memory, essentially bypassing bit locker and many other forms of protections.
- RUST 
Memory safe, used defensively.
- C# 
Also memory safe?

## Guardians of Healthcare Shielding IoMT from cyber threats

I forgot to note down the speaker, see the schedule for friday at 1335 in breakout 1.

IoMT - Internet of Medical Things.

She did corporate security if I remember correctly.

IoMT, it came to stay. More secure and standardization through interoperability. Ideally everything should have sinergy, from the moment the patient comes in, everything should be secure, standardized and interoparable.

Some patients have to be connecected to many different devices, and they have to work together and securely.

Regulatiors, they don't talk to each other and that causes problems since they are saying different things and manufacturers have to adapt to all of them.

The responsability should not be entirily reliant on the patients.

Sometimes the priorities are jumbled and the industry does not protect what it already has, and instead opt for new or better tech.

The security experts have to go and meet how they are working for.

## Breaking Barriers Safely: Mastering Physical Penetration Testig in Healthcare Security

Disclusure: you are responsible for your actions. It is your responsability either take advantage or be taken advatage of.

Speaker started as IT. 

One of the few certified CISSP.

Some hospitals leave doors unlocked.

Recently there was a hack that stopped the emition of Rx in PR and USA.
Some people claim that they were updating the tech and that's why they were down.

Before starting a pentest:
1. Understand the engagement. If you take PHI data in any shape or form, you are now liable for that data.
1. Who will do the engagement. In USA, the PHI data can only be taken and held by US citizens and on US soil.
1. You need the authorization letter and all the required documents. In the case you get caught you must know what to give, what to say, and all the details, otherwise you will have a very bad time. The company does not always want to tell that a pentest will be conducted. Even when you are conducting a pentest, there are limits, you HAVE TO KNOW THEM AND NOT VIOLATE THEM, otherwise you will loose your engagement.

The engagement that you do today, can probably blow up in the future.

What are the requirements of the engagement? Some just require that you take pictures to have evidence that you were where you said you were.

Phishing attacks are incredibly easy.

You have consider the fact that you might get fucked.

Tactics:
-Social engineering
The employees must be trained to challeng and to not let go to be more secure.

Cases:
- Social engineering
- Electronic access
There are usually a lot of services that protect against this type of access. In PR however, this tends to not be implemented or implemented well.

Windows 2000 - running MRI machines today. You can use it to see your personal emails.

Most exploits and penetrations are done due to lack patching.

Access control strats:
- Piggy back - fit in and follow someone who has access. You should look like you belong.
- Pretend your access does not work. Again, you have to look like you belong.

What of you get caught?
- Have the documents in hand.
- Have the get out of jail free card.
- You might also want to use your real name, but just not say where you work.
- You have to make them assume, so that they fuck up.

### Interesting Concepts

- CISSP
- PHI
This has to be protected.
- Network Injector
- Key logger
- Pendrive and load it with remote access
- Devices that detect things like pinapple wifi and attacks it so that the pineapple cannot post the SSID and hurt enviroment.

## Red Team vs Blue Team

Primer inte medical device hacking. You can use against any kind of device. Medical devices are not special in any way.

Be fluent on our feet, use all your skills and change what you are trying to do to see if you find anything.

Aparentemente el pana has some 0 day vulnerabilities. He open to talk.

Somethings to have if you want to ocmpromise medical devices:
- Wireshark
- TCPdump
- Ettercap
- BurpSuite
- Lan Tap 
- Switch with Port Mirroring
- Crossover Cable - this has been phased out, but still useful.
- Lock picking kit
- SDR 

Start small, have a broad skillset, use it all.

[v3gahax's github course](https://github.com/v3gahax/BSidesPR_Course)

If you run python script on your linux host you will be sending codes to the server. You need to intercept and modify, then send it back. After that, you have effectively killed the patient.

Unencrypted traffic happens or reasons like: UDP, interoperability. To make things interoperable you lower the bar and make sure everything works.

Windows, embedded or real time operating systems.

If you don't see a lot of traffic, you can just MITM it. That way you can force things to go to you.

hl7 is incredibly easy to crack. You can you just modify the packet and as long as it looks simar enough it will accepted. So a simple python script is enough to send fake data.

SAMBA or SAMDA uses port 445 i think. This means that if you can look out for that. This is also an unprotected, or not really gaurded port. You can exploit the communication of that port.

Kiosk, yes, a literal kiosk where somethings are displayed. Very easy to break. You can use:
- FlipperZero
- BashBunny
- USB Rubber Ducky
- Ducky Scripting

The kiosk escape: you can easily escape the kiosk and enter the OS? by using: different keystrokes(usually ones that have to do with accesibility settings).
Escape teh kiosk through context menus.
Sometimes kiosks just launch web server in full screen mode. 
Account pivoting.
You can just play around with the kiosk to escape and break the machine.
After you escape the kiosk, you can start exploiting.

DICOM has a 128 byte stub. You can add anything you want. You can write code and effectively do an RCE. You can do RCE as long as your code is less than 128 bytes with a binary null terminator I think.

Applocker Bypasses:
- C windows tasks
- DLL's
- Third party execution - if you see extra languages installed, you can get a shell a bypass.


### Interesting Concepts

- DLL proxying code
- Alternative Data Streams - you hide the file behind something and unless you open it the right way, you can't access the file.
- Non-emulated API's - a way to determine if the system is running a protection scripts.
- hexbeast

Get on disk, execute the payload, make a proxy, get off disk, and now you have access to system and if you do other things they can't see you.

## DevSecOps

The course is inside the course folder of the repo. This is the [repo link](https://github.com/tweag/bsides-pr-devsecops-2024).
What is DevSecOps? Intefrating security in the DevOps processes. Improve the speed of the dev process since the security is already integrated in the pipeline.

Shifting Left: Moving security earlier in the process.

IDE plug-ins are the first line of defense.

OWASP Top 10 is useful to see what's going on.
Copilot is a copilot not an autopilot.

Use .gitignore whenever possible, sometimes you might accidentally commit ssh keys, secrets, and many more sensitive information.

If you manage an enterprise and you manage the process, you can automate the process using a REST API.

You can scan for secrets with github native tooling:
github->code security and analyisis->secret scanning
You can add costume platforms to scan for secrets of unsupported platforms.

You can set it up to automatically contact the person in charge of security instead of making the f-up public.

If your organization is using templated repositories, you can make all the security pipelines, rules and scans, ahead of time.

If there is a costume reporting tool, if the tool generates the output in the correct format you can also use that other tool.


Software Bill Of Materials (SBOMs)
I think github supports them out of the box I think. You can make it so that everytime you commmit to main, you are also generating an SBOM.
You should always want to make SBOMs be a part of every release?
The goverment requires SBOMs to prove that your code is not riddled with vulnerabilities and outdated software.

The horusec output can placed as json in the github, if I remember correctly.
Horusec can be added to the security pipeline in github.

The SBOM is pretty much a huge json object.

How to learn about enterprise tooling without being in an enterprise?
Use microsoft learn. The learning resources are free but the test(certification) is not. It has great github resources that will prepare you well in github actions and branch rules.



### Intersting Concepts

- SDLC
- Horusec
Can be run locally in docker, or remotely I think.
- Talisman
Pre-commit hook suite. I think this is only for github.
- Branch protection rules
Prevent the merge of secrets or any other sensitive information. You can specify the specific people that MUST review the code before the branch/pull_erquest is merged. I think this needs a licence.
- Static Analysis (SAST)
Multiple language support, allows for costume queries/query packs. Executes as a gating mechanism in your CI/CD pipeline.
- Dependency Vulnerability
There are tools to scan for vulnerabilities that are intrinsic to the depency being used. These tools also grab the vulnerabilities in the dependency inside the dependency inside the...
  - Dependabot is one such tool. It creats a pull request to fix the issue?! This is pretty cool.
- Checkov 
Its free I think. Somehting about infrastructures as a code and also for, or as?, container definations.

For a copy of the presentation: `andy.dennis@moduscreate.com`.

## State of the offensive ML Union

A machine learning model is a full blown program, which means that it can contain malware.
This mallware may be impercievable to users. 
You do not need to know anything about ML to attack it.
Machine learning models can contain executable binaries.
This makes it ripe for supply chain attacks.

How to make someone run a mallicious model?
- Machine learning people soruce models from Hugging Face. This is just like github for ML models. So they don't really evaluate it. It is important to note that analyzing a model is extremely difficult, so the developers do not eveluate the models.
- Now remember that the data those models are going to be trained on critical business data.
- Also remember that these developers are expected to experiment quickly. So security is not a priority.
- Tools like kubernetes, containers and more that are used.
- Hugging Face allows to register the orginazatoin of the organization you want to pretend to be. Some characters like i and l look similar.
- Some people just join the fake company space, or sometimes even request to join. Alternatively, you can just invite the  employees(the emil will come from Hugging Face, so it does not look suspicious). Then the employees start uploading company data.
- Now we can deploy our attack.
- Using Lambda Model we can hide our malware.
- The file does not look suspiciously big. It is usually very well hidden.
- The most likely phase the attack will execute will be in training and data? phase.
- Post exploitation:
  - Using reverse shells can cause the access to crash, since these methods are hacking methods adn not official methods.
  - There are a lot of costume tooling and sensitive data that you will have access to.
  - Since these enviroments are highly costumized, you might get lost.
  - Many model tools are actually very insecure since they are very new, very experimental and are expected to be used in very secure locations.
  - Now for poissoning:
    - Some allignment tools can be run remotly. Now you effectively changed the behaviour of a built model. These tools are written in plain english, so they are very easily to use.
- Clam AV is used to protect. It is not very good, it caps are like a couple gigs, but most models are huge, and it doesn't even really scan the files.
- Defensive tools can used offensively. They don't seem to know that though.

### Interesting Concepts

- Hugging Face
Its like github for ML models.
- Lambda Layer
You can make them passthrough so that they don't affect the calculations of the model.

### Resources

- https://wiki.offsecml.com/Welcome+to+the+Offensive+ML+Playbook
- https://wiki.offsecml.com/Offensive+ML/Phishing/Avoiding+phishing+webpage+detectors+via+black+box+ML
- https://www.elastic.co/jp/blog/opening-machine-learning-black-box-model-interpretability
- https://wiki.offsecml.com/Welcome+to+the+Offensive+ML+Playbook
- https://5stars217.github.io/2023-08-08-red-teaming-with-ml-models/


## Using containers to analysis malware at scale

This workshop is not designed to learn mallware analysis. Pero estamos aqui para aprender y sufrir.
Wifi del centro de convenciones:
ssid: obsidis
password: 6pe,$S88

About the speaker:
  - AUSCF - Association of US Cyber Force, included AUSA membership.
  - CompSecDirect
  - twitch jfersec

Kleared4 - you can sign up for 1$, I think. This site offers many more courses.

Mallware - a pretty broad term.

The industry got really good at virtual machines. Consequently malware authors got really good at deteting virtual enviroments.

Buying baremetal is cheaper today. Some free tools are depricated.

Ideally we want to automate the malware analysis, this is because we want to do it at scale.

Instead of uploading the malware sample, we upload a hash so that the attacker does not know we have their malware.

What does the malware do?
What architecture is it for?
What does it need to execute?
  Some malware does not even run on baremetal. You can modify to run on a virtual enviroment or get the cheap baremetal. Some need a specific driver.

AWS tends to be very cheap. The expensive part of cloud is high computation power.

Where do you find malware?
- Virus total, but you have to negotiate, they are not cheap, and they are inconsistent.
- Malware-bazaar does let you download malware freely. This is not divided, meta info is missing, and just pulls everything from the previous day. Running another command we can get all the missing data, and we can have more information on what we have.

Where will we execute this?
It really depends, but it all leads back to where the fuck will we run this?
We have to analyze the risks.
Can I?
Can we?
At home, cloud, baremetal lab?
Who are the providers? Where they located? Who owns them?

Executing:
- Scripted execution
- Remote managers
- Async calls

Containers are really just the BSD jails that were there since the 90s. They are sandboxed. They do not store anything by default.

How do we submit things for analysis?
- USB?
- Can we automate it? Some may still require manual labor.
- We want to make sure the results are accurate, we can't blindly trust the workflow.
- It needs to be fast.
- We need to be sure we actually saving time.


To analyze malware with malware daily, all you need is a compatible version of python.

Containers by default are configured unsafely, they allow interactions with system, especially when the user is part of the docker group.

To be safer, you should make volumes instead of mount points since it reduces the attack surface.

`docker info` gives information about the host.

Volumes can be pretty much anything, there are exotic configs that use samda shares or other types of file/folder/drive shares.

The shells in docker behave very wierdly. Bien trambolicos.

There are commands for parallelism.

You can commit docker image states or at least docker images(I think it saves the state but am not sure).

### Interesting Concepts

- PXE boots
- Anti memory forensics
- Virtual enviroment detection
- Virus Total
- malware-bazaar
- malwaredaily.py
To get the malware samples published the day before.
- C2 - command and control
- jpcert teaches or has ways to analyze malware.
- yara to make yara rules for malware samples.
  - yara?
  - yarGen?
- parallel
Linux tools for making various process at the same time. Tiene un syntax trambolico.


## Notes to self

Make the nextcloud server, start taking notes with obsidian or whatever for the love of god. Having notes and resources specifically make for you is really advantagious and makes learning new things easier and it doubles as a knowledge base.

