# GET /artists Route Design Recipe
Copy this design recipe template to test-drive a Sinatra route.

# 1. Design the Route Signature
You'll need to include:

* the HTTP method => GET
* the path => /artists
* any query parameters (passed in the URL) => no
* or body parameters (passed in the request body) => Pixies, ABBA, Taylor Swift, Nina Simone

# 2. Design the Response
The route might return different responses, depending on the result.

For example, a route for a specific blog post (by its ID) might return 200 OK if the post exists, but 404 Not Found if the post is not found in the database.

Your response might return plain text, JSON, or HTML code.

Replace the below with your own design. Think of all the different possible responses your route will return.

Response when the post is found: 200 OK

Pixies, ABBA, Taylor Swift, Nina Simone


# 3. Write Examples
Replace these with your own design.
```ruby
# Request:
GET /artists

# Expected response:
Response for 200 OK
```
# 4. Encode as Tests Examples
# EXAMPLE
# file: spec/integration/application_spec.rb
```ruby
require "spec_helper"

describe Application do
  include Rack::Test::Methods

  let(:app) { Application.new }

  context "get /artists" do
    it 'should get a list of all artists' do
      # Assuming the post with id 1 exists.
      response = get('/artists')

      expect(response.status).to eq(200)
      expect(response.body).to eq("Pixies, ABBA, Taylor Swift, Nina Simone")
    end
  end
end

# app.rb

get '/artists/' do
  repo = ArtistRepository.new
  artist = Artist.new
  artist.name = params[:name]
  return ''
end
```
# 5. Implement the Route
Write the route and web server code to implement the route behaviour.