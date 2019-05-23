To get started, let us login to the OpenShift cluster by running the following:

``oc login -u developer -p developer``{{execute}}

Now let's verify that you're logged in as a developer _note: due to a temporary Katakoda bug, you may have to issue the oc login command twice_

``oc whoami``{{execute}}

Output should be as follows:
```
developer
```

To begin, let's create a new directory and go into it.

``mkdir sample-applier; cd sample-applier``{{execute}}

To complete the generic project structure, we want to create the rest of these:

```
.
├── inventory
│   ├── group_vars
│   │   └── all.yml
│   └── hosts
├── params
│   ├── ruby
│   └── projectrequests
├── projectrequests
├── requirements.yml
└── templates
    ├── app
    └── project
```

Let's go ahead and create that structure:

```
mkdir -p inventory/group_vars params/{ruby,projectrequests} templates/{app,project}
```{{execute}}

And now the files:

``` 
touch inventory/group_vars/all.yml inventory/hosts requirements.yml
```{{execute}}
