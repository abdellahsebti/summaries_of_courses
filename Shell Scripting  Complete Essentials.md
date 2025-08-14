

A **shell script** is a plain text file containing commands that the shell (e.g., **Bash**, **Sh**, **Zsh**) can execute in sequence.  
It’s used to automate repetitive tasks, configure systems, run backups, and more.

---

## 1. What is a Shell?

A **shell** is a program that interprets and executes commands you type into the terminal.  
Common shells:
- **bash** — Bourne Again SHell (most common)
- **sh** — original Bourne shell
- **zsh** — Z Shell, with more features
- **fish** — user-friendly shell

---

## 2. Creating Your First Shell Script

1. Create a new file:
```bash
nano script.sh
```

2. Add the **shebang** line at the top (tells system which shell to use):
```bash
#!/bin/bash
```

3. Write your commands under it:
```bash
#!/bin/bash
echo "Hello, World!"
```

4. Save and close the file.

---

## 3. Making the Script Executable

```bash
chmod +x script.sh
```

Run it:
```bash
./script.sh
```

Alternatively, run without changing permissions:
```bash
bash script.sh
```

---

## 4. Comments in Scripts

- Single-line comment:
```bash
# This is a comment
```

- Multi-line comment (using `: <<'END'` trick):
```bash
: <<'END'
This is
a multi-line
comment
END
```

---

## 5. Variables

**Assigning and using variables:**
```bash
name="Abdellah"
age=25
echo "Name: $name, Age: $age"
```
- No spaces around `=`.
- Access with `$variable`.

**Environment variables:**
```bash
echo $HOME
echo $USER
```

---

## 6. User Input

```bash
read -p "Enter your name: " user_name
echo "Hello, $user_name"
```

- `-p` allows prompting on the same line.

---

## 7. Script Arguments

When running a script:
```bash
./script.sh arg1 arg2
```

Inside the script:
```bash
echo "First arg: $1"
echo "Second arg: $2"
echo "Number of args: $#"
echo "All args: $@"
```

---

## 8. Arithmetic in Bash

Using `$(( ))`:
```bash
x=5
y=3
sum=$((x + y))
echo "Sum: $sum"
```

Increment:
```bash
((x++))
```

---

## 9. Conditionals

**If statement:**
```bash
if [ $1 -gt 10 ]; then
    echo "Greater than 10"
elif [ $1 -eq 10 ]; then
    echo "Equal to 10"
else
    echo "Less than 10"
fi
```

**String comparison:**
```bash
if [ "$name" = "Abdellah" ]; then
    echo "Hi Abdellah!"
fi
```

**Common comparison operators:**

| Numeric | Meaning | String | Meaning |
|---------|---------|--------|---------|
| `-eq`   | equal   | `=`    | equal   |
| `-ne`   | not equal | `!=` | not equal |
| `-gt`   | greater than | `<` | less than |
| `-lt`   | less than | `>` | greater than |
| `-ge`   | greater or equal | `-n` | not empty |
| `-le`   | less or equal | `-z` | is empty |

---

## 10. Loops

**For loop:**
```bash
for i in {1..5}; do
    echo "Number $i"
done
```

**While loop:**
```bash
count=1
while [ $count -le 5 ]; do
    echo "Count: $count"
    ((count++))
done
```

**Until loop:**
```bash
num=1
until [ $num -gt 5 ]; do
    echo "Num: $num"
    ((num++))
done
```

---

## 11. Functions

```bash
greet() {
    echo "Hello, $1"
}

greet "World"
```
- `$1` inside the function is the first argument passed to it.

---

## 12. Exit Codes

Every command returns an **exit code**:
- `0` = success  
- Non-zero = error

Check last exit code:
```bash
echo $?
```

Use exit in script:
```bash
if [ "$1" = "" ]; then
    echo "No argument provided!"
    exit 1
fi
```

---

## 13. Working with Files

**Check if a file exists:**
```bash
if [ -f "file.txt" ]; then
    echo "File exists"
fi
```

**Check if a directory exists:**
```bash
if [ -d "myfolder" ]; then
    echo "Directory exists"
fi
```

**Common file operators:**

| Operator | Meaning |
|----------|---------|
| `-f` | File exists |
| `-d` | Directory exists |
| `-e` | Exists (file or dir) |
| `-r` | Readable |
| `-w` | Writable |
| `-x` | Executable |

---

## 14. Useful Commands Inside Scripts

- `pwd` — print working directory  
- `ls` — list files  
- `date` — current date and time  
- `whoami` — current user  
- `hostname` — system name  
- `df -h` — disk space usage  
- `top` — process monitor  
- `grep` — search in text  
- `awk` — text processing  
- `sed` — stream editor  

---

## 15. Debugging Scripts

Run with:
```bash
bash -x script.sh
```
- `-x` prints each command before executing it.

---

## 16. Example Script

```bash
#!/bin/bash

read -p "Enter a number: " num

if [ $num -gt 10 ]; then
    echo "$num is greater than 10"
else
    echo "$num is 10 or less"
fi

for i in {1..$num}; do
    echo "Counting: $i"
done
```

---

## Quick Summary Table

| Concept     | Syntax Example |
|-------------|---------------|
| Shebang     | `#!/bin/bash` |
| Variable    | `x=10` |
| Input       | `read var` |
| Argument    | `$1` |
| If          | `if [ $x -gt 5 ]; then ... fi` |
| For loop    | `for i in {1..5}` |
| While loop  | `while [ $x -lt 5 ]` |
| Function    | `func() { ... }` |
| Execute     | `chmod +x file.sh && ./file.sh` |

---

✅ **Tips:**
- Always start with `#!/bin/bash`
- Use `chmod +x` to make scripts executable
- Test small parts before writing a long script
- Use comments for clarity
