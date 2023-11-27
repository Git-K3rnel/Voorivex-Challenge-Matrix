# Level-25

Level25-26 (https://matrix.voorivex.academy/the-final-fight-4dba54234d41bc0bbe7c7a8193f22a61)

you see a javascript in this page :

```text
https://matrix.voorivex.academy/the-final-fight-4dba54234d41bc0bbe7c7a8193f22a61
```

it has 4 if condition that we should avoid getting false for them:

- first condition is `if (flag.length != '0'.charCodeAt(0))`
it means our flag should be 48 character long 

- second condition is `if (!/^the-final-fight-/.test(flag))`
it means our flag should start with `the-final-fight-` string

- third condition
it means our flag at position 16 to 32 must be a specific string
if we calculate the return statement it returns `0a9fe5e4822afb91`
meaning characters 16 to 32 must be `0a9fe5e4822afb91`

- fourth condition
it means from position 32 to 48 must be a specific string
if we calculate `((s, k) => [...Array(s.length).keys()].map(i => String.fromCharCode(s.charCodeAt(i) + (i % 2 === 0 ? -k : k))).join(''))("e5956b6a605e536e", 3)`
in the console we get `b8683e3d332h263h`
meaning characters 32 to 48 must be `b8683e3d332h263h`

- our final flag will become : `the-final-fight-0a9fe5e4822afb91b8683e3d332h263h`
and that's the next level

go to:

```text
https://matrix.voorivex.academy/the-final-fight-0a9fe5e4822afb91b8683e3d332h263h
```
