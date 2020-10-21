# CVE-2020-16938

`CVE-2020-16938` is a vulnerability that allows you to get unrestricted file read capabilities on the entire disk as unprivileged user. The bug was originally found and reported by my friend [Jonas](https://twitter.com/jonasLyk/status/1316104870987010048). His PoC can be found [here](https://twitter.com/jonasLyk/status/1316104870987010048).

My version of the exploit consists of a bunch of Windows API calls to get the handle directly without using 7zip, the PoC can be found in the `poc` folder which mirrors the [tweet](https://twitter.com/layle_ctf/status/1316108167609188354) I created a while ago.

In short, this exploit allows you to dump the entire disk. The dump in itself can be opened using 7zip or any other parser that supports NTFS.

![](/image/poc.png)

