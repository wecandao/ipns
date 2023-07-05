# <img src="wecando.svg" alt="WeCanDO" height="120px">
# IPFS Name Service Resolver

### _Are you tired of encountering the "504 Gateway Time-out" error from ipfs.io and dweb.link ?_

To access your IPNS name, just use URL https://your-ipns-hash.ipns.surf

### How to save and publish a webpage to IPFS and IPNS?

#### 1. Start your IPFS daemon:
```
# ipfs daemon
```

#### 2. Create an example.html file on your local disk.

#### 3. Store your file on IPFS:
```
# ipfs add --cid-version 1 example.html
```
It will return a CID (hash) for this version of the file. You can access your file through the following URL: https://ipfs.io/ipfs/your-cid 
```
Example output:
added bafkreibvqu2vgcvyjlrwrqxldelrcr3mug45xrv56qcjfhwans66pa4jlm example.html
```
Where "bafkreibvqu2vgcvyjlrwrqxldelrcr3mug45xrv56qcjfhwans66pa4jlm" is the CID of your file.
You can use the following URLs to access your file:

https://ipfs.io/ipfs/bafkreibvqu2vgcvyjlrwrqxldelrcr3mug45xrv56qcjfhwans66pa4jlm
or
https://bafkreibvqu2vgcvyjlrwrqxldelrcr3mug45xrv56qcjfhwans66pa4jlm.ipfs.dweb.link
#### 4. Publish your link to IPNS:
```
# ipfs name publish /ipfs/cid-of-your-file
```
It will return the hash of the IPNS record for your file. You can use this hash as a **subdomain of ipns.surf**
```
Example output:
Published to k51qzi5uqu5dipo4719isofxynwutbh3zdhhtqbfgqcp3sr4gxarf2vsniqtnq: /ipfs/bafkreibvqu2vgcvyjlrwrqxldelrcr3mug45xrv56qcjfhwans66pa4jlm
```
Where "k51qzi5uqu5dipo4719isofxynwutbh3zdhhtqbfgqcp3sr4gxarf2vsniqtnq" is the hash of your IPNS record for this file.
#### Example of the IPNS URL:
#### https://k51qzi5uqu5dipo4719isofxynwutbh3zdhhtqbfgqcp3sr4gxarf2vsniqtnq.ipns.surf
_Afterwards, you can use this URL permanently on any web pages, messengers, or wherever you need this file._

#### 5. To update your file, run the "add" command again to obtain a new CID:
```
# ipfs add example.html
```
#### 6. Publish the new version of your file:
```
# ipfs name publish /ipfs/new-cid-of-your-file
```

#### 7. _The latest version of your file will always be accessible through the IPNS URL that you obtained in STEP 4._

#### Enjoy! ;)
