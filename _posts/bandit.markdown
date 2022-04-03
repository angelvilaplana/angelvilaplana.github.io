---
layout: post
title:  "Bandit"
categories: linux ctf
---

## CONNECT SERVER

```bash
ssh <bandit(level)>@bandit.labs.overthewire.org -p 2220
```

<br>

## LEVELS

- [LEVEL 0](#level-0-bandit0)
- [LEVEL 1](#level-1-bandit1)
- [LEVEL 2](#level-2-bandit2)
- [LEVEL 3](#level-3-bandit3)
- [LEVEL 4](#level-4-bandit4)
- [LEVEL 5](#level-5-bandit5)
- [LEVEL 6](#level-6-bandit6)
- [LEVEL 7](#level-7-bandit7)
- [LEVEL 8](#level-8-bandit8)
- [LEVEL 9](#level-9-bandit9)
- [LEVEL 10](#level-10-bandit10)
- [LEVEL 11](#level-11-bandit11)
- [LEVEL 12](#level-12-bandit12)
- [LEVEL 13](#level-13-bandit13)
- [LEVEL 14](#level-14-bandit14)
- [LEVEL 15](#level-15-bandit15)
- [LEVEL 16](#level-16-bandit16)
- [LEVEL 17](#level-17-bandit17)
- [LEVEL 18](#level-18-bandit18)
- [LEVEL 19](#level-19-bandit19)
- [LEVEL 20](#level-20-bandit20)
- [LEVEL 21](#level-21-bandit21)
- [LEVEL 22](#level-22-bandit22)
- [LEVEL 23](#level-23-bandit23)
- [LEVEL 24](#level-24-bandit24)
- [LEVEL 25](#level-25-bandit25)
- [LEVEL 26](#level-26-bandit26)
- [LEVEL 27](#level-27-bandit27)
- [LEVEL 28](#level-28-bandit28)
- [LEVEL 29](#level-29-bandit29)
- [LEVEL 30](#level-30-bandit30)
- [LEVEL 31](#level-31-bandit31)
- [LEVEL 32](#level-32-bandit32)
- [LEVEL 33](#level-33-bandit33)

<br>

### LEVEL 0 (bandit0)

**Solution**

```bash
cat readme
```

**Password**

```
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```

<br>

### LEVEL 1 (bandit1)

**Solution**

```bash
cat ./-
```

**Password**

```
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```

<br>

### LEVEL 2 (bandit2)

**Solution**

```bash
cat spaces\ in\ this\ filename
```

**Password**

```
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```

<br>

### LEVEL 3 (bandit3)

**Solution**

```bash
cat inhere/.hidden
```

**Password**

```
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
```

<br>

### LEVEL 4 (bandit4)

**Solution**

```bash
cd inhere
passwd=$(find . | xargs file | grep 'ASCII text' | cut -d: -f1)
cat $passwd
```

**Password**

```
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```

<br>

### LEVEL 5 (bandit5)

**Solution**

```bash
cd inhere
find . -type f -readable -size 1033c ! -executable
cat ./maybehere07/.file2
```

**Password**

```
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```

<br>

### LEVEL 6 (bandit6)

**Solution**

```bash
cd /
find . -type f -size 33c -user bandit7 -group bandit6 -print 2>/dev/null
cat ./var/lib/dpkg/info/bandit7.password
```

**Password**

```
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```

<br>

### LEVEL 7 (bandit7)

**Solution**

```bash
grep 'millionth' data.txt
```

**Password**

```
cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```

<br>

### LEVEL 8 (bandit8)

**Solution**

```bash
cat data.txt | sort | uniq -u
```

**Password**

```
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

<br>

### LEVEL 9 (bandit9)

**Solution**

```bash
strings data.txt | grep "&="
```

**Password**

```
truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```

<br>

### LEVEL 10 (bandit10)

**Solution**

```bash
base64 -d data.txt
```

**Password**

```
IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```

<br>

### LEVEL 11 (bandit11)

**Solution**

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

**Password**

```
5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```

<br>

### LEVEL 12 (bandit12)

**Solution**

```bash
mkdir /tmp/bandit12
cp ~/data.txt /tmp/bandit12
cat data.txt | xxd -r > data.gz
gzip -d data.gz
mv data data.bz2
bzip2 -d data.bz2
mv data data.gz
tar -xvf data
tar -xvf data5.bin
mv data6.bin data6.bz2
bzip2 -d data6.bz2
tar -xvf data6
mv data8.bin data8.gz
gzip -d data8.gz
cat data8
```

**Password**

```
8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
```

<br>

### LEVEL 13 (bandit13)

**Solution**

```bash
ssh -i sshkey.private bandit14@localhost
cat /etc/bandit_pass/bandit14
```

**Password**

```
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
```

<br>

### LEVEL 14 (bandit14)

**Solution**

```bash
echo 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e | nc localhost 30000
```

**Password**

```
BfMYroe26WYalil77FoDi9qh59eK5xNr
```

<br>

### LEVEL 15 (bandit15)

**Solution**

```bash
echo BfMYroe26WYalil77FoDi9qh59eK5xNr | openssl s_client -connect localhost:30001 -ign_eof
```

**Password**

```
cluFn7wTiGryunymYOu4RcffSxQluehd
```

<br>

### LEVEL 16 (bandit16)

**Solution**

```bash
for i in {31000..32000}; do
    if nc -z localhost $i 1> /dev/null 2>&1; then
        echo cluFn7wTiGryunymYOu4RcffSxQluehd | openssl s_client -connect localhost:$i &>/dev/null
        ret=$?
        if [ $ret -eq 0 ]; then
            echo $i
        fi
    fi
done

echo cluFn7wTiGryunymYOu4RcffSxQluehd | openssl s_client -connect localhost:31790 -ign_eof
mkdir /tmp/bandit17
echo '-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----' > /tmp/bandit17/sshkey.private
chmod 400 /tmp/bandit17/sshkey.private
ssh -i /tmp/bandit17/sshkey.private bandit17@localhost
cat /etc/bandit_pass/bandit17
```

**Password**

```
xLYVMN9WE5zQ5vHacb0sZEVqbrp7nBTn
```

<br>

### LEVEL 17 (bandit17)

**Solution**

```bash
diff passwords.old passwords.new
```

**Password**

```
kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
```

<br>

### LEVEL 18 (bandit18)

**Solution**

```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/bash
cat readme
```

**Password**

```
IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
```

<br>

### LEVEL 19 (bandit19)

**Solution**

```bash
./bandit20-do cat /etc/bandit_pass/bandit20
```

**Password**

```
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
```

<br>

### LEVEL 20 (bandit20)

**Solution**

```bash
echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -l localhost -p 1234 &
./suconnect 1234
```

**Password**

```
gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
```

<br>

### LEVEL 21 (bandit21)

**Solution**

```bash
cd /etc/cron.d
cat cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```

**Password**

```
Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
```

<br>

### LEVEL 22 (bandit22)

**Solution**

```bash
cd /etc/cron.d
cat cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh
myname=bandit23
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
cat /tmp/$mytarget
```

**Password**

```
jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n
```

<br>

### LEVEL 23 (bandit23)

**Solution**

```bash
cd /etc/cron.d
cat cronjob_bandit24
cat /usr/bin/cronjob_bandit24.sh
mkdir /tmp/bandit23
cd /tmp/bandit23
touch script.sh
chmod 777 script.sh
echo '#!/bin/bash' >> script.sh
echo 'cat /etc/bandit_pass/bandit24 > /tmp/bandit23/password' >> script.sh
touch password
chmod 666 password
cp script.sh /var/spool/bandit24
# Wait for the script to be executed in bandit24
cat password
```

**Password**

```
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
```

<br>

### LEVEL 24 (bandit24)

**Solution**

```bash
mkdir /tmp/bandit24 && cd $_
passwords=""

for i in {0000..9999}; do
    echo $i
    passwords="$passwords\nUoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i"
done

echo -e $passwords > passwords.txt
nc localhost 30002 < passwords.txt
```

**Password**

```
uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG
```

<br>

### LEVEL 25 (bandit25)

**Solution**

```bash
cat /etc/passwd | grep bandit26
ssh -i bandit26.sshkey bandit26@localhost
# Reduce the height of the terminal windows
# Press "v" to enter vim editing
# Enter :e /etc/bandit_pass/bandit26
```

**Password**

```
5czgV9L3Xx8JPOyRbXh6lQbmIOWvPT6Z
```

<br>

### LEVEL 26 (bandit26)

**Solution**

```bash
# Reduce the height of the terminal windows
# Press "v" to enter vim editing
# Enter :set shell=/bin/bash
# Enter :shell
# Enter :q! if you haven't exited vim mode
./bandit27-do cat /etc/bandit_pass/bandit27
```

**Password**

```
3ba3118a22e93127a4ed485be72ef5ea
```

<br>

### LEVEL 27 (bandit27)

**Solution**

```bash
mkdir /tmp/bandit27 && cd $_
git clone ssh://bandit27-git@localhost/home/bandit27-git/repo
# Same password as "bandit27"
cat repo/README
```

**Password**

```
0ef186ac70e04ea33b4c1853d2526fa2
```

<br>

### LEVEL 28 (bandit28)

**Solution**

```bash
mkdir /tmp/bandit28 && cd $_
git clone ssh://bandit28-git@localhost/home/bandit28-git/repo
# Same password as "bandit28"
cd repo
git log
git checkout c086d11a00c0648d095d04c089786efef5e01264
cat README.md
```

**Password**

```
bbc96594b4e001778eee9975372716b2
```

<br>

### LEVEL 29 (bandit29)

**Solution**

```bash
mkdir /tmp/bandit29 && cd $_
git clone ssh://bandit29-git@localhost/home/bandit29-git/repo
# Same password as "bandit29"
cd repo
git branch -r
git checkout dev
cat README.md
```

**Password**

```
5b90576bedb2cc04c86a9e924ce42faf
```

<br>

### LEVEL 30 (bandit30)

**Solution**

```bash
mkdir /tmp/bandit30 && cd $_
git clone ssh://bandit30-git@localhost/home/bandit30-git/repo
# Same password as "bandit30"
cd repo
git tag
git show secret
```

**Password**

```
47e603bb428404d265f59c42920d81e5
```

<br>

### LEVEL 31 (bandit31)

**Solution**

```bash
mkdir /tmp/bandit31 && cd $_
git clone ssh://bandit31-git@localhost/home/bandit31-git/repo
# Same password as "bandit31"
cd repo
echo 'May I come in?' > key.txt
rm .gitignore
git add .
git commit -m "push commit"
git push
```

**Password**

```
56a9bf19c63d650ce78e6ec0354ee45e
```

<br>

### LEVEL 32 (bandit32)

**Solution**

```bash
$0
id
cat /etc/bandit_pass/bandit33
```

**Password**

```
c9c3199ddf4121b10cf581a98d51caee
```

<br>

### LEVEL 33 (bandit33)

**Solution**

```bash
cat README.txt
```

**Password**

```

```
