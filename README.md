Вот таблица в формате Markdown, подготовленная специально для вашего `README.md` файла, согласно вашим требованиям:

| NAME | PROMPT | DESCRIPTION | EXAMPLE |
| :--- | :--- | :--- | :--- |
| **Base Deployment** | "Generate a K8s Deployment for a Python Flask app with 3 replicas and port 8080." | Стандартизирует базовую доступность приложения и структуру подов. | [app.yaml](./yaml/app.yaml) |
| **Liveness Probe** | "Add a liveness probe to the Flask deployment checking /health every 10s with a 5s delay." | Автоматически перезапускает контейнеры при зависании или внутренних сбоях. | [app-livenessProbe.yaml](./yaml/app-livenessProbe.yaml) |
| **Readiness Probe** | "Configure a readiness probe for the app to ensure traffic only flows when /ready returns 200." | Исключает простои при обновлении, направляя трафик только на готовые поды. | [app-readinessProbe.yaml](./yaml/app-readinessProbe.yaml) |
| **Volume Mounts** | "Add a persistent volume mount to /data using a PVC named 'app-data-pvc'." | Обеспечивает сохранность данных приложения между перезапусками подов. | [app-volumeMounts.yaml](./yaml/app-volumeMounts.yaml) |
| **CronJob Task** | "Create a K8s CronJob that runs a database cleanup script every night at 2 AM." | Автоматизирует регулярное обслуживание базы данных без ручного вмешательства. | [app-cronjob.yaml](./yaml/app-cronjob.yaml) |
| **Batch Job** | "Define a K8s Job to run a one-time data migration script with a completion limit." | Гарантирует успешное выполнение разовых задач миграции данных. | [app-job.yaml](./yaml/app-job.yaml) |
| **Multi-container** | "Modify the deployment to include a Fluentd sidecar container for log collection." | Реализует паттерн Sidecar для централизованного сбора логов инфраструктуры. | [app-multicontainer.yaml](./yaml/app-multicontainer.yaml) |
| **Resource Limits** | "Apply CPU/Memory limits and requests to the pod to prevent cluster-wide OOM kills." | Оптимизирует затраты на кластер и предотвращает влияние «шумных соседей». | [app-resources.yaml](./yaml/app-resources.yaml) |
| **Secret Injection** | "Inject DB credentials into the pod via environment variables using a K8s Secret." | Повышает безопасность, разделяя конфиденциальные данные и код приложения. | [app-secret-env.yaml](./yaml/app-secret-env.yaml) |
