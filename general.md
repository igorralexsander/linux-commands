# General commands

## Watch cpu clock
`watch -n1 vcgencmd measure_clock arm`

## Watch temperature
`watch -n1 vcgencmd measure_temp`

## Loop for into command line
`for cont in $(seq 1 10); do curl http://localhost:8080; done`