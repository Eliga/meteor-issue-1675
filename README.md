meteor-issue-1675
=================

Meteor Issue 1675 : "lib order"

Documentation says : 
>Files in the lib directory at the root of your application are loaded first.

but if you organize your app with modules directory structure, you get :

> app/lib/some_code.js

loaded AFTER :

> app/module/lib/some_other_code.js

It seems it's rather : 
> Files in the deepest directory, with a lib part,  are loaded first.

