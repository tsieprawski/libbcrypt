project('bcrypt', 'c',
    version: '1.3'
)

bcrypt_inc = include_directories('crypt_blowfish')
bcrypt_lib = shared_library('bcrypt',
    'crypt_blowfish/crypt_blowfish.c',
    'crypt_blowfish/crypt_gensalt.c',
    'crypt_blowfish/wrapper.c',
    'crypt_blowfish/x86.S',
    include_directories: bcrypt_inc,
    install: true
)
install_headers(
    'crypt_blowfish/crypt.h',
    'crypt_blowfish/ow-crypt.h'
)

bcrypt_dep = declare_dependency(link_with: bcrypt_lib,
    include_directories: bcrypt_inc)
