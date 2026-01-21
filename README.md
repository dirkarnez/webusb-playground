# webusb-playground
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
