# Our first solve

SELECT * FROM blocket_listings
LEFT JOIN received_products
ON blocket_listings.id = received_products.blocket_listing_id
WHERE received_product = 'No'
ORDER BY date;

SELECT * FROM received_payments
WHERE received_payment = 'No';

SELECT * FROM blocket_listings
LEFT JOIN received_products
ON blocket_listings.id = received_products.blocket_listing_id
WHERE received_product = 'No' AND
date < '2019/10/20'
ORDER BY date;

SELECT * FROM blocket_listings
LEFT JOIN received_payments
ON blocket_listings.id = received_payments.bought_item
WHERE received_payment = 'No' AND
blocket_listings.id = 904
ORDER BY date; 

SELECT * FROM blocket_listings
LEFT JOIN received_payments
ON blocket_listings.id = received_payments.bought_item
WHERE received_payment = 'Yes' AND
blocket_listings.id = 85
ORDER BY date; 