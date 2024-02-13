# --- Library setup -----------------------------------------------------------

# When importing from the root of the unpacked tarball or git checkout,
# Python sees the "h5py" source directory and tries to load it, which fails.
# We tried working around this by using "package_dir" but that breaks Cython.
