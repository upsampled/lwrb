project('lwrb', 'c',
  version : '2.0.3',
  license : 'MIT')

inc = include_directories('lwrb/src/include')


pkg_mod = import('pkgconfig')

subdir('lwrb/src/include')
subdir('lwrb/src')


libsimple_dep = declare_dependency(include_directories : inc,
  link_with : liblwrb)

pkg_mod = import('pkgconfig')
pkg_mod.generate(libraries : liblwrb,
                 version : '2.0.3',
                 name : 'librb',
                 filebase : 'lwrb',
                 description : 'Library provides generic FIFO ring buffer implementation.')
