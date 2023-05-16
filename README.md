# Leasing App
Daml templates designed for a platform for leasing agreements.

### I. Overview 
This project was created by using the `empty-skeleton` template. The project adopts and exemplifies the `proposal-accept` design pattern.

A landlord or tenant can propose a lease on a property to the other.
The counterparty can accept, reject or make a counter proposal.
When both parties agree, a lease agreement is reached.

The proposing party can recall an outstanding lease proposal at any time.

### II. Example Workflow
1. A landlord creates a LeaseProposal, adding the tenant as an observer.
2. The tenant exercises the Counter choice on the LeaseProposal with a slightly lower rate, archiving the old LeaseProposal and creating a new one.
3. The landlord exercises the Counter choice on the LeaseProposal, meeting in the middle.
4. The tenant exercises the Accept choice on the LeaseProposal and a new Lease contract is created.

### III. Building
To compile the project
```
$ daml build
```

### IV. Testing
Run:
```
$ daml test
```

### V. Running
To load the project into the sandbox and start navigator:
```
$ daml start
```