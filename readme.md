# SafeCron

SafeCron is a wrapper for the `crontab` command that automatically includes the `-i` flag to prevent accidental deletion of the user's crontab when using the `-r` flag.

## Installation

To install SafeCron, use one of the following methods:

### Using `wget`


```bash
sudo wget -q https://raw.githubusercontent.com/cuddlyclara/safecron/refs/heads/main/safecron.sh -O /usr/local/bin/safecron && sudo chmod +x /usr/local/bin/safecron
```

### Using `curl`


```bash
sudo curl -s https://raw.githubusercontent.com/cuddlyclara/safecron/refs/heads/main/safecron.sh -o /usr/local/bin/safecron && sudo chmod +x /usr/local/bin/safecron
```


## Usage

Once installed, you can use `safecron` just like the regular `crontab` command. It will automatically include the `-i` flag for safety, preventing any accidental deletion of crontab entries.

### Example

To edit your crontab:

```bash
safecron -e
```

If you run the following command to delete your crontab:

```bash
safecron -r
```

You will always be prompted with the following question:

```
crontab: really delete user's crontab? (y/n)
```
