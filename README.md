# Build libgnome-volume-control

This repo helps to build [libgnome-volume-control](https://gitlab.gnome.org/GNOME/libgnome-volume-control) outside Gnome environment.
The built files include
```
/usr/lib/gnome-shell
├── Gvc-1.0.typelib
└── libgvc.so

/usr/share/gnome-shell
└── Gvc-1.0.gir
```

Run the following to install:

```sh
meson build --prefix=/usr
ninja -C build install
```
