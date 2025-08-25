# dirmap
A directory mapping tool that can output a user-friendly or xml directory mapping to the console or to a specified directory to be saved at.

## NOTICE
This tool requires you to make a file executable nad make a symlink to your system PATH. It should go without saying that you should trust none of the code I have in this repository. Please read through my code and ONLY clone and set this tool up if you have verified you trust the code I wrote. Obviously, I have not written malicious code, but you should trust no one, ever. Stay safe.

## How to use?
These only work for OSX, if you use Windows, this likely will not work. If you figure out how to use this on Windows, please shoot me an email with the instructions, or make an issue and PR.<br>

1. Install using git clone

2. Make the dirmap file executable<br>
```chmod +x dirmap```

3. Make a symlink to make it callable from the terminal (you can add it to your system path, but that is not necessary so I would advise against it)<br>
```sudo ln -s /path/to/your/dirmap /usr/local/bin/dirmap```

4. Now that the tool is ready to go, you can use it as such<br>
```dirmap /path/to/target/directory // Custom Directory```<br>
```dirmap . // Current Directory``` 

5. To specify a custom save location<br>
```dirmap /path/to/target/directory -s /absolute/path/to/<desired_filename>.xml```

6. To save user-friendly version as a text file instead of xml<br>
```dirmap /path/to/target/directory -s -u /absolute/path/to/save.xml```

7. To save it to desktop, simply do not specify a location<br>
```dirmap /path/to/target/directory -s```<br> or <br>
```dirmap /path/to/target/directory -s -u```

## Sample Usage and Output
```dirmap .```<br><br>
Scanning: /Users/.../dirmap<br>
Maximum directory depth: 5 levels<br>

Directory Structure:<br>
├── 📄 README.md<br>
└── 📄 dirmap

<br>

```dirmap . -s -u```<br><br>
Directory Map: /Users/.../dirmap<br>
Generated on: ... ...<br>
===================================================<br>
├── 📄 README.md<br>
└── 📄 dirmap<br>
