# Retail Search
Demo for the Vision API Product Search (https://cloud.google.com/vision/product-search/docs)


## Demo - create product catalog manually

1. Create product set -> create_product_set(product_set_id, product_set_display_name)

2. Create product -> create_product(product_id, product_display_name, product_category)

3. Add product to product set -> add_product_to_product_set(product_id, product_set_id)

4. Add reference image to product -> create_reference_image(product_id, reference_image_id, gcs_uri)

[wait for indexing to trigger] -> [30 mins aprox]

5. Search for similar products -> get_similar_products_uri(product_set_id, product_category, image_uri, filter)


## Demo - bulk import to create product catalog

1. Create csv file -> how to format bulk import csv (https://cloud.google.com/vision/product-search/docs/csv-format)
or you can use this sample one pointing to a public apparel image dataset: (gs://cloud-samples-data/vision/product_search/product_catalog.csv)

2. Import csv file -> import_product_sets(gcs_uri)


[wait for indexing to trigger] -> [30 mins aprox]


3. Search for similar products -> get_similar_products_uri_and_display(product_set_id, product_category, image_uri, filter, threshold)
