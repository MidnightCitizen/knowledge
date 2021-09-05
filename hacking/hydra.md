Hydra allows cracking passwords by testing thousands of possibilities, i.e. by a brute-force method.
You need to give the tool the name of the user and a wordlist of common passwords in order to find the good combination.

```shell
hydra -l jan -P rockyou.txt ssh://10.10.80.16
```

![Hydra Example](/images/hydra_results.png)

## References

[Password Cracking:SMB](https://www.hackingarticles.in/password-crackingsmb/)