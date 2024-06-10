# Shopify Query parameters

There are collections of shopify query parameter, it was hard for me to find them that's why ill add them here for future usage

GENERIC
[store]/[any_url]?section_id=[section_id]

`section_id is the name of the liquid file in the sections folder, this will render the current page with that selected section only. You can fetch this data to get that page html as text response`

PDP

[store]/products/[product_handle]?variant=[variant_id]

`Usefull if you have the variant id, will return data with that variant id selected`

[store]/products/[product_handle]?option_values=[option_values_id]

`will return data for the variant of which those option values ids are selected, if no valid variant can be created with those option, it will return null. Values need to be separated by comma (',')`

[store]/products/[product_handle].json
`return generic product json data does not return selling_plans and metafields`

[store]/products.json

`return a json formated list of all products available to the store these are paginated, default is 30 products per page if you want to increase the limit you can pass the following query, limit is set to 250 max you can get pagination info by passing &page_info`

[store]/products.json?limit=250&page_info

PLP

[store]/collections.json

`returns a list of collection available to the store`

[store]/collections/[collection_handle]/products.json

`return generic json data for products in a specific collection`