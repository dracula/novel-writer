### [novelWriter](https://novelwriter.io/)

#### Install using Git

If you are a git user, you can install the theme and keep up to date by cloning the repo:

    git clone https://github.com/bvout/novelwriter-dracula.git

#### Install manually

Download using the [GitHub .zip download](https://github.com/bvout/novelwriter-dracula/archive/master.zip) option and unzip them.

#### Copy theme to novelWriter config directory
On most UNIX-based systems the following should work:

	mkdir -p ~/.config/novelWriter/syntax && cp novelWriter/dracula.conf ~/.config/novelWriter/syntax/dracula.conf

	mkdir -p ~/.config/novelWriter/themes && cp novelWriter/dracula.conf ~/.config/novelWriter/themes/dracula.conf

If that does not work on your machine, manually copy syntax/dracula.conf & themes/dracula.conf to the respective syntax and themes directories in the novelWriter config directory:

Windows: C:\Users<your_user_name>\AppData\Roaming\novelWriter\<syntax_or_themes>
Windows portable mode: <your_novelWriter_portable_folder>\data\<syntax_or_themes>
GNU/Linux: ~/.config/novelWriter/<syntax_or_themes>
macOS: ~/Library/Application Support/novelWriter/<syntax_or_themes>

#### Activating theme

1. Go to Tools > Preferences
2. Select Dracula GUI theme in General Tab
3. Select Dracula syntax highlighting theme in Highlighting tab
