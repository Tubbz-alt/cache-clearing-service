require_relative "app/environment"

begin
  require "rspec/core/rake_task"
  RSpec::Core::RakeTask.new(:spec)
rescue LoadError # rubocop:disable Lint/SuppressedException
end

Dir.glob("lib/tasks/*.rake").each { |r| load r }

task default: %i[spec lint]
