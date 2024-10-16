# Hyper-V Bridge network connection (External Network)

A fix for those who want to use WSL 2 on bridge networking.

> Basically, this is my first time doing Github stuff, and I don't know much about it. So, with that said, let me get started.



# The Issue

I'm starting out in the world of digital cybersecurity, and I've often found myself having trouble using many programs or scripts that required my virtual machine (WSL) to have a connection to the external network.

Personally, up until the moment I'm posting this, I haven't found any tutorial on YouTube that could actually solve the problem without exhaustive steps, without losing my virtual machine's IP and having to format it, etc.

As you can see, in the image below, my machine has an IP that starts with 172.[...], this is the virtual IP that was generated when I started the machine.

![IP screenshot](https://github.com/dynastyyy003/hyper-v-fix-4150/blob/main/Screenshot_1.png?raw=true)

With this generated IP, we can perform most tasks on the virtual machine, but if you want to practice pentests or network tests, you won't be able to do it using an internal network.

As I was reading some manuals and forums about how WSL behaves, I discovered a solution that was quite simple.

# The Solution (Fix)
