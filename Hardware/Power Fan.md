## Fan sound louad and work like a jet

Sometimes after installing an arch linux or other linux the fan going to be speed and make a lot of noise.

Most of time this is because of wrong or not complete configuration of boot files.
For example the GRUB boot loader or systemd must be configure to be in correct way and your laptop or pc computer work and turning on.

If your hard is GPT and have UEFI installed GRUB , you should be have efi boot partition and have some files in it.

So if you installed your linux and after turning on and have full working system , suddenly the fan going to be crazy , then in this situation we have some guests:
        If you have intel CPU , then the function keyboard for screen brightness have to be working but fan isn't correct.
        So you must do this :
                sudo nano /etc/grub/grub.cfg
                Add this :
                title Arch Linux
                linux /vmlinuz-linux
                initrd /intel-ucode.img
                initrd /initramfs-linux.img
                options root=PARTUUID=write_down_root_UUID_here rw i915.preliminary_hw_support=1                                                                        intel_idle.max_cstate=1 i915.enable_execlists=0 acpi_osi= acpi_backlight=native quiet

## Thanks

Thank you again for follow one of our other solving tut.
If our solving is useful for you come and give me a star, its like a cup of coffee. :)
Thanks.
