project('gnome-shell', 'c',
  version: '44.1',
  meson_version: '>= 0.58.0',
  license: 'GPLv2+'
)

prefix = get_option('prefix')

datadir = join_paths(prefix, get_option('datadir'))
libdir = join_paths(prefix, get_option('libdir'))
pkgdatadir = join_paths(datadir, meson.project_name())
pkglibdir = join_paths(libdir, meson.project_name())

libgvc = subproject('gvc',
  default_options: [
    'package_name=' + meson.project_name(),
    'package_version=' + meson.project_version(),
    'pkgdatadir=' + pkgdatadir,
    'pkglibdir=' + pkglibdir,
    'static=false',  
    'introspection=true',
    'alsa=false'    
  ]
)
libgvc_gir = libgvc.get_variable('libgvc_gir')
