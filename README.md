# Notes DevOpsDays Geneva 2022
Programme: https://devopsdays.org/events/2022-geneva/program

## Developer Productivity Engineering - Etienne Studer

Two thirds of GDP digitalized, so given our current way of organizing things
that's quite scary!

Flaky tests - embarrassing re-run the tests.

Working in groups increases pain threshold - which is a bad thing here, because you're not focusing on reducing the pain.

Not to be confused with Developer Productivity Management which is less
scientific.

Issues:

- Takes too long
- Takes too long to fix
- This could have been prevented

These inefficiencies add up.

Capture data about builds.

	dotnet list package --include-transitive

Even builds that are faster than 10 minutes still cause significant waiting time.

### Build Caching
Fully compiled dependencies.

Advantage: You can also reduce CI complexity.

### Predictive Test Selection
Predict the tests that are likely impacted by the change - you want to fail
fast.

https://github.com/microsoft/MSBuildPrediction

### Test distribution
Nothing special to note there, we're quite good at that already.

### Flaky tests
Better to work around it than do nothing at all.

### DPE Playbook
- Capture and measure whenever software is built, locally and on CI
- Reason about the data and derive specific actions
- keep on it


## Tekton: From source to production inside Kubernetes - Giovanni Galloro
Task CRD, composed via Pipeline Custom Resource Definition.

Parametrize the tasks.

Kaniko to build images inside containers, completely userspace https://github.com/GoogleContainerTools/kaniko

CI in Tekton - configure a web hook from the repo that triggers the pipeline run.

There is also a dashboard

## Advanced Authentication patters at the Edge - Denis Jannot
Put a proxy in front, service mesh for in-between-apps.

Envoy: filter chain

OPA - Open Policy Agent for authentication.

## Closing the feedback loop for infrastructure development - Max Andersson

A lot of people using Gitlab. They are also mostly spending less than 10 minutes
per day waiting for their changes to go through CI.

The feedback loop Code -> Build -> Test -> Release -> Deploy -> Operate -> Monitor -> Plan -> Code

But mostly it's just code -> build -> code etc.

### Things to measure
- Lead time: Commit to production
- Deployment Frequency: How many deployments per day
- Mean Time to Restore: If something goes wrong, how long does it take to restore or rollback
- Change Fail Percentage

### The Hare and the Tortoise - Open Source, Standards and Technical Debt - Rapha??l Pinson

The more technical the team, the more you get the Not Invented Here syndrome (can attest).

Idea: contribute more actively to the existing software. Set standards even?

Anecdote: Shared libraries in Linux break printing in KDE.

### Immutability encourages loose coupling

### Cloud providers to the rescue?
The more you lean into one cloud provider's API, the more you will depend on
them in the future.

### Team Topologies

### Tortoise vs Hare
How close are you to the state of the art so that you can get there when a
security issue comes up.






