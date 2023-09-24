### [novelWriter](https://novelwriter.io/)

#### Install using Git

If you are a git user, you can install the theme and keep up to date by cloning the repo:

    git clone https://github.com/dracula/novel-writer.git

#### Install manually

Download using the [GitHub .zip download](https://github.com/dracula/novel-writer/archive/master.zip) option and unzip them.

#### Copy theme to novelWriter config directory
Copy `syntax/dracula.conf`, `themes/dracula.conf`, & `themes/dracula_alt.conf` to the respective syntax and themes directories in the novelWriter config directory:

* GNU/Linux: `~/.local/share/novelwriter/<syntax_or_themes>`
* macOS: `~/Library/Application Support/novelwriter/<syntax_or_themes>`
* Windows: `C:\Users\<your_user_name>\AppData\Roaming\novelwriter\<syntax_or_themes>`

#### Activating theme

1. Go to Tools > Preferences
2. In the *General* Tab, select the **Dracula** or **Dracula Alt** GUI theme
3. In the *Highlighting* tab, select the **Dracula** syntax highlighting theme

#### Changing label colors

There is no separate config file to copy and paste into a folder. One either needs to change the settings manually in each novelWriter project or edit each project's `nwProject.nwx` file.

##### Within novelWriter

1. Go to Project > Project Settings
2. In the *Status* Tab, select a Label, click **Color**, input hex value, and click **Save** for each Label
	* **Minimal** or **Custom** project:
		- New: `#44475a`
		- Notes: `#ff5555`
		- Draft: `#ffb86c`
		- Finished: `#50fa7b`
	* **Example** project:
		- New: `#44475a`
		- Notes: `#ff5555`
		- Started: `#ff5555`
		- 1st Draft: `#ffb86c`
		- 2nd Draft: `#ffb86c`
		- 3rd Draft: `#ffb86c`
		- Finished: `#50fa7b`
3. In the *Importance* Tab, same as in step 2
	* None: `#44475a`
	* Minor: `#8be9fd`
	* Major: `#ff79c6`
	* Main: `#bd93f9`

##### Editing `nwProject.nwx`

1. Go to the location of an existing novelWriter project
2. Create a backup of `nwProject.nwx` in case something breaks
3. Open `nwProject.nwx`
4. For a new **Minimal** or **Custom** project, replace the `<status>` and `<importance>` tags with:
```
    <status>
      <entry key="sc23dcb" count="5" red="68" green="71" blue="90">New</entry>
      <entry key="sa5bc93" count="0" red="255" green="85" blue="85">Note</entry>
      <entry key="sa4dc09" count="0" red="255" green="184" blue="108">Draft</entry>
      <entry key="sccbbbb" count="0" red="80" green="250" blue="123">Finished</entry>
    </status>
    <importance>
      <entry key="i1b9bd9" count="3" red="68" green="71" blue="90">New</entry>
      <entry key="i375425" count="0" red="139" green="233" blue="253">Minor</entry>
      <entry key="iaae736" count="0" red="255" green="121" blue="198">Major</entry>
      <entry key="i4207ac" count="0" red="189" green="147" blue="249">Main</entry>
    </importance>
```

5. For a new **Example** project, same as in step 4 but using the codeblock below:

	**Important!** The `key` values may change between versions and not updating them will break the Example project's existing Label assignments. Check before pasting!
```
    <status>
      <entry key="sf4fb66" count="5" red="68" green="71" blue="90">New</entry>
      <entry key="s61a90c" count="1" red="255" green="85" blue="85">Notes</entry>
      <entry key="s4b5bd5" count="2" red="255" green="85" blue="85">Started</entry>
      <entry key="s40ee5b" count="6" red="255" green="184" blue="108">1st Draft</entry>
      <entry key="s569406" count="1" red="255" green="184" blue="108">2nd Draft</entry>
      <entry key="sfc557a" count="0" red="255" green="184" blue="108">3rd Draft</entry>
      <entry key="s715de7" count="0" red="80" green="250" blue="123">Finished</entry>
    </status>
    <importance>
      <entry key="i7560ff" count="5" red="68" green="71" blue="90">None</entry>
      <entry key="ib7f90e" count="2" red="139" green="233" blue="253">Minor</entry>
      <entry key="i8632bb" count="2" red="255" green="121" blue="198">Major</entry>
      <entry key="ie81f49" count="1" red="189" green="147" blue="249">Main</entry>
    </importance>
```
