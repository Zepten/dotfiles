# Dotfiles

В этом репозитории содержатся все мои личные конфигурационные файлы (dotfiles) для облегчения их версионирования и переноса на другие устройства.

Для управления dotfiles используется [GNU Stow](https://www.gnu.org/software/stow/).

## Установка

1. Установить GNU Stow (я использую пакетный менеджер `apt`):

```bash
sudo apt install stow
```

2. Клонировать этот репозиторий в директорию `~/.dotfiles`:

```bash
cd ~ && git clone https://github.com/Zepten/dotfiles.git && mv ~/dotfiles ~/.dotfiles && cd ~/.dotfiles
```

3. Установить нужные модули командой `stow` из директории `~/.dotfiles`:

```bash
stow -R -v alacritty kitty git lazygit bash eza zsh tmux nvim poetry
```

## Удаление симлинков

Удаление симлинков делается командой `stow` с флагом `-D` и списком модулей, симлинки к которым нужно удалить:

```bash
stow -D -v alacritty kitty git lazygit bash eza zsh tmux nvim poetry
```
