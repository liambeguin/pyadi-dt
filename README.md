# pyadi-dt

Device tree management tools for ADI hardwre

## Quick install

```bash
pip install git+https://github.com/tfcollins/pyadi-dt.git
```

## CLI basics

Get basic info of CLI
```bash
> adidtc
Usage: adidtc [OPTIONS] COMMAND [ARGS]...

  ADI device tree utility

Options:
  -nc, --no-color                 Disable formatting
  -c, --context [local|remote_fs|remote_sd]
                                  Set context  [default: local]
  -i, --ip TEXT                   Set ip used by remote contexts  [default:
                                  192.168.2.1]
  -u, --username TEXT             Set username used by remote SSH sessions
                                  (default is root)  [default: root]
  -w, --password TEXT             Set password used by remote SSH sessions
                                  (default is analog)  [default: analog]
  --help                          Show this message and exit.

Commands:
  prop  Get and set device tree properties COMPATIBLE_ID - Value of..
```

Use the **prop** sub command to read device tree attributes
```bash
> adidtc -c remote_fs -i 192.168.2.1 prop adi,ad9361 clock-output-names
clock-output-names rx_sampl_clk,tx_sampl_clk
```