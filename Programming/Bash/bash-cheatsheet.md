# Bash Cheat Sheet — Essentials

![Bash](../../Images/bash.webp)

## 🚀 Running Commands
```bash
command
command --flag value
command1 && command2   # run if previous succeeded
command1 || command2   # run if failed
command1 ; command2    # run always
```

## 📂 Navigation
```bash
pwd           # current directory
ls            # list
ls -la        # detailed list
cd /path
cd ..         # up
cd ~          # home
```

## 📄 File Operations
```bash
touch file.txt
cp a.txt b.txt
mv old new
rm file
rm -r folder
mkdir newfolder
```

## 📦 Viewing Files
```bash
cat file
less file
head file
tail file
tail -f log.txt
```

## ✍️ Editing (CLI)
```bash
nano file
vim file
```

## 🔁 Loops
```bash
for i in {1..5}; do
  echo $i
done

while true; do
  sleep 1
done
```

## 🎯 Variables
```bash
name="Shashank"
echo $name
```

## 📥 Reading Input
```bash
read var
read -p "Enter name: " name
```

## 🧩 Conditionals
```bash
if [ $x -gt 5 ]; then
  echo "big"
else
  echo "small"
fi
```

## 🔍 Comparisons
```bash
-e file       # exists
-d dir        # is directory
-f file       # is file

==  !=        # string compare
-lt -gt -eq   # numbers
```

## ⚙️ Functions
```bash
greet() {
  echo "Hello $1"
}
greet "Shashank"
```

## 🗂️ Arrays
```bash
arr=(a b c)
echo ${arr[0]}
for x in "${arr[@]}"; do echo $x; done
```

## 🔀 Pipes & Redirects
```bash
ls | grep txt
echo "hi" > file.txt
echo "more" >> file.txt
command 2> errors.txt      # stderr
command &> all.txt         # both
```

## 🔧 Permissions
```bash
chmod +x script.sh
chmod 755 file
chown user:group file
```

## 🐳 Process Control
```bash
ps aux
top
htop
kill PID
kill -9 PID
```

## 🚨 Sudo & System
```bash
sudo command
sudo systemctl status service
sudo systemctl restart service
```

## 💻 Networking
```bash
ping google.com
curl https://example.com
wget fileurl
ip a
ss -tulpn
```

## 📦 Packages (APT)
```bash
sudo apt update
sudo apt install pkg
sudo apt remove pkg
```

## 🔒 SSH
```bash
ssh user@host
scp file user@host:/path
```

## 🛠️ Script Template
```bash
#!/bin/bash
set -e

echo "Running..."
```

## 🧼 Cleanup Tricks
```bash
history
history -c
sudo apt autoremove
```

## ⚡ Useful One-Liners
```bash
find . -name "*.txt"
du -sh *               # folder sizes
grep -R "text" .
```

