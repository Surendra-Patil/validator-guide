# Chihuahua v4.0.0 Upgrade

The Upgrade is scheduled for block `4787878`. A countdown clock is [here](https://www.mintscan.io/chihuahua/blocks/4787878)

This guide assumes that you use cosmovisor to manage upgrades

```bash
# get the new version
cd chihuahua
git pull
git checkout v4.0.0
make install
```

# check the version

```bash
# should be v4.0.0
chihuahuad version
# Should be commit ef7a6b9f416f8175ca11bb4838e763384ab98107
chihuahuad version --long | grep commit
```

# Make new directory and copy binary

```bash
mkdir -p $HOME/.chihuahua/cosmovisor/upgrades/v400/bin
cp $HOME/go/bin/chihuahuad $HOME/.chihuahua/cosmovisor/upgrades/v400/bin
```

# check the version again

```bash
# should be v4.0.0
$HOME/.chihuahua/cosmovisor/upgrades/v400/bin/chihuahuad version
```
