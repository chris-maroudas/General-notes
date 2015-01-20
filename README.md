# General-notes

#### CanCanCan
In every admin controller which has model you add this:
`load_and_authorize_resource`

And in controller without model
`load_and_authorize_resource class: false`