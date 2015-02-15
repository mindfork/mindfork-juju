# mindfork-juju
A Juju charm for running Mindfork agents.

## Usage

```bash
mkdir trusty
cd trusty
git clone https://github.com/mindfork/mindfork-juju.git
juju deploy --repository=../ mindfork
juju status

...

services:
  mindfork:
    ...
      public-address: W.X.Y.Z

...

curl W.X.Y.Z:25000/mf
```

 > Change port

```bash
juju set mindfork port=12345

...

curl W.X.Y.Z:<port>/mf
```

 > Upgrade to a specific git ref

```bash
juju set \
  version=41a41f935c76757c02f953a8d117659b6455c44a \
  remote=https://github.com/binary132/mindfork.git

...
```
