# Change Docker Bridge IP (BIP)

Useful when Docker's default subnet conflicts with your existing network ranges.

Edit `/etc/docker/daemon.json`:

```json
{
  "bip": "172.20.0.1/24",
  "default-address-pools": [
    {
      "base": "172.20.0.0/16",
      "size": 24
    }
  ]
}
```

Then restart Docker:

```bash
sudo systemctl restart docker
```
