# go-app-config

##Easy to use config helper for golang application

###Write the code:

import (
  "https://dpr-gitlab.otr.ru/go/go-app-config"
)

paramL := config.Local.Get("param")  // get params from ./config/{start arg}.conf
paramL := config.Global.Get("param") // get params from ./config/global.conf


###Create the config file in the config dir( ./config ):

> ./config/dev.conf
> ./config/global.conf

param:  somevalue

###Run the apllication

./yourApp   -  run in default mode (dev.conf)

./yourApp  prod  - run with prod.conf

./yourApp  xyz  - run with xyz.conf


P.S. don't use other runtime arguments :(