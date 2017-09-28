# Introduction

This repository is a simple test one.
No real code should be submitted here, as all can be removed without any notice.

It currently implements a simple noop pipeline, with Jenkinsfile.

Thanks

Used for tests with github with versions fixes and more with just a job configured. Nothing on server side...
But we need a credential user/passwd registered and attached to the organization folder.

Forjj now is able to reproduce that behavior with jobdsl... 
Unfortunately all can't be done by standard dsl. This said, jobdsl itself has a parade for that, dealing with underlying XML data. It is called `configure`.

Here is the documentation to follow:
http://www.devexp.eu/2014/10/26/use-unsupported-jenkins-plugins-with-jenkins-dsl/

The complexity here is the need to create multiple source repo, to match what forjj do today.
The key thing is :
- If the overall organization must uses the same flow, we just need the organization list.
- otherwise, we should list all repo where each may have different flow.

For the exercise, I will do the 2nd option.

last try just after jobdsl run... Success.

I created both option. All works fine.

Now, I'm testing the standard pipeline with source from github...
with jobdsl. The dsl is totally different... It really depends on how the plugin is going to be managing this relationship with jobdsl...

Without the need to add a configure, the default behaviours are applied (2) 
It looks like a work is in transition in this subject, where old behavior is still connected and created new data in the job config.

So, I can use that syntax for forjj-jenkins, now, as it will create those pipeline as usual. I just need to verify what happened if I set the api-uri...

Forj Team
