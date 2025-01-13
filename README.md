# Мои dotfiles

Для управления файлами конфигураций (dotfiles) используется [GNU Stow](https://www.gnu.org/software/stow/)

## Установка

1. Установить GNU Stow:

```bash
sudo apt install stow
```

2. Установить dotfiles из репозитория:

```bash
cd ~ && git clone https://github.com/Zepten/dotfiles.git && cd ~/dotfiles && stow -R -v -t ~ .
```

## Выборочная установка

Установить только zsh и tmux:

```bash
stow -R -v -t ~ zsh tmux
```

## Удаление симлинков

```bash
stow -D -v -t ~ .
```
