```shell
command -v <the_command>
```

```bash
if ! command -v COMMAND &> /dev/null
then
    echo "COMMAND could not be found"
    exit
fi
```

## References

[How can I check if a program exists from a Bash script?](https://stackoverflow.com/questions/592620/how-can-i-check-if-a-program-exists-from-a-bash-script)