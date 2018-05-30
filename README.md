# rust-tips
some good things

### cannot resolve std::convert::AsRef<_>
#### error 
`error[E0283]: type annotations required: cannot resolve std::string::String: std::convert::AsRef<_>
--> /home/.cargo/git/checkouts/parity-dc9825eb65b3adf1/0ecbb3e/util/network-devp2p/src/service.rs:35:91
info!(target: "network", "Public node URL: {}", Colour::White.bold().paint(public_url.as_ref()));
error: aborting due to previous error`

#### Resolve:
Change `public_url.as_ref()` to `AsRef::<str>::as_ref(public_url)`


###
