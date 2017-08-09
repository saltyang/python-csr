# python-csr
## Purpose
Generate a key, self-signed certificate, and certificate request.

## Information
You'll notice there is a csrgen and csrgen35. This corresponds to their respective Python versions.
- csrgen uses Python 2.7
- csrgen34 uses Python 3.5

## Installation / Dependencies
The following modules are required:
- OpenSSL (pyopenssl)
- Argparse (argparse)
- YAML (pyyaml)

I've included a setup.py that will install these dependencies if you run:
```
python setup.py install`
```

## Usage
csrgen [fqdn]

```
python csrgen test.test.com
```

When more than one hostname is provided, a SAN (Subject Alternate Name)
certificate and request are generated.  This can be acheived by adding a -s.

csrgen <hostname> -s <san0> <san1>

```
python csrgen test.test.com -s mushu.test.com pushu.test.com
```
