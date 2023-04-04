- [https://chaos.projectdiscovery.io/#/](https://chaos.projectdiscovery.io/#/)

- Amass:
```
amass enum -passive -norecursive -noalts -df list-domains.txt -o subs.txt
amass enum -passive -norecursive -noalts -d domain -o subs.txt
amass enum -passive -d DOMAIN -cidr CIDR -asn ASN
```

- assetfinder + findomain + subfinder
```
findomain -f {list} -q | anew {output}
cat {list} | assetfinder --subs-only | anew {output}
subfinder -dL {list} -silent | anew {output}
```

