# my-company-project-materialized-view

The event processor is stateless and listens for events from the event store, applying an action for incoming event messages.
Each event is used to update a database record that results in an incremental materialized view for describing an aggregate.
