# Defaults. For supported versions check .travis.yml
ENV['rails'] ||= '3.2.13'
ENV['orm']   ||= 'active_record'

source 'https://rubygems.org'

# Define Rails version
gem 'rails', ENV['rails']

gem 'database_cleaner', '~> 1.0.0.RC1' if ENV['rails'][0] == '4'

case ENV['orm']
when 'active_record'
  gem 'activerecord'

when 'mongoid2'
  gem 'mongoid', '2.5.1'
  gem 'bson_ext', '~> 1.7'

when 'mongoid3'
  gem 'mongoid', '3.0.10'
  
when 'monogid4'
  gem "mongoid", '~> 4', github: 'mongoid/mongoid', ref: '9b3bc1264032209b7a6c0e82d0ca656f401e476b'
  gem "bson_ext"

when 'mongo_mapper'
  gem 'mongo_mapper', '0.12.0'
  gem 'bson_ext', '~> 1.7'

end

gemspec
