# Redis (RedisFailover)

Redis HA instance via **Spotahome RedisFailover** CR in namespace **redis**. Install **redis-operator** (operator/) in cluster-tools first.

**Hostname for apps:** `redis-master.redis.svc.cluster.local` (port 6379). Optional: auth via 1Password and ExternalSecret (add to chart if needed).

---

## Requirements

- **redis-operator** chart (operator/) installed in cluster-tools.
- Namespace **redis**.
- **Nodes:** Soft affinity to nodes with label **node-role=database** (homelab convention).
- **PDB:** Chart creates PodDisruptionBudgets so only one Redis and one Sentinel pod can be down at a time.
