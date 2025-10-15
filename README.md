# config file for tmux 
## this config file works only for current user

## you can directly copy the config file to `~/` as `~/.tmux.conf` and inside `tmux` shell source the file `tmux source-file ~/.tmux.conf` 

OR 

## make it yourself according to the modification you need  
`nano ~/.tmux.conf`

```

###split view                
#Ctrl+Alt+z splits horizontally
bind -n C-M-z split-window -v  
###Ctrl+Alt+x splits vertically
bind -n C-M-x split-window -h   
                                

##navigation 
              
###Ctrl+Alt+o
#move to down panel
bind -n C-M-o select-pane -D
                            
###Ctrl+Alt+p              
#move to left panel        
bind -n C-M-p select-pane -L
                            
###Ctrl+Alt+a                        
#move to up panel                    
bind -n C-M-a select-pane -U           
                                        
###Ctrl+Alt+s                         
#move to right panel                  
bind -n C-M-s select-pane -R           

```

### then open tmux
`tmux`

### inside tmux terminal
`tmux source-file ~/.tmux.conf`

Basically all we don't need all four navigation key combo at the same place all we need is left/right + up/down combo, cause when are at the left most terminal and move tries to move to left panel tmux sends us to right panel same for up/down as well, the cursor actually rotates vertically as well horizontally.





__________________________________________________________________________________________________________________________________
### meaning of the keys
###bind -n C-M-z split-window -v                                                                                                    
                                                                                                                                  
bind   ->	Tells tmux               : “bind a key to a command.”                                                               
-n     -> 	Means no prefix          : don’t need Ctrl+B first; just press the key combo directly.                            
C-M-z	                             : The key combination Ctrl+Alt+Z (C = Ctrl, M = Meta/Alt).                                   
split-window                         :	The tmux command to split the current pane.                                               
-v    ->	Vertical split           : creates a new pane below the current one.(Horizontal is -h)                            
###Effect: Pressing Ctrl+Alt+Z immediately splits the current pane horizontally (new pane appears below) without needing a prefix.  
__________________________________________________________________________________________________________________________________




# "when an idea or thought pops in mundane moment always work on it" 
