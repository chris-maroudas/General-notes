# General-notes

#### CanCanCan
In every admin controller which has model you add this:

```haml
load_and_authorize_resource

And in controller without model

```haml
load_and_authorize_resource class: false