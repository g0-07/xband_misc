# How to prepare your XBAND modem for serial-only connection:

1. **! Carefully !** lift pin 18 (TXD) and pin 29 (RXD) on the rockwell modem IC and connect wires to the lifted pins. They are needed to restore modem functionality if needed.

    ![fs_001](https://user-images.githubusercontent.com/37120278/200299754-c1e4fe74-9bf8-4724-8336-9760c4eb45da.png)

2. Connect a wire on pin 29 on the FRED IC. This wire will be the RX pin for serial connection (For me it was easier to avoid soldering under the lifted pins.)

    ![fs_002](https://user-images.githubusercontent.com/37120278/200302563-2f42f008-6fd7-4159-bba5-1b03b6f36b24.png)

3. Connect a wire on the solder pad above the R10 label. This wire will be the TX pin for serial connection.

    ![fs_003](https://user-images.githubusercontent.com/37120278/200306359-3723e15f-45fd-48b5-a921-eca58cbf037e.png)

4. Connect a wire for example on the battery ground pad.

    ![fs_004](https://user-images.githubusercontent.com/37120278/200307764-e92c061d-0d47-47a8-83b1-b7d7cec75c6d.png)

5. Connect the wires to a pin header, correct ordering gives the possibility to add a jumper on RX and TX to get modem funcionality back.

    ![image](https://user-images.githubusercontent.com/37120278/200310006-239061cd-ba35-40f2-a647-91ad43045cb9.png)

6. Replace the ROM with a flash ROM which contains the FredSerial firmware. You can use [xband_sak](https://github.com/g0-07/xband_sak) to flash a AM29F400BB/BT.

7. Fix everything, for example with hot glue.

    ![image](https://user-images.githubusercontent.com/37120278/200310231-a6fa69fb-a571-423b-aaad-82c0d1672b6f.png)
