# wheeliebin

A rubbish bin for the command line.

## install

Drop `wb` somewhere in path.

There are no dependencies other than python (3.4+).

## usage

Move a file or folder into the bin with:

```bash
wb /file/to/delete
```

Or move a glob

```bash
wb *.txt
```

List the contents of bin with:

```bash
wb list
```

And empty the bin with:

```bash
wb empty
```

You can also empty the bin without confirmation. Useful for scheduled
tasks/cron. For example, to take the bins out on Thursday night using
cron:

```bash
0 20 * * 4 wb force
```

## usage on windows

As ever, Windows is a bit different. There you need to prepend commands
with py:

```powershell
py path/to/wb /file/to/delete
```

But you can avoid this by adding a function to your powershell $profile:

```powershell
function wb {
  py path/to/wb $args[0]
}
```
