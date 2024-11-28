Should we use upcastors in Event Sourcing?

First of all, what are upcasters?

This has long been a practice that's been used in Event Sourcing as a way to migrate data from one version of an event to the next. For example, if we have an event called "UserRegistered", we might want to add a field to the event for storing the user's date of birth in addition ot the existing fields such as name, email and address.

The idea is that we don't really want to deal with the old event so our code will be only concerned with the current version of the event. But we know that in event sourcing, we store all events in the system and those that we were using last year, have the previous schema.

So we need to be able to take the old event and convert it to the new event. These are typically functions that take in an event of one version and return an event of the next version. For simple cases, this often is just populating the extra field with a null, empty string, zero or other default value.

Why is this a problem?

Looking at the nature of event sourcing, it is like accouning that presevres to keep an accurate history. So by removing the logic that used the old event, we lose the ability to see the history of how the event evolved with respect to all the different uses of it over time. 

problem 2

The complexity of the extra code that we would need to have to handle the old versions of the events does not get in the way of working with the current version of the event. Event sourced systems observe this Open Closed Principle at a higher level and it really isn't a challenge to work with the old event handlers sitting alongside the new one.





