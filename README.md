# webusb-playground
- https://github.com/geryb-bg/gery-web/tree/master/blog/WebUSB/Example/code
- https://github.com/geryb-bg/webusb
- https://github.com/maarten-pennings/WebUSB-LED
- https://docs.nordicsemi.com/bundle/ncs-1.4.2/page/zephyr/samples/subsys/usb/webusb/README.html
- https://medium.com/@gerybbg/webusb-by-example-b4358e6a133c
- [**michalin/Android_UsbIO: Example app to control FT232 over USB**](https://github.com/michalin/Android_UsbIO/tree/main)
```
navigator.usb.addEventListener("connect", (event) => {
  console.log("Device connected:", event.device);
  // Update UI or perform actions related to the connected device
});
navigator.usb
  .requestDevice({ filters: [{ vendorId: 0x1C4F, productId: 0x002}] })
  .then(async (device) => {
    console.log(device.productName); // "Arduino Micro"
    console.log(device.manufacturerName); // "Arduino LLC"
const listen = async () => {
debugger;
  const result = await device.transferIn(3, 64);
  const decoder = new TextDecoder();
  const message = decoder.decode(result.data);
  const messageParts = message.split(' = ');
  if (messageParts[0] === 'Count') {
    deviceHeartbeat.innerText = messageParts[1];
  } else if (messageParts[0] === 'Button' 
             && messageParts[1] === '1') {
    
    deviceButtonPressed.innerText = new Date()
             .toLocaleString('en-ZA', {
               hour: 'numeric',
               minute: 'numeric',
               second: 'numeric',
             });
  }
    await device.open();
  await listen();
};
  })
  .catch((error) => {
    console.error(error);
  });
```
