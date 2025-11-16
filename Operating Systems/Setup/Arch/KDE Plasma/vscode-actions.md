
# ⚙️ KDE Plasma Customization  
## 🖱️ One-Click “Open in VS Code” Right-Click Menu Entry

Plasma 6 tightened security, so service menus need proper validation.  
Here’s the **fully working, system-level version** (most reliable).

---

## 1️⃣ Create the service menu folder
```bash
mkdir -p ~/.local/share/kio/servicemenus
```

## 2️⃣ Create the `vscode.desktop` file
```bash
nano ~/.local/share/kio/servicemenus/vscode.desktop
```

## 3️⃣ Paste this validated KDE-friendly config
```ini
[Desktop Entry]
Type=Service
Name=Open in VS Code
Comment=Open the selected file or folder in Visual Studio Code
Icon=visual-studio-code
ServiceTypes=KonqPopupMenu/Plugin
X-KDE-Priority=TopLevel
X-KDE-PluginInfo-EnabledByDefault=true
MimeType=inode/directory;application/octet-stream;
Actions=openCode;

[Desktop Action openCode]
Name=Open in VS Code
Icon=visual-studio-code
Exec=code "%U"
```

---

# 🔧 Why move it to system level?  
Plasma 6 sometimes misclassifies user-level service menus and refuses to load them unless:
- they’re **root-owned**
- placed in **system service menu path**
- have strict permissions  
So we place it where KDE expects validated plugins.

---

## 4️⃣ Move the menu to the system directory
```bash
sudo mkdir -p /usr/share/kio/servicemenus
sudo cp ~/.local/share/kio/servicemenus/vscode.desktop /usr/share/kio/servicemenus/
sudo chmod 644 /usr/share/kio/servicemenus/vscode.desktop
sudo chown root:root /usr/share/kio/servicemenus/vscode.desktop
```

## 5️⃣ Delete the user copy
```bash
rm ~/.local/share/kio/servicemenus/vscode.desktop
```

## 6️⃣ Rebuild KDE’s service database (forces Plasma to “see” the file)
```bash
kbuildsycoca6 --noincremental
```

## 7️⃣ Restart Dolphin cleanly
```bash
kquitapp6 dolphin
dolphin &
```

---

# ✨ Result
You’ll now have a **top-level, one-click, icon-enabled** “Open in VS Code” option right in your right-click menu — no submenus, no fuss, just clean workflow.

---