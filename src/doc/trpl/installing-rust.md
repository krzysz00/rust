% Installing Rust

The first step to using Rust is to install it! There are a number of ways to
install Rust, but the easiest is to use the `rustup` script. If you're on Linux
or a Mac, all you need to do is this: 

> Note: you don't need to type in the `$`s, they just indicate the start of
> each command. You’ll see many tutorials and examples around the web that
> follow this convention: `$` for commands run as your regular user, and
> `#` for commands you should be running as an administrator.

```bash
$ curl -sf -L https://static.rust-lang.org/rustup.sh | sh
```

If you're concerned about the [potential insecurity][insecurity] of using `curl
| sh`, please keep reading and see our disclaimer below. And feel free to
use a two-step version of the installation and examine our installation script:

```bash
$ curl -f -L https://static.rust-lang.org/rustup.sh -O
$ sh rustup.sh
```

[insecurity]: http://curlpipesh.tumblr.com

If you're on Windows, please download either the [32-bit installer][win32] or
the [64-bit installer][win64] and run it.

[win32]: https://static.rust-lang.org/dist/rust-1.0.0-i686-pc-windows-gnu.msi
[win64]: https://static.rust-lang.org/dist/rust-1.0.0-x86_64-pc-windows-gnu.msi

## Uninstalling

If you decide you don't want Rust anymore, we'll be a bit sad, but that's okay.
Not every programming language is great for everyone. Just run the uninstall
script:

```bash
$ sudo /usr/local/lib/rustlib/uninstall.sh
```

If you used the Windows installer, just re-run the `.msi` and it will give you
an uninstall option.

Some people, and somewhat rightfully so, get very upset when we tell you to
`curl | sh`. Basically, when you do this, you are trusting that the good
people who maintain Rust aren't going to hack your computer and do bad things.
That's a good instinct! If you're one of those people, please check out the
documentation on [building Rust from Source][from-source], or [the official
binary downloads][install-page].

[from-source]: https://github.com/rust-lang/rust#building-from-source
[install-page]: http://www.rust-lang.org/install.html

Oh, we should also mention the officially supported platforms:

* Windows (7, 8, Server 2008 R2)
* Linux (2.6.18 or later, various distributions), x86 and x86-64
* OSX 10.7 (Lion) or greater, x86 and x86-64

We extensively test Rust on these platforms, and a few others, too, like
Android. But these are the ones most likely to work, as they have the most
testing.

Finally, a comment about Windows. Rust considers Windows to be a first-class
platform upon release, but if we're honest, the Windows experience isn't as
integrated as the Linux/OS X experience is. We're working on it! If anything
does not work, it is a bug. Please let us know if that happens. Each and every
commit is tested against Windows just like any other platform.

If you've got Rust installed, you can open up a shell, and type this:

```bash
$ rustc --version
```

You should see the version number, commit hash, commit date and build date:

```bash
rustc 1.0.0 (a59de37e9 2015-05-13) (built 2015-05-14)
```

If you did, Rust has been installed successfully! Congrats!

This installer also installs a copy of the documentation locally, so you can
read it offline. On UNIX systems, `/usr/local/share/doc/rust` is the location.
On Windows, it's in a `share/doc` directory, inside wherever you installed Rust
to.

If not, there are a number of places where you can get help. The easiest is
[the #rust IRC channel on irc.mozilla.org][irc], which you can access through
[Mibbit][mibbit]. Click that link, and you'll be chatting with other Rustaceans
(a silly nickname we call ourselves), and we can help you out. Other great
resources include [the user’s forum][users], and
[Stack Overflow][stackoverflow].

[irc]: irc://irc.mozilla.org/#rust
[mibbit]: http://chat.mibbit.com/?server=irc.mozilla.org&channel=%23rust
[users]: http://users.rust-lang.org/ 
[stackoverflow]: http://stackoverflow.com/questions/tagged/rust
