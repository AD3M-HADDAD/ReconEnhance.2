# ReconEnhance

ReconEnhance is an efficient tool for network reconnaissance that utilizes multiple threads to carry out partially automated enumeration of services. Its purpose is to save time during CTFs and penetration testing scenarios, such as OSCP. 

To begin, the tool conducts port scans and service detection scans, but only after obtaining explicit permission from the user. Based on the initial findings, the tool proceeds to conduct additional enumeration scans on the identified services, utilizing various tools with the user's explicit consent. For instance, if HTTP is detected, feroxbuster, along with several others, will be launcheed, given that the user grants permission.

## Origin

ReconEnhance was inspired by two tools : [AutoRecon](https://github.com/Tib3rius/AutoRecon) and [SemiAutoRecon](https://github.com/Tib3rius/SemiAutoRecon). While all both tools were useful, none of them alone had the functionality desired. ReconEnhance combines the best features of the aforementioned tools while also implementing many new features to help testers with enumeration of multiple targets.

## Features

* Prompts the user before executing any command.
* Supports multiple targets in the form of IP addresses, IP ranges (CIDR notation), and resolvable hostnames. IPv6 is also supported.
* Advanced plugin system allowing for easy creation of new scans.
* Customizable port scanning plugins for flexibility in your initial scans.
* Customizable service scanning plugins for further enumeration.
* Suggested manual follow-up commands for when automation makes little sense.
* Ability to limit port scanning to a combination of TCP/UDP ports.
* An intuitive directory structure for results gathering.
* Full logging of commands that were run, along with errors if they fail.
* A powerful config file lets you use your favorite settings every time.
* A tagging system that lets you include or exclude certain plugins.
* Global and per-target timeouts in case you only have limited time.
* Four levels of verbosity, controllable by command-line options, and during scans using Up/Down arrows.
* Colorized output for distinguishing separate pieces of information. Can be turned off for accessibility reasons.
* A user-friendly graphical interface (GUI) to assist users in comprehending the outputs.

###Verbosity 

ReconEnhance supports four levels of verbosity:

* (none) Minimal output. ReconEnhance will announce when scanning targets starts / ends.
* (-v) Verbose output. ReconEnhance will additionally announce when plugins start running, and report open ports and identified services.
* (-vv) Very verbose output. ReconEnhance will additionally specify the exact commands which are being run by plugins, highlight any patterns which are matched in command output, and announce when plugins end.
* (-vvv) Very, very verbose output. ReconEnhance will output everything. Literally every line from all commands which are currently running. When scanning multiple targets concurrently, this can lead to a ridiculous amount of output. It is not advised to use -vvv unless you absolutely need to see live output from commands.

Note: You can change the verbosity of ReconEnhance mid-scan by pressing the up and down arrow keys.

### Results

By default, results will be stored in the ./results directory. A new sub directory is created for every target. The structure of this sub directory is:

```
.
├── exploit/
├── loot/
├── report/
│   ├── local.txt
│   ├── notes.txt
│   ├── proof.txt
│   └── screenshots/
└── scans/
	├── _commands.log
	├── _manual_commands.txt
	├── tcp80/
	├── udp53/
	└── xml/
```

The exploit directory is intended to contain any exploit code you download / write for the target.

The loot directory is intended to contain any loot (e.g. hashes, interesting files) you find on the target.

The scans directory is where all results from scans performed by SemiAutoRecon will go. This includes port scans / service detection scans, as well as any service enumeration scans. It also contains two other files:
* \_commands.log contains a list of every command ReconEnhance ran against the target. This is useful if one of the commands fails and you want to run it again with modifications.
* \_manual_commands.txt contains any commands that are deemed "too dangerous" to run automatically, either because they are too intrusive, require modification based on human analysis, or just work better when there is a human monitoring them.

By default, directories are created for each open port (e.g. tcp80, udp53) and scan results for the services found on those ports are stored in their respective directories. You can disable this behavior using the --no-port-dirs command line option, and scan results will instead be stored in the scans directory itself.

