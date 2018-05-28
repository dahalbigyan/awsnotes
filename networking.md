
Hardwares: Host 1 --- n Routers --- Host 2

Layer 5 ==== Application === Data
Layer 4 ==== Transport === Segment
Layer 3 ==== Network   === Datagram
Layer 2 ==== DataLink  === Frame

As frame goes from the router to router frame header changes, the IP header is looked at, but never changes.

- Transport and data headers are not even looked by routers
- Transport layer + Application Layer is called the end to end layers as they are only looked upon by the end point hosts.
- Network and DataLink layers are called host to host layers. 
