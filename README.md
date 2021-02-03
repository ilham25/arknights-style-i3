# Screenshots

![Arknight - Regular](/Other/regular.png)
![Arknight - Rhine](/Other/rhine.png)

# Cara Pasang

> **Salin file**

- ```bash
  git clone https://github.com/ilham25/arknights-style-i3
  ```

- ```bash
  cd arknights-style-i3/ && cp -r {.*,*} ~/
  ```

> **Pasang Icon**

- ```bash
  cd ~/.icons/
  ```
- ```bash
  tar -Jxvf oomox-arknights.tar.xz && tar -Jxvf oomox-arknights-rhine.tar.xz
  ```

- ```bash
  sudo cp -r {oomox-arknights,oomox-arknights-rhine} /usr/share/icons/
  ```

- ```bash
  rm -r ~/.icons/{oomox-arknights,oomox-arknights-rhine,*.tar.xz} # Delete unnecessary files
  ```

> **Buka file `~/.config/i3/startup`**

```bash
geany ~/.config/i3/startup
```

> **Salin config berikut, setelah fungsi `aestheticDark()` dan simpan**

```shell
arknightsRhine() {
    # Dunst
    dunst -config ~/.config/dunst/dunstrc-dark-left &
    # Wallpaper
    feh --bg-fill ~/.wallpaper/rhine-lab.jpg
    # GTK, rofi, color theme
    ~/.config/i3/theme/arknights-rhine/arknights-rhine-theme
    # Panel
    tint2 -c ~/.config/tint2/arknights-i3-rhine.tint2rc &
    # Terminal Color Scheme
    xrdb ~/.config/i3/theme/arknights-rhine/.Xresources
}
arknights() {
    # Dunst
    dunst -config ~/.config/dunst/dunstrc-dark-left &
    # Wallpaper
    feh --bg-fill ~/.wallpaper/ark3.jpg
    # GTK, rofi, color theme
    ~/.config/i3/theme/arknights/arknights-theme
    # Panel
    tint2 -c ~/.config/tint2/arknights-i3.tint2rc &
    # Terminal Color Scheme
    xrdb ~/.config/i3/theme/arknights/.Xresources
}
```

> **Buka file `~/.config/i3/change`**

```bash
geany ~/.config/i3/change
```

> **Salin config berikut**

```shell
    3)
    echo "arknights" > ~/.config/i3/theme/now
    echo "Theme changed to : Arknights - Regular"
    ;;
    4)
    echo "arknightsRhine" > ~/.config/i3/theme/now
    echo "Theme changed to : Arknights - Rhine"
    ;;
```

Setelah bagian

```shell
    2)
    echo "aestheticDark" > ~/.config/i3/theme/now
    echo "Theme changed to : Aesthetic - Dark"
    ;;
```

> **Ubah Tema, jalankan perintah berikut di terminal**

Untuk Arknights Regular

```shell
~/.config/i3/change 3
```

Untuk Arknights Rhine

```shell
~/.config/i3/change 4
```
