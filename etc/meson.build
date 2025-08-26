install_data(['secrets'],
  install_dir : davfs2_sysconfdir,
  install_mode : 'rw-------'
)

install_data(['davfs2.conf'],
  install_dir : davfs2_sysconfdir,
)

if meson.version().version_compare('>= 0.60.0')
  install_emptydir(davfs2_sysconfdir / davfs2_certdir)
  install_emptydir(davfs2_sysconfdir / davfs2_certdir / 'private')

else
  install_subdir(
    davfs2_certdir,
    install_dir : davfs2_sysconfdir
  )

  install_subdir(
    'private',
    install_dir : davfs2_sysconfdir / davfs2_certdir
)
endif

install_data(['davfs2.conf', 'secrets'],
  install_dir : davfs2_sharedir
)
