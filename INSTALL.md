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
    - Background: `#f1fa8c`
    - Minor: `#8be9fd`
    - Major: `#ff79c6`
    - Main: `#bd93f9`

##### Editing `nwProject.nwx`

1. Go to the location of an existing novelWriter project
2. Create a backup of `nwProject.nwx` in case something breaks
3. Open `nwProject.nwx`
4. For a new **Fresh** or **Custom** project, replace the `<status>` and `<importance>` tags with:

    **Important!** The `key` values for new projects may change between versions and not updating them will break any of the Fresh/Custom project's existing Label assignments. Check before pasting!

```
    <status>
      <entry key="sf99c9b" count="23" red="68" green="71" blue="90" shape="SQUARE">New</entry>
      <entry key="sc95fc9" count="0" red="255" green="85" blue="85" shape="SQUARE">Note</entry>
      <entry key="s12c26e" count="0" red="255" green="184" blue="108" shape="SQUARE">Draft</entry>
      <entry key="s7ee763" count="0" red="80" green="250" blue="123" shape="SQUARE">Finished</entry>
    </status>
    <importance>
      <entry key="ie17778" count="4" red="68" green="71" blue="90" shape="SQUARE">New</entry>
      <entry key="i3ce947" count="0" red="139" green="233" blue="253" shape="SQUARE">Minor</entry>
      <entry key="ifed6e3" count="0" red="255" green="121" blue="198" shape="SQUARE">Major</entry>
      <entry key="ic449c2" count="0" red="189" green="147" blue="249" shape="SQUARE">Main</entry>
    </importance>
```

1. For a new **Example** project, same as in step 4 but using the codeblock below:

    **Important!** The `key` values for new projects may change between versions and not updating them will break the Example project's existing Label assignments. Check before pasting!

```
    <status>
      <entry key="sf12341" count="8" red="68" green="71" blue="90" shape="SQUARE">New</entry>
      <entry key="sf24ce6" count="2" red="255" green="85" blue="85" shape="SQUARE">Notes</entry>
      <entry key="sc24b8f" count="3" red="255" green="85" blue="85" shape="BARS_1">Started</entry>
      <entry key="s90e6c9" count="5" red="255" green="184" blue="108" shape="BARS_2">1st Draft</entry>
      <entry key="sd51c5b" count="1" red="255" green="184" blue="108" shape="BARS_3">2nd Draft</entry>
      <entry key="s8ae72a" count="1" red="255" green="184" blue="108" shape="BARS_4">3rd Draft</entry>
      <entry key="s78ea90" count="1" red="80" green="250" blue="123" shape="STAR">Finished</entry>
    </status>
    <importance>
      <entry key="ia857f0" count="5" red="68" green="71" blue="90" shape="SQUARE">None</entry>
      <entry key="i4a1d39" count="1" red="241" green="250" blue="140" shape="BLOCK_1">Background</entry>
      <entry key="icfb3a5" count="1" red="139" green="233" blue="253" shape="BLOCK_2">Minor</entry>
      <entry key="i2d7a54" count="2" red="255" green="121" blue="198" shape="BLOCK_3">Major</entry>
      <entry key="i56be10" count="1" red="189" green="147" blue="249" shape="BLOCK_4">Main</entry>
    </importance>
```
