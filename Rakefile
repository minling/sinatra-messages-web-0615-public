task :environment do
  require_relative './config/environment'
end

namespace :db do
  task :migrate => :environment do
    ActiveRecord::Migrator.migrate('db/migrate')
  end

  task :rollback => :environment do
    ActiveRecord::Migrator.rollback('db/migrate')
  end

  task :drop => :environment do
    ActiveRecord::Migrator.migrate('db/migrate', 0)
  end
end

task :console => :environment do
  Pry.start
end
