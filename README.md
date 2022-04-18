# pyTSISP003

This project aims to become an at least partial Python implementation of the "Communications Protocol for Roadside Devices" (TSI-SP-003) of Roads and Maritime Services NSW, including the "VicRoads Extensions to RTA Protocol For Roadside Devices (TCS 060–1–2012)".

This project is curently in the planning stage.

## Documentation

### Master to controller via serial port

~~~python
import pyserial
import tsisp003

conn = pyserial.Serial(...)
master = tsisp0003.Connection(conn, AUTH)
~~~
The master can send application level packets to the controller and receive the responses. All application packets 
~~~python
request = tsisp003.TODO()
response = master.send(address, packet)
assert respons.SOMETHING = SOMETHING
~~~
The master will automatically re-establish the connection ...

### Application packets

## Links

* [TSI-SP-003 Communications Protocol for Roadside Devices](https://roads-waterways.transport.nsw.gov.au/business-industry/partners-suppliers/documents/specifications/tsi-sp-003.pdf)
* [TCS 060–1–2012 VicRoads Extensions to RTA Protocol For Roadside Devices](https://www.vicroads.vic.gov.au/-/media/files/technical-documents-new/its-specifications-tcs/specification-tcs-060--vr-extensions-to-rta-protocol.ashx)
