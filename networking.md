
Hardwares: Host 1 --- n Routers --- Host 2
- Hosts have IP address + mac address
- Routers(Default gateway)
    - They have multiple IP addresses + mac addresses(each for an interface)

Layer 5 ==== Application === Data
PORT PORT PORT PORT PORT PORT
Layer 4 ==== Transport === Segment
Layer 3 ==== Network   === Datagram
Layer 2 ==== DataLink  === Frame

As frame goes from the router to router frame header changes, the IP header is looked at, but never changes.

- Transport and data headers are not even looked by routers
- Transport layer + Application Layer is called the end to end layers as they are only looked upon by the end point hosts.
- Network and DataLink layers are called host to host layers.
