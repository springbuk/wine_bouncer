# frozen_string_literal: true

source 'https://rubygems.org'

ENV['grape'] ||= '1.3.0'
ENV['rails'] ||= '~> 6.0.0'
ENV['doorkeeper'] ||= '5.0.0'

gem 'rails', ENV['rails']
# ActiveRecord 5 needs sqlite3 ~> 1.3 and ActiveRectod 6 needs ~>1.4
gem 'sqlite3', ENV['rails'].match(/5\.\d\.\d/) ? '~> 1.3.6' : '~> 1.4.2'

# Change in the rack response API broke grape <1.3
# Version lock rack for those versions of grape
gem 'rack', '2.0.8' unless ENV['grape'].match(/1\.3\.\d/)

gem 'doorkeeper', ENV['doorkeeper']
gem 'grape', ENV['grape']

# Specify your gem's dependencies in wine_bouncer.gemspec
gemspec
