# Bash Tricks
## Editing `.bash_profile`:

`.bash_profile` is a script that is run when `bash` is invoked. For Mac, it gets run every time you open terminal, it's basically a config file for terminal. Add code to the file and restart terminal for the changes to take effect.

A couple things you can do include:
* setting aliases, e.g.: having `alias notebook="jupyter notebook"` lets me open jupyter notebook by just typing one word, which is a lot faster than two considering autocomplete.

## Loops

```bash
for file in *.h5 do 
  if ! ls ../fil/*.fil | grep ${file%.h5} -c &>/dev/null
    then echo ${file%.h5} "not found, transferring"
         h52fil $file 
  fi 
done
```
