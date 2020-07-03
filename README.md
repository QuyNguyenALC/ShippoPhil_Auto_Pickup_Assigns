1. Build your images as defined by docker-compose.yml
   docker-compose build
2. Run the built images as local containers (-d to do it in the background)
   docker-compose up -d

3. Launch a shell from inside the app container
   docker-compose exec app bash

4. Stop the running containers
   docker-compose stop
  
  Then run the jupyter notebook:
  jupyter notebook --ip 0.0.0.0 --no-browser --allow-root
   
About this project:
Shippo Philippines is the last-mile delivery. The process of an order is after new order created, the shipper will 
come and pick up the packages with a pickup-request, which is manually created by an operator. If the new order creates 
while the shipper is in a delivery process who is the available and nearest with the pickup location, we can auto-assign 
a requested pickup for him to get the packages. This project will solve it.
Thus, this project will follow some tasks:
1/ Determine the realtime location of Shipper.
2/ Receive pickup request and mapping location.
3/ Finding the optimize shipper satisfy the requirement (Nearest, Available).
4/ Auto-assign for the shipper, who we found from the previous step.