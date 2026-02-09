# zoomcamp-data-warehouse

```


SELECT COUNT(*) FROM `terraform-demo-484500.zoomcamp.yellow_tripdata_2024`


SELECT COUNT(DISTINCT(pu_location_id)) FROM `terraform-demo-484500.zoomcamp.yellow_tripdata_2024`


SELECT COUNT(DISTINCT(pu_location_id)) FROM `terraform-demo-484500.zoomcamp.yellow_tripdata_2024_material`


CREATE TABLE zoomcamp.rides_optimized
PARTITION BY DATE(tpep_dropoff_datetime)
CLUSTER BY vendor_id AS
SELECT *
FROM `zoomcamp.yellow_tripdata_2024_material`;


SELECT DISTINCT vendor_id
FROM `terraform-demo-484500.zoomcamp.yellow_tripdata_2024_material`
WHERE DATE(tpep_dropoff_datetime) BETWEEN '2024-03-01' AND '2024-03-15'
ORDER BY vendor_id;

```
