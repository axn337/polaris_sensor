# Polaris_indigo

# Need Serial: https://github.com/RANHAOHR/serial.git

If you plan to access the Polaris Vicra from a non-root user account, you will need to add the

user account to the “lock” group. It may also be necessary to add the user account to the

following groups:

uucp

tty

dialout

# Please run:
'sudo usermod -G group_name account_name' 
# for the above three groups

# To run the node for mutiple rom files:
'rosrun polaris_sensor polaris_sensor_node _roms:="$(rospack find polaris_sensor)/rom/kuka.rom,$(rospack find polaris_sensor)/rom/T0.rom" _port:=/dev/ttyUSB0'
