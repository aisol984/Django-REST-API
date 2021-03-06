# Django REST API

## Implement a REST API with Django REST Framework to synchronize remote mobile devices executing Tasks.

#### In your model you should represent the concept of a Customer, where each customer has:

An email address

A password

#### Each customer may posses zero or more Devices, where each device has:

A unique UUID

#### For each customer there is a list of Tasks, where each Task has:

An ID (INTEGER)

A state (INTEGER)

#### Devices can execute Tasks. Devices can only execute tasks belonging to their owner. When a device starts executing a task, it has 2 minutes to complete it. Tasks can be retried an arbitrarily large amount of times. Devices have a mobile connectivity and may go offline at any time (may not be able to call any REST API).

The result of an execution of a Task by a Device can be:

Success (in that case the Task is completed)

Failure (the task should be re-executed)

Execution Time Exceeded (the device did not complete in 2 minutes and the task should be re-executed)

#### The same Task can only be executed by one device at a time.
#### One Device can execute at most one Task at a Time.
#### Different Devices can execute different tasks concurrently.