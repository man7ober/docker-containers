## E-Commerce Application (Dockerfile)

**01 - Create a network**

- docker network create micros-network

**02 - Containerize profile-management (Node)**

- docker build -t profile-management .
- docker run --rm -d \
   --name profile-management \
   -p 3003:3003 \
   --network micros-network \
   profile-management

**03 - Containerize shipping-and-handling (Golang)**

- docker build -t shipping-and-handling .
- docker run --rm -d \
   --name shipping-and-handling \
   -p 8080:8080 \
   --network micros-network \
   shipping-and-handling

**04 - Containerize contact-support-team (Flask)**

- docker build -t contact-support-team .
- docker run --rm -d \
   --name contact-support-team \
   -p 8000:8000 \
   --network micros-network \
   contact-support-team

**05 - Containerize product-inventory (Flask)**

- docker build -t product-inventory .
- docker run --rm -d \
   --name product-inventory \
   -p 3002:3002 \
   --network micros-network \
   product-inventory

**06 - Containerize product-catalog (Node)**

- docker build -t product-catalog .
- docker run --rm -d \
   --name product-catalog \
   -p 3001:3001 \
   --network micros-network \
   product-catalog

**07 - Containerize order-management (Java)**

- docker build -t order-management .
- docker run --rm -d \
   --name order-management \
   -p 9090:9090 \
   --network micros-network \
   -e PRODUCT_INVENTORY_API_HOST=http://product-inventory \
   -e PRODUCT_CATALOG_API_HOST=http://product-catalog \
   -e SHIPPING_HANDLING_API_HOST=http://shipping-and-handling \ order-management

**08 - Containerize ecommerce-ui (React + Node)**

- docker build -t ecommerce-ui .
- docker run --rm \
   --name ecommerce-ui \
   -p 4000:4000 \
   --network micros-network \
   -e REACT_APP_PROFILE_API_HOST=http://profile-management \
   -e REACT_APP_SHIPPING_API_HOST=http://shipping-and-handling \
   -e REACT_APP_CONTACT_API_HOST=http://contact-support-team \
   -e REACT_APP_INVENTORY_API_HOST=http://product-inventory \
   -e REACT_APP_PRODUCT_API_HOST=http://product-catalog \
   -e REACT_APP_ORDER_API_HOST=http://order-management \
   ecommerce-ui
