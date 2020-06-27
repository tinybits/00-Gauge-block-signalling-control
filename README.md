# 00-Gauge-block-signalling-control
micromite based control of model railway signalling based on UK Network Rail main line practices
The idea is to use a Maximite to set up train routings. Points and corresponding signals are pre-allocated according to the route to be followed.
This data is then downloaded over I2C bus to various micromite controllers used to locally drive the points motors (SG90 servos) and either semaphore
arm signals or 4-lamp signals depending on where they are on the layout.  In some locations the 4 lamp signals will be facing away from the control postion
so the person operating the system cannot set them.  Semaphors also driven by the SG90 servos.  28 pin Micromites have 5 servo outputs per device.
The micromites can also sense trains passing using optical beams to count vehicle passings into and out of a block section.  British Rail used treadle operated wheel counters but model trucks are very light and easily derailed by encountered items in the track hence the optical approach.
The micromites can report back over I2C the block occupancy for the maximite to display track status and train locations on its screen.
