source "https://rubygems.org"
gemspec

# Rubinius 2.0 distributes the standard library as gems
platform :rbx do
  stdlibs = %w(benchmark cgi coverage delegate erb find logger net-http open-uri
               optparse ostruct prettyprint singleton tempfile tmpdir yaml)
  stdlibs.each { |lib| gem "rubysl-#{lib}", "~> 2.0" }
  # rubysl-test-unit 2.0.2's gemspec relaxed its dependency on minitest to allow
  # any version (previously, it specified "~> 4.7"). Minitest 5 doesn't have a
  # Test::Unit compatibility layer like 4.x, so it doesn't work with Test::Unit
  # at all (see e.g. https://github.com/seattlerb/minitest/issues/358). So, I'm
  # holding this one back until we find out what's going on.
  gem "rubysl-test-unit", "2.0.1"
  gem "psych", "~> 2.0"
end
