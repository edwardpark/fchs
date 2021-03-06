# Humane Society of Fairfax County

This is the home of the Ruby for Good project to redo the [old site](http://www.hsfc.org/adopt_forms.php) for the Humane Society of Fairfax County.

Issue tracking can be found [here](https://trello.com/b/uiGhjbJI/humane-society-project).

## Getting Started:

    bundle install
    rake db:create db:migrate
    pg_restore db/hsfc_rubyforgood.dump

## cms-admin credentials
    username: admin@rubyforgood.com
    password: password
    
## Managing non-application code (CMS Fixtures):

After pulling latest changes from the remote you need to **import** the fixture files into your local db.

    rake comfortable_mexican_sofa:fixtures:import FROM=example.local TO=localhost
    
When you want to push your changes up to Github and PR in order for others to see and use your changes **export**.

    rake comfortable_mexican_sofa:fixtures:export FROM=localhost TO=example.local

## Contributing:

Branch off of master:

    git checkout -b <name of your feature branch>

Make changes, commit, then push your changes.

    rake db:dump

    git push
    
Submit PR into master.


