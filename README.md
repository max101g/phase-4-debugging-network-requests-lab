# Add a new toy when toy form is submitted
How i debugged:

Errors encounteres => internal server error, uninitialized constant Toys in ToysController
Solution :
  Check the update action in the ToysController
  Here is the error found :toy = Toys.find_by(id: params[:id])
  change the Toys to Toy

# Update the number of likes for a toy
How i debagged:

Errors encountered => unexpected end of Json input, unrecognized staus code :updated
Solution:
  Check the fetch request
  Check the controller update action to make sure it renders a json
  change the status code to Status: :ok

# Donate a toy to Goodwill(delete the toy from database) 
How i debagged:

Errors encountered => Not found, No routes match for /[Delete]\
Solution:
  check the route.rb file and ensure the destroy route is included