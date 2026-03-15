# tmux - terminal multiplexer

sudo apt install tmux

ctrl+b is the prefix key

written in documentation as C-b



### detach session

ctrl+bd

### attach / re-attach

tmux a

attaches to most recent session


tmux has three laters

1. session

tmux new -s bob

starts new session with name bob

tmux ls

list session

tmux a -t 0

attaches to specified session, can be index or name

tmux kill-session [-t session index|name]

kills the tmux session, most recent or as specified when using -t switch

2. window

[session] 0:bash*

session window

split window horizontally

ctrl+b%

split window vertically
ctrl+b"


selecting windows

ctrl+b+cursor

ctrl+bq - followed by number matching desired window


re-sizing

ctrl+b+cursor

keep ctrl down, tap cursor to move

for larger increments, ctl+b+alt+cursor


select layouts

(ctrl+b)+(alt+n)

i.e. press ctrl plus b, release, press alt + num, where num is 1 to 5


ctl+b c

create new window

ctrl+b n

switch through windows

ctl+b ,

rename window


ctl+b w

move between sessions/windows

ctl+b x 

kill session as selected, either after ctl+b w, or when in a pane

kill current window

ctl+b &



copy mode

first edit your ~/.tmux.conf as follows

set -g mouse on
setw -g mode-keys vi

kill tmux sessions (all of them)

tmux kill-server

then create a new session, as normal

tmux

enable copy mode

ctrl+b [

move with cursor

press space to start selection

enter to finish

