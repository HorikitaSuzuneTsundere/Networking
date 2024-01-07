Router> ~~~ this is the user executive mode

Router>enable ~~~ privilege executive mode

//if already in privilege mode
type 'show ip int br'
type 'show run' ~~~ show the running configuration

type 'conf t' ~~~ to enter global configuration mode

//if already in global mode ~~~ Router(config)#
type 'hostname RouterA' ~~~ to change router name
type 'banner motd # This is a secure network! #' ~~~ to put message
type 'enable password nameofpassword' ~~~ to set password in privilege mode
type 'enable secret nameofpassword'

//next process is
type 'line console 0'
type 'password nameofpassword'
type 'login'
type 'exit'

// second process is
type 'line vty 0 4'
type 'password nameofpassword'
type 'login'
type 'exit'

//encrypt all passwords
type 'service password-encryption'

//goto global mode ~~~ Router(config)#
type 'int fa 0/0'
type "ip add 'gateway' 'subnet mask' "
type 'no shut'

// (IF) setting serial
type 'clock rate 56000'

type 'exit'

//last step at privilege executive mode
type 'copy run start'
