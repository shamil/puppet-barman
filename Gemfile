source ENV['GEM_SOURCE'] || "https://rubygems.org"

group :development, :unit_tests do
  gem 'rake',                    :require => false
  gem 'json_pure', '<= 2.0.1',   :require => false if Gem::Version.new(RUBY_VERSION) < Gem::Version.new('2.0.0')
  gem 'rspec-core',              :require => false
  gem 'rspec-puppet',            :require => false
  gem 'puppetlabs_spec_helper',  :require => false
  gem 'puppet-lint',             :require => false
  gem 'simplecov',               :require => false
  gem 'puppet_facts',            :require => false
  gem 'json',                    :require => false
  gem 'metadata-json-lint',      :require => false
  gem 'iconv',                   :require => false
  gem 'rubocop',                 :require => false
  gem 'rubocop-rspec',           :require => false
  gem 'rubocop-i18n',            :require => false
  gem 'parallel_tests',          :require => false
  gem 'librarian-puppet', '>= 2.0'
end

group :development do
  gem 'puppet-blacksmith', git: 'https://github.com/deric/puppet-blacksmith'
  gem 'pdk', '>= 1.0'
end

group :system_tests do
  gem 'beaker-rspec',  :require => false
  gem 'serverspec',    :require => false
end

if facterversion = ENV['FACTER_GEM_VERSION']
  gem 'facter', facterversion, :require => false
else
  gem 'facter', :require => false
end

if puppetversion = ENV['PUPPET_GEM_VERSION']
  gem 'puppet', puppetversion, :require => false
else
  gem 'puppet', :require => false
end

# vim:ft=ruby
