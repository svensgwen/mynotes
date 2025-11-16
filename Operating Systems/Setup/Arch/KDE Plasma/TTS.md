sudo pacman -S git rust python python-pip base-devel


git clone https://github.com/MycroftAI/mimic3.git
cd mimic3


pip install --break-system-packages --editable .

python -m venv ~/mimic3-env
source ~/mimic3-env/bin/activate
pip install --editable .

mimic3 --help

mimic3 --voices
mimic3 --download-voice en_US/ljspeech

echo "Arch Linux is alive" | mimic3

sudo pacman -S pyenv


git clone https://github.com/pyenv/pyenv.git ~/.pyenv
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo -e 'if command -v pyenv >/dev/null; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bashrc
source ~/.bashrc

sudo pacman -S pyenv

git clone https://github.com/pyenv/pyenv.git ~/.pyenv
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo -e 'if command -v pyenv >/dev/null; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bashrc
source ~/.bashrc

pyenv install 3.11.9


pyenv local 3.11.9
python -m venv ~/mimic3-env
source ~/mimic3-env/bin/activate

mimic3 --version


FIX 2

yay -S piper-tts

pip install piper-tts


piper --list-voices
piper --download en_US-amy-medium


echo "Hello" | piper
