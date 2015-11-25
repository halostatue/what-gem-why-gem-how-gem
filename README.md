![fit](rails-girls-toronto.jpeg)

---
# [fit] What Gem
# [fit] Why Gem
# [fit] How Gem

---
# [fit] or

---
# [fit] Sharing Your Code
# [fit] as RubyGems

---
# [fit] Austin Ziegler
# [fit] [github.com/halostatue][gh]

[gh]: https://github.com/halostatue
---
# [fit] Rubyist since 2002

---
# [fit] 19+ gems

---
# [fit] 19+ gems
# [fit] 114M+ downloads

---
# [fit] What is a Gem?

---
# [fit] Downloadable
# [fit] Ruby Code

---
# [fit] Your code
# [fit] +
# [fit] A gemspec

---
# [fit] Gemspec = Gem metadata

```ruby
Gem::Specification.new do |spec|
  s.name          = "marlowe"
  s.version       = "1.0.1"
  s.authors       = ["Trevor Oke", "Kinetic Cafe ALDO Team"]
  s.email         = ["toke@kineticcafe.com", "dev@kineticcafe.com"]
  s.description   = %q{Provides a correlation …}
  s.summary       = %q{Correlation IDs for Rails and other Rack applications}
  s.homepage      = "https://github.com/KineticCafe/marlowe"
  s.license       = "MIT"

  # …
end
```

---
# [fit] When packaged
# [fit] Install with
# [fit] `gem install marlowe`

---
# [fit] Why make a Gem?

---
# [fit] 1️⃣
# [fit] Reuse Your
# [fit] Own Code

---
# [fit] Kinetic Cafe
# [fit] 6 private gems

---
# [fit] Shared Code
# [fit] for all apps

---
# [fit] Not Published
# [fit] on Rubygems.org

---
# [fit] Geminabox
# [fit] + OpenShift
# [fit] + [rubygems-quickstart][]
# [fit] = Free Private Gem Server

[rubygems-quickstart]: https://github.com/halostatue/rubygems-quickstart

---
# [fit] or
# [fit] use [Gemfury][]

[Gemfury]: https://gemfury.com/

---
# [fit] 2️⃣
# [fit] Share
# [fit] Your code

---
# [fit] Other people might
# [fit] find your code
# [fit] useful

---
# [fit] Published
# [fit] on Rubygems.org

---
# [fit] Open Source

---
# [fit] How to make a Gem?

---
# [fit] Gems are easy

---
# [fit] create gemspec

---
# [fit] build gem

---
# [fit] release gem

---
# [fit] Hardest part:

---
# [fit] Hardest part:
# [fit] The idea

---
# [fit] Hardest part:
# [fit] ~~The idea~~

---
# [fit] Hardest part:
# [fit] The Name

---
# [fit] The Best Gems
# [fit] Are from
# [fit] Working Code

---
# [fit] Tools for
# [fit] Building Gems

---
# [fit] Tool: [Bundler][]
## `bundler gem GEM`

[Bundler]: http://bundler.io/

---
# [fit] Why
# [fit] Bundler?

* Ubiquitous
* You Already Have it

---
# [fit] `bundler gem GEM [OPTIONS]`
# [fit] _`-b, [--bin], [--no-bin]`_

---
# [fit] `bundler gem GEM [OPTIONS]`
# [fit] _`-b, [--bin], [--no-bin]`_
# [fit] Generate a binary for your library.

---
# [fit] `bundler gem GEM [OPTIONS]`
# [fit] _`[--coc], [--no-coc]`_

---
# [fit] `bundler gem GEM [OPTIONS]`
# [fit] _`[--coc], [--no-coc]`_
# [fit] Generate a code of conduct file.

---
# [fit] `bundler gem GEM [OPTIONS]`
# [fit] _`[--ext], [--no-ext]`_

---
# [fit] `bundler gem GEM [OPTIONS]`
# [fit] _`[--ext], [--no-ext]`_
# [fit] Generate the boilerplate for C extension code

---
# [fit] `bundler gem GEM [OPTIONS]`
# [fit] _`[--mit], [--no-mit]`_

---
# [fit] `bundler gem GEM [OPTIONS]`
# [fit] _`[--mit], [--no-mit]`_
# [fit] Generate an MIT license file.

---
# [fit] `bundler gem GEM [OPTIONS]`
# [fit] _`-t, [--test=rspec]`_

---
# [fit] `bundler gem GEM [OPTIONS]`
# [fit] _`-t, [--test=rspec]`_
# [fit] Generate a test directory for your library,
# [fit] either rspec or minitest.

---
# [fit] Why Not
# [fit] Bundler?

* Most useful for the simplest gems
* Not _DRY_
* Questionable Defaults

---
# [fit] Tool: [Hoe][]
## `gem install hoe`
## `sow GEM`

[Hoe]: http://www.zenspider.com/projects/hoe.html

---
# [fit] Why
# [fit] Hoe

* Built for Gem Developers
* Full Development Workflow, Very _DRY_
* Plug-In Based
* Uses a Manifest

---
# [fit] `sow GEM`
# [fit] `sow --style TEMPLATE GEM`

* Templates are in `~/.hoe_template`.
* Only one by default, copied when first run.
* [quik][] may be better than sow, but uses Hoe.

[quik]: https://github.com/rubylibs/quik

---
# [fit] Full Development Workflow
# [fit] Built around Rake

---
# [fit] Full Development Workflow
### `rake` (tests)
### `rake docs`
### `rake dcov` (doc coverage)
### `rake package` (builds)

---
# [fit] Full Development Workflow
# [fit] `rake release VERSION=x.y.z`

* Will not release unless `VERSION=x.y.z` matches your gem version

---
# [fit] Full Development Workflow
# [fit] Also has tasks for announcements, blog posts, etc.

---
# [fit] Very _DRY_
# [fit] Parses README and HISTORY files
# [fit] Finds `VERSION` in your source code

---
# [fit] Plug-In Based
# [fit] Lots of plug-ins

---
## Add otherwise missing features:

* `hoe-doofus` (release checklist)
* `hoe-gemspec2` (create `GEM.gemspec`)
* `hoe-git` (changelog, manifest, and tag management)
* `hoe-travis` (Travis-CI build support)
* `hoe-geminabox` (Private gem server support)
* __more…__

---
# [fit] Why not
# [fit] Hoe?

* Existing templates are idiosyncratic.
* Sharing templates is hard.
* Most useful for simple-to-medium complexity gems.
* *_Very_* opinionated.

---
# [fit] NOTE: More tools
### • [Jeweler][]
### • [rubygems-tasks][]

[Jeweler]: https://github.com/technicalpickles/jeweler
[rubygems-tasks]: https://github.com/postmodern/rubygems-tasks

---
# [fit] Let’s

---
# [fit] Release

---
# [fit] a

---
# [fit] Gem

## (Demo)

---
# [fit] Q&A

---
# [fit] Further
# [fit] Watching

---
# [fit] [Pluck It](http://confreaks.tv/videos/rubyconf2015-pluck-it)
# Adam Cuppy
## RubyConf 2015

Split your code into micro-libraries released as RubyGems.

---
![](https://www.youtube.com/watch?v=r5l0CaxqSvA)

---
# [fit] [Seven Habits of Highly Effective RubyGems](http://confreaks.tv/videos/rubyconf2015-seven-habits-of-highly-effective-gems)
## Mat Brown

Seven good ideas for making and maintaining good RubyGems. I attended this talk
and it’s worth a listen.

---

![](https://www.youtube.com/watch?v=tqLbgS0fw5c)

---
# [fit] [How does Bundler work, anyway?](http://confreaks.tv/videos/rubyconf2015-how-does-bundler-work-anyway)
## Andre Arko

How *does* Bundler work? Why do we need `bundle exec`?

---

![](https://www.youtube.com/watch?v=4DqzaqeeMgY)
