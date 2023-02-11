### simple OS

writing this while following the post from 
[Philipp Opperman](https://os.phil-opp.com/minimal-rust-kernel/)

### Some thing I learned following the tutorial I didn't know

As we won't use the standar library we have to create a Panic function to
deal with possible panics in our program.

We don't have as well a Runtime to rely on, so we create a new start declaring
the lang item "start" on the function.

It must have the same name and an additional `#[no_mangle]` to guarantee the
BIOS know which function to call when starting the OS