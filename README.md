# waydroid-fc43-fix
Patched code at /usr/lib/waydroid/tools/actions/initializer.py for fixing the pickling error:

```
when serializing dict item '_target'
when serializing multiprocessing.context.Process state
when serializing multiprocessing.context.Process object
```

This error appears in Fedora 43 which ships Python 3.14.

# Install
Paste into terminal for a simple install:
```
git clone https://github.com/bby256/waydroid-fc43-fix.git
cd waydroid-fc43-fix
sudo mv /usr/lib/waydroid/tools/actions/initializer.py /usr/lib/waydroid/tools/actions/initializer.py.bak
sudo cp initializer.py /usr/lib/waydroid/tools/actions/initializer.py
```

# Undo changes
To undo the changes and restore the unpatched code:
```
sudo rm /usr/lib/waydroid/tools/actions/initializer.py
sudo mv /usr/lib/waydroid/tools/actions/initializer.py.bak /usr/lib/waydroid/tools/actions/initializer.py
```
