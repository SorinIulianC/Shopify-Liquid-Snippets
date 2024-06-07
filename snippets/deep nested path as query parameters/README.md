# Create a list of Shopify objects

shopify can only nest paths up to 2 levels. Example: `shopify-store/pages/level2/level3` will lead to `shopify-store/pages/level2`
BUT we can still read /level3 since it's a path, and because Shopify does not allow the usage of query params liquid, because of caching issues we can use this trick to pass it as query params.

Purpose of this snippet is to show an example of this. We will use the path to filter a collection and a product from that collection, dynamically.
