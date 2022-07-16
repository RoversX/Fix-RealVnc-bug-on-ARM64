# Fix-RealVnc-bug-on-ARM64
<br>

## Suitable for developboard and arm64 device

Bug like this:
![_2022-06-11_12-0-34.png](https://pic.iqy.ink/i/2022/06/11/62a4a4bf4302c.png)
![6-11_212-16-37.png](https://pic.iqy.ink/i/2022/06/11/62a4a4bf70b43.png)

Useful for Ubuntu and Manjaro (I tried)

To solve the problem, you need to bring <code>libbcm_host.so.0</code> <code>libvchiq_arm.so.0</code> <code>libvcos.so.0</code> to <code>usr/lib</code>

After that Run these to let software activate:

```
sudo systemctl start vncserver-x11-serviced.service

sudo systemctl enable vncserver-x11-serviced.service

sudo vnclicensewiz
```

DONE.

File from /usr/lib/aarch64-linux-gnu/ (on ubuntu22.04 raspberry4 8G) 
