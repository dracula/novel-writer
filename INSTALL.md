### [novelWriter](https://novelwriter.io/)

#### Native Theme

[As of novelWriter 2.5](https://novelwriter.io/releases/release_2_5.html#theme-additions), a Dracula GUI and syntax theme comes bundled with the software.

1. Go to Tools > Preferences
2. In the _Appearance_ section, select the **Dracula** Color theme for the GUI theme
3. In the _Document Style_ section, select the **Dracula** Document color theme for the syntax highlighting theme

The native version differs slightly from our original themes, which remain available for use as alternatives.

#### Install using Git

If you are a git user, you can install the theme and keep up to date by cloning the repo:

    git clone https://github.com/dracula/novel-writer.git

#### Install manually

Download using the [GitHub .zip download](https://github.com/dracula/novel-writer/archive/master.zip) option and unzip them.

#### Copy theme to novelWriter config directory

Copy `syntax/dracula_alt.conf`, `themes/dracula_flat.conf`, & `themes/dracula_border.conf` to the respective syntax and themes directories in the novelWriter config directory:

-   GNU/Linux: `~/.local/share/novelwriter/<syntax_or_themes>`
-   macOS: `~/Library/Application Support/novelwriter/<syntax_or_themes>`
-   Windows: `C:\Users\<your_user_name>\AppData\Roaming\novelwriter\<syntax_or_themes>`

#### Activating themes

1. Go to Tools > Preferences
2. In the _Appearance_ section, select the **Dracula Flat** or **Dracula Border** Color theme for the GUI theme
3. In the _Document Style_ section, select the **Dracula Alt** Document color theme for the syntax highlighting theme

#### Changing label colors

There is no separate config file to copy and paste into a folder. One either needs to change the settings manually in each novelWriter project or edit each project's `nwProject.nwx` file.

##### Within novelWriter

1. Go to Project > Project Settings
2. In the _Status_ Tab, select a Label, select the color box at the bottom of the menu, input the hex value, and click **Apply** for each Label
    - **Minimal** or **Custom** project:
        - New: `#44475a`
        - Notes: `#ff5555`
        - Draft: `#ffb86c`
        - Finished: `#50fa7b`
    - **Example** project:
        - New: `#44475a`
        - Notes: `#ff5555`
        - Started: `#ff5555`
        - 1st Draft: `#ffb86c`
        - 2nd Draft: `#ffb86c`
        - 3rd Draft: `#ffb86c`
        - Finished: `#50fa7b`
3. In the _Importance_ Tab, same as in step 2
    - None: `#44475a`
    - Background: `#F1FA8C`
    - Minor: `#8be9fd`
    - Major: `#ff79c6`
    - Main: `#bd93f9`

##### Editing `nwProject.nwx`

1. Go to the location of an existing novelWriter project
2. Create a backup of `nwProject.nwx` in case something breaks
3. Open `nwProject.nwx`
4. For a new **Minimal** or **Custom** project, replace the `<status>` and `<importance>` tags with:

```
    <status>
      <entry key="s3d19cf" count="5" red="68" green="71" blue="90">New</entry>
      <entry key="s215281" count="0" red="255" green="85" blue="85">Note</entry>
      <entry key="s42e692" count="0" red="255" green="184" blue="108">Draft</entry>
      <entry key="s44be75" count="0" red="80" green="250" blue="123">Finished</entry>
    </status>
    <importance>
      <entry key="if15af4" count="3" red="68" green="71" blue="90">New</entry>
      <entry key="i12d160" count="0" red="139" green="233" blue="253">Minor</entry>
      <entry key="ie85c9e" count="0" red="255" green="121" blue="198">Major</entry>
      <entry key="ife27d3" count="0" red="189" green="147" blue="249">Main</entry>
    </importance>
```

5. For a new **Example** project, same as in step 4 but using the codeblock below:

    **Important!** The `key` values may change between versions and not updating them will break the Example project's existing Label assignments. Check before pasting!

```
    <status>
      <entry key="sf12341" count="5" red="68" green="71" blue="90">New</entry>
      <entry key="sf24ce6" count="1" red="255" green="85" blue="85">Notes</entry>
      <entry key="sc24b8f" count="2" red="255" green="85" blue="85">Started</entry>
      <entry key="s90e6c9" count="6" red="255" green="184" blue="108">1st Draft</entry>
      <entry key="sd51c5b" count="1" red="255" green="184" blue="108">2nd Draft</entry>
      <entry key="s8ae72a" count="0" red="255" green="184" blue="108">3rd Draft</entry>
      <entry key="s78ea90" count="0" red="80" green="250" blue="123">Finished</entry>
    </status>
    <importance>
      <entry key="ia857f0" count="5" red="68" green="71" blue="90">None</entry>
      <entry key="icfb3a5" count="2" red="139" green="233" blue="253">Minor</entry>
      <entry key="i2d7a54" count="2" red="255" green="121" blue="198">Major</entry>
      <entry key="i56be10" count="1" red="189" green="147" blue="249">Main</entry>
    </importance>
```
