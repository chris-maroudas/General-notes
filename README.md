# General-notes

#### CanCanCan
In every admin controller which **has model** you add this:
`load_and_authorize_resource`

And in every controller **without a model**
`load_and_authorize_resource class: false`

Inside `admin_ability.rb` you need to declare the *non-model* authorizations with a symbol *not* a class
For example,
`can :manage, Article`
`can :manage, :dashboard`

#### Translations
If a model has translations include a default scope in your model to avoid N+1 queries

`default_scope -> { includes(:translations) }`

####Style guide
Code should follow the official Rails guide (https://github.com/bbatsov/rails-style-guide)

####Notes
Leave notes in code with:

`#TODO: Refactor method`

`#FIXME: Fix this bug`

and see an overview of them with rake:notes

####Indexes
You should index:

Foreign keys

Fields that you search or sort by

On join tables, you should index:
key1, key2, [key1, key2], [key2, key1]

#### Contribute

#####To contribute to this repo
1. Fork the project
2. `git clone your_forked_repo.git`
3. Add your content (markdown basics can be found at (https://help.github.com/articles/markdown-basics/))
4. `commit` and `push` to your master branch and open a pull request

#####To keep your fork up to date
1. `git remote add upstream git@github.com:aypn0s/General-notes.git`
2. `git fetch upstream` to update your local repo with the latest changes. This creates an `upstream/master' branch
3. Merge created branch with your master branch `git merge upstream/master`
4. Push changes to your github remote repo `git push`