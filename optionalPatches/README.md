`cmakelists_*.patch` -> Adds compiler optimizations for various CPU extensions. This might not have any effect at all, as the cpu intensive emulation core already includes optimizations for each extension, regardless of compiler flag.

`shadowFlicker.patch` -> Workaround for the issue described here https://github.com/yuzu-emu/yuzu/issues/10320#issuecomment-1573316956