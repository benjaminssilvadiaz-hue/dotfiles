# dotfiles ✦

Mis configuraciones de Arch Linux + KDE Plasma (Wayland), con estilo **espacial**:
negro, blanco, cian y toques dorados.

| Color | Hex | Uso |
|---|---|---|
| Negro | `#0A0A0F` | Fondo |
| Superficie | `#16161D` | Ventanas, cabeceras |
| Blanco | `#F5F5F7` | Texto |
| Cian | `#22D3EE` | Acento: selección, foco, enlaces |
| Dorado | `#F5C542` | Toques: hover, elemento activo |

## Contenido

Cada carpeta es un paquete de [GNU Stow](https://www.gnu.org/software/stow/) que imita la estructura de `~`.

| Paquete | Archivos |
|---|---|
| `bash` | `.bashrc` (fastfetch + starship al abrir la terminal) |
| `kde` | Esquema de colores `Espacial.colors` |
| `konsole` | Perfil y esquema de colores `Espacial` (fuente JetBrains Mono Nerd) |
| `starship` | Prompt `starship.toml` |
| `fastfetch` | `config.jsonc` (logo cian, etiquetas doradas) |

Otros ajustes (aplicados desde Configuración del sistema): tema global Breeze Dark,
iconos Papirus-Dark, fondo "Imagen del día" con NASA APOD.

## Instalar en un sistema nuevo

```bash
sudo pacman -Syu git stow starship fastfetch papirus-icon-theme ttf-jetbrains-mono-nerd
git clone https://github.com/benjaminssilvadiaz-hue/dotfiles.git ~/dotfiles
cd ~/dotfiles
stow --no-folding -t ~ bash kde konsole starship fastfetch
```

Si un archivo ya existe en `~`, stow se detiene sin sobrescribir: muévelo o respáldalo primero.
