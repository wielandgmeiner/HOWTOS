## Get bitcoin.pdf from the bitcoin blockchain in one line

```
bitcoin-cli getrawtransaction 54e48e5f5c656b26c3bca14a8c95aa583d07ebe84dde3b7dd4a78f4e4186e713  | sed 's/0100000000000000/\n/g' | tail -n +2 | cut -c7-136,139-268,271-400 | tr -d '\n' | cut -c17-368600 | xxd -p -r > bitcoin.pdf
```
