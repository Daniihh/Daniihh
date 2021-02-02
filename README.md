I'm Danii
=========
I'm Danii, a 17 year old programmer who primarily uses Rust. I also program in TypeScript, Python, Java, Shell, and for languages I don't know yet, I doubt I'd take any longer than a day to learn it.

I'm currently helping a friend develop a Discord bot and Discord bot framework, check it out at [pylon.bot](https://pylon.bot/). Outside of that, I'm not getting paid for anything and am looking for a generic fast food job just to do something. Inbetween all of that I have also started volunteering for food drives.

Currently I'm 17 years old, white, gay, living in Florida, United States, and a high school drop out trying to proove that being a high school drop out doesn't mean I can't do good work. I use Arch btw, well actually Manjaro, but I'm looking forward to eventually just installing vanilla Arch Linux.

Programming
-----------
When it comes to programming, here are the subjects I'm most confident in.
- Memory Safety (Thanks Rust)
- High Level Networking
- Library APIs
- Network APIs (E.x. HTTP Servers)
- Data Formats
- Data Streams
- Asynchronous Programming
- Synchronous Programming
- Command Line Interfaces
- Terminal User Interfaces
<!-- - Cat Boys -->

And here are my most favorite languages to least favorite, that I know how to use.
1. Rust
1. C & C++
	- I know I haven't used C, but with the amount of C like languages and Rust having taught me everything there is about Memory Safety, I could pick it up in 2 seconds flat
1. Python
1. TypeScript
1. Bash
1. JavaScript
1. Java

### Libraries
I tend to have a bit of a god complex when it comes to writing libraries... Well, it's not so that I am correct, but rather that it's obvious things should be done the way they are in my mind. Here's the rundown, I suppose, on the way I believe libraries should be written.
- Libraries should offer the most simplistic and clean API, while still being versatile and support all the operations one would expect
- Libraries should be thoroughly documented
- Libraries should have at least one well defined main entry point for interacting with the library, documented in the top level documentation
- Libraries should use the right language feature for the job
	- A bad example
	```rust
	// Gross!
	api.do(message.reply("Hey!")).await;
	```
	- A good example
	```rust
	// Beautiful, I don't have to look into trait implementations to see what's happening.
	api.send_message(message.build_text_reply("Hey!")).await;
	```
- Finally, libraries should be customizable and expose all information the structs or objects of the library may contain (where reasonable)

Yeah, it's quite a lot. The libraries that tend to deviate the most from those principles frustrate me to no end.

To give some examples, here's a few libraries that I think are exceptional and check all those boxes.
- [rustube](https://lib.rs/crates/rustube)
	- Easily customizable with feature flags
	- Shows you the main entry point to the library in one of it's first paragraphs in the top level documentation
	- Gives you all the information you could need (it currently does give you a lot, but giving you the entirety of video metadata is planned for a future version)
	- Good documentation
	- (Yes, the current build is broken, I've submitted a PR to fix it - it wasn't a lot to change)
- [serde](https://docs.serde.rs/serde/)
	- Uses the best language feature for it's job
	- Extremely versatile, and extremely fast
	- Although it doesn't have a well defined endpoint, it's manual explains what it offers very well
		- The crates that implement Deserializer and Serializer don't have this problem (e.g. [serde-json](https://lib.rs/crates/serde_json))
		- It's not much of a problem as it is that *the crate's abilities are very broad*

...and here are some of the libraries that fail to check those boxes.
- [ffmpeg-next](https://lib.rs/crates/ffmpeg-next)
	- Zero documentation. Unusable. I'm certain it would be a breeze to use a Muxer and what not to do work with video, *if I could read up on how they work*
		- As with these things, I don't hate the library, I just hate the fact no one added documentation. If you know the ins and outs of ffmpeg, [please help add documentation](https://github.com/zmwangx/rust-ffmpeg/issues/39)
- [serenity](https://lib.rs/crates/serenity)
	- Extreme overuse of `Arc`s, turning Rust into Python wherever you decide to add the crate as a dependency
	- This isn't to say the library doesn't has a decent api

### Binaries
In my opinion, when it comes to writing binaries, the same rules for libraries ought to be applied; albeit a lot more sparingly. For one, with a private personal binary, you don't have to worry about documentation or anything. Maybe buisness applications don't need to follow the rules so strongly either.

One situation where I think the rules still apply is open source binaries, where you want other people to collaborate. Of course, whether or not you add documentation to your binary is one thing, but adding documentation for the people who *use* that binary is another thing. You should always add documentation for the users of your binary whether it be a command line application or graphical user interface, provided you intend to release it publicly. E.g. your web browser has a manual, I [know that](https://support.mozilla.org/en-US/kb/get-started-firefox-overview-main-features) [for sure](https://support.google.com/chrome/?p=help).

Unfinished
----------
I'm still writing this... This will probably be very big on my GitHub profile so I might move it to my website.
