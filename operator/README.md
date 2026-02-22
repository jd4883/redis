# redis-operator

Installs the **Spotahome Redis operator** so you can manage Redis via **RedisFailover** CRs. Deploy this chart in **cluster-tools**. The actual Redis instance is deployed by the **redis** chart in this repo (**cluster/**) in namespace **redis**.

---

## Requirements

| Dependency | Notes |
|------------|--------|
| Namespace | **cluster-tools** (e.g. `helm install -n cluster-tools`). |

---

## Render

> `helm dependency update . && helm template redis-operator . -f values.yaml -n cluster-tools`

---

## Next steps

Install the **redis** chart (cluster/) in namespace **redis** to create the RedisFailover. Hostname for apps: **`redis-master.redis.svc.cluster.local`**.
