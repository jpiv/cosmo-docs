---
icon: cloud-binary
---

# Persisted Queries

The router supports two distinct features, both dealing with persisted queries.&#x20;

* **Persisted operations** allow you to register queries / mutations / subscriptions within a federated graph, enabling the clients to send just an identifier in their request instead of sending the whole operation body. These operations need to be registered ahead of time, using the `wgc operations push` command, and can be run by sending the hash of the command to the router.&#x20;
* **Automatic Persisted Queries (APQ)** enables the system to automatically persist queries that are sent to it in a designated format, which can then be run again by sending the hash of the command to the router (even via GET operations through a CDN).