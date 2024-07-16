# Kali-Linux-essentials

## Tmux.conf
First install 
```
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```
then add these plugins
```
# List of plugins

set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'tmux-plugins/tmux-logging'

# Initialize TMUX plugin manager (keep at bottom)
run '~/.tmux/plugins/tpm/tpm'
```
After creating this config file, we need to execute it in our current session, so the settings in the .tmux.conf file take effect. We can do this with the source command.
```
tmux source ~/.tmux.conf 
```
Once in the session, type [Ctrl] + [B] and then hit [Shift] + [I] (or prefix + [Shift] + [I] if you are not using the default prefix key), and the plugin will install (this could take around 5 seconds to complete).

##### TIPS
Once the plugin is installed, start logging the current session (or pane) by typing [Ctrl] + [B] followed by [Shift] + [P] (prefix + [Shift] + [P]) to begin logging. If all went as planned, the bottom of the window will show that logging is enabled and the output file. To stop logging, repeat the prefix + [Shift] + [P] key combo or type exit to kill the session. Note that the log file will only be populated once you either stop logging or exit the Tmux session.

## .Zshrc
First do a backup for original .zshrc file that you have right now.
```
cp ~/.zshrc ~/.zshrc.bak
```
