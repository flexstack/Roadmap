# Workers

## Introduction 

Workers (or background workers) are a way to run tasks in the background. They are useful for 
tasks that are not time-sensitive and can be run in the background. For example, sending emails, 
processing images, or updating a database. 

FlexStack workers will automatically scale based on the number of messages in their queue. This means
that you can run as many workers as you need to process your tasks, and FlexStack will automatically
scale them up or down based on the number of messages in the queue.

Because workers will use SQS as their queue, they will be fairly durable and reliable. If a worker
fails to process a message, it will be retried and if it fails too many times, it will be moved to
a dead-letter queue for manual inspection.

## Target date

Q3 2024