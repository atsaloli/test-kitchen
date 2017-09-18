# -*- encoding: utf-8 -*-
source "https://rubygems.org"
gemspec
gem "rack", "< 2.0"

gem "train", "~> 0.22"

gem "chef-telemetry", git: "https://github.com/chef/chef-telemetry.git"

group :integration do
  gem "berkshelf"
  gem "kitchen-inspec"
end

instance_eval(ENV["GEMFILE_MOD"]) if ENV["GEMFILE_MOD"]

# If you want to load debugging tools into the bundle exec sandbox,
# add these additional dependencies into chef/Gemfile.local
eval(IO.read(__FILE__ + ".local"), binding) if File.exist?(__FILE__ + ".local")
