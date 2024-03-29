# IOb Timer Linux Kernel Drivers
- Structure:
    - `drivers/`: directory with linux kernel module drivers for iob_timer
        - `iob_timer.c`: driver source
        - `[iob_timer.h]`: header file generated by:
        ```bash
        python3 ./scripts/bootstrap.py iob_timer -f gen_linux_driver_header -o [output_dir]
        ```
    - `user/`: directory with user application example that uses iob_timer
      drivers
        - `iob_timer_user.c`: example user application that uses iob_timer
          drivers
        - `Makefile`: user application compilation targets
    - `iob_timer.dts`: device tree template with iob_timer node
        - manually add the `timer` node to the system device tree so the
          iob_timer is recognized by the linux kernel
