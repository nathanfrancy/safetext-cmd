# safetext-cmd
Command line interface for safetext.

## General information
For general information about the `safetext` api that this tool uses please refer to the [safetext](https://www.npmjs.com/package/safetext) module (this is the command line interface).
 
## Setting Up
Install this package globally:

```bash
npm install safetext-cmd --global
```

If you install `safetext-cmd` globally, it will be symlinked into your system, and you'll have access to the `safetext` command from anywhere in your file system.

### Create the safetext file

```bash
cd /path/to/your/project
safetext init <master password>
```

You should see a `safetext` file in your working directory now. Keep the password in a safe place. Once you create this file, it's almost impossible to decrypt the file without the master.

### Add a key
This should show you a success message. If so, your key value is now added to the store.

```bash
safetext add <key> <value> <master password>
```

### Get contents
This will print out all the contents of the file, decrypted. Assuming you provide the correct master password.

```bash
safetext get-all <master password>
```

### Get value by key
This will do the same thing as above, but will only print one value out depending on which key you give it. This is case sensitive and will error if you give it a key that isn't in the object. You obviously have to provide the correct password too.

```bash
safetext get <key> <master password>
```

### Remove a value by key
This will read from the safetext file, remove the provided key value out (if it exists), and give you a success message.

```bash
safetext remove <key> <master password>
```
