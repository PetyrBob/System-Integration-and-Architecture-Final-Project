# System Integration Api Documentation Endpoints
# Final Exam

Peter Bob R. Domogma

John Rymell P. Pabellosa

# **J & B GameHub**
## Base URL

    https://api.jandbgames.com/v1



## End Point 1: Get all available games
- **Request:**
    `GET /api/games`

**Description:**
    Retrieve all available F2P and P2P games

**Headers:**
    
    Accept: application/json
    Accept: application/xml

**Response(JSON):**
Status code: `200 OK`

     Body:
	[
    	{
		    	“id”: 001,
                "name": "Valorant",
        		"developer": “Riot Games",
       		    "category": "First-Person Shooting Games",
		        “released: “2 June, 2020”
        		"price": "Free",
        		"advertisement": "Video Link"
    		},
    		{
        		“id”: 002,
        		"name": "League of Legends",
        		"developer": "Riot Games",
        		"category": “Multiplayer Online Battle Arena(MOBA)",
		        “released: “27 October, 2007”
        		"price": "Free",
        		"advertisement": "Video Link"
    		},
    		{
		        “id”: 003,
                "name": "Minecraft",
        		"developer": “Mojang Studios",
       		    "category": "Survival, Multiplayer",
		        “released: “18 November, 2011”
        		"price": "₱69",
        		"advertisement": "Video Link"
    		}
	]
    		
Response(XML):

    <body>
    	<game>
        	<id>001</id>
        	<name>Valorant</name>
        	<developer>Riot Games</developer>
        	<category>First-Person Shooting Games</category>
		    <released>2 June, 2020</released>
        	<price>zFree</price>
        	<advertisement>Video Link</advertisement>
	    </game>
	    <game>
        	<id>002</id>
        	<name>League of Legends</name>
        	<developer>RiotGames</developer>
        	<category>Multiplayer Online Battle Arena(MOBA)</category>
		    <released>27 October, 2007</released>
        	<price>Free</price>
        	<advertisement>Video Link</advertisement>
	    </game>
	    <game>
        	<id>003</id>
        	<name>Minecraft</name>
        	<developer>Mojang Studios</developer>
        	<category>Survival, Multiplayer</category>
		    <released>18 November, 2011</released>
        	<price>₱69</price>
        	<advertisement>In Stock</advertisement>
	    </game>
    <body>




## End Point 2: Filter a games by name
- **Request:**
    `GET /api/games/{name}`

**Description:**
    Filter a game by name

**Headers:**
    
    Accept: application/json
    Accept: application/xml
**Request(JSON):**
Status code: `200 OK`

	Body:
		{
            "name": "Tekken 8",
        	"developer": “Bandai Namco",
       		"category": "Martial Arts, Multiplayer",
		    “released: “26 Jan, 2024”
        	"price": "₱2799.95",
        	"advertisement": "Video Link"
    	},

Response(XML):

	<body>
    	<game>
            <name>Tekken 8</name>
        	<developer>Bandai Namco Studios</developer>
        	<category>Martial Arts, Multiplayer</category>
		    <released>26 Jan, 2024</released>
        	<price>₱2799.95</price>
        	<advertisement>Video Link</advertisement>
	    </game>
	</body>





## End Point 3: Create a game 
- **Request:**
    `POST  /api/games`

**Description:**
    Add a new game

**Headers:**
    
    Accept: application/json
    Accept: application/xml
**Request Body(JSON):** Status code: `200 OK`

    body:
		{
            "name": "DRAGON BALL: Sparkling! ZERO",
        	"developer": “Spike Chunsoft",
       		"category": "3D Fighter, Multiplayer",
		    “released: “11 October, 2024”
        	"price": "₱2799.00",
        	"advertisement": "Video Link"
    	},

**Request Body(XML):**

	<body>
    	<game>
        	<name>DRAGON BALL: Sparkling! ZERO</name>
        	<developer>Bandai Namco Studios</developer>
        	<category>3D Fighter, Multiplayer</category>
		    <released>26 Jan, 2024</released>
        	<price>₱2799.95</price>
        	<advertisement>Video Link</advertisement>
	    </game>
	</body>

**Response(JSON):**

    body:
		{
		    “id”: 004,
            "name": "DRAGON BALL: Sparkling! ZERO",
        	"developer": "Spike Chunsoft",
       		"category": "3D Fighter, Multiplayer",
		    "released": “11 October, 2024”
        	"price": "₱2799.00",
            "advertisement": "Video Link"
    	},

**Response(XML):**

	<body>
    	<game>
        	<id>004</id>
        	<name>DRAGON BALL: Sparkling! ZERO</name>
        	<developer>Bandai Namco Studios</developer>
        	<category>3D Fighter, Multiplayer</category>
	        <released>26 Jan, 2024</released>
        	<price>₱2799.95</price>
        	<advertisement>Video Link</advertisement>
	    </game>
	</body>


## End point 4: Update game by ID
- **Request:**
   `PUT /api/games/{id}`

**Description:**
   Update a game by ID

**Headers:**
    
    Accept: application/json
    Accept: application/xml

**Request Body(JSON):** Status code: `200 OK`

    body:
		{
            "name": "Assasin’s Creed Origins",
        	"developer": “Ubisoft Montreal",
       		"category": "Action Role-Playing",
		    “released: “27 October, 2017”
        	"price": "₱2200.00",
        	"advertisement": "Video Link"
    	},

**Request Body(XML):**

	<body>
    	<game>
            <name>Assasin’s Creed Origins</name>
            <developer>Ubisoft Montreal</developer>
            <category>Action Role-Playing</category>
		    <released>27 October, 2017</released>
            <price>₱2200.00</price>
        	<advertisement>Video Link</advertisement>
	    </game>
	</body>

**Response(JSON):**

    body:
		{
		    “id”: 006,
            "name": "Assasin’s Creed Origins",
        	"developer": “Ubisoft Montreal",
       		"category": "Action Role-Playing",
		    “released: “27 October, 2017”
        	"price": "₱2200.00",
        	"advertisement": "Video Link"
    	},

**Response(XML):**

	<body>
    	<game>
		<id>006</id>
        <name>Assasin’s Creed Origins</name>
        <developer>Ubisoft Montreal</developer>
        <category>Action Role-Playing</category>
		<released>27 October, 2017</released>
        <price>₱2200.00</price>
        <advertisement>Video Link</advertisement>
	</game>
	</body>


## End point 5: Add a game to WishList Collection
- **Request:**
   `POST /api/games/name/game_list`

**Description:**
   
**Headers:**
    
    Accept: application/json
    Accept: application/xml

**Request Body(JSON):** Status code: `200 OK`

	body:
		{
            "name": "Red Dead Redemption 2",
        },

Request Body(XML):

	<body>
    	<game>
        <name>Red Dead Redemption 2</name>
        </game>
	</body>

Response(JSON):

	body:
		{
            "name": "Red Dead Redemption 2",
		    "name": "Minecraft",
		    "name": "Valorant",
        },

Response(XML):
	<body>
    	<game>
            <name>Red Dead Redemption 2</name>
		    <name>Minecraft</name>
		    <name>Valorant</name>
        </game>
	</body>

## End point 6: Get game by ID
- **Request:**
   `GET /api/games/{id}`

**Description:**
    Retrieve a game by ID

**Headers:**

    Accept: application/json
    Accept: application/xml

**Request Body(JSON):** Status code: `200 OK`

	body:
		{
		    “id”: 006,
            "name": "Call of Duty: Black Ops 6",
        	"developer": “Treyarch, Raven Software",
       		"category": "FPS",
		    “released: “25 October, 2024”
        	"price": "₱3699.00",
        	"advertisement": "Video Link"
    	},


**Response(XML):**

	<body>
    	<game>
			<id>006</id>
        	<name>Call of Duty: Black Ops 6</name>
        	<developer>Treyarch, Raven Software</developer>
        	<category>FPS</category>
		    <released>25 October, 2024</released>
        	<price>₱3699.00</price>
        	<advertisement>Video Link</advertisement>
	</game>
	</body>


## End point 7: Retrieve all games in a collection 
- **Request:**
     `HEAD /api/games/game_list`

**Description:**
Get all the games in a wishlist collection
   
**Headers:**

    Accept: application/json
    Accept: application/xml
**Request Body(JSON):** Status code: `200 OK`

	body:
		{ 
            "wishlist": { 
            "games": [ 
            "Red Dead Redemption 2", 
            "Minecraft", 
            "Valorant" 
                ] 
            } 
        },

**Response(XML):**

	<wishlist>
    		<games>
        	<name>Red Dead Redemption 2</name>
		    <name>Minecraft</name>
		    <name>Valorant</name>
        	</games>
	</wishlist>

## End point 8: Delete game by ID
- **Request:**
  `DELETE /api/games/{id}`

**Description:**
   Deletes a game by ID

**Headers:**

    Accept: application/json
    Accept: application/xml
**Request Body(JSON):** Status code: `200 OK`

	body:
		{
            "message": “Game has been successfully deleted”
        },
**Response(JSON):**

	<body>
		<message>Game has been successfully deleted.</message>
	</body>


## End point 9: Retrieve games by the developer
- **Request:**
  `GET /api/games/{developer}`

**Description:**
   Get games from the developers

Headers:

    Accept: application/json
    Accept: application/xml
**Request Body(JSON):** Status code: `200 OK`

	Body:
    	{
            “name”: “Valorant”,
            “name”: “League of Legends”,
            “name”: “Teamfight Tactics(TFT)”,
    	}


	
## End point 10: Retrieve games by their category
- Request:
  `GET /api/games/{category}`

**Description:**
   Get games by the category
**Headers:**

    Accept: application/json
    Accpet: application/xml
**Request Body(JSON):** Status code: `200 OK`
		
	   Body:
		[
    		{
		        "name": "Minecraft",
        		"developer": “Mojang Studios",
       		    "category": "Survival, Multiplayer",
		        “released: “18 November, 2011”
        		"price": "₱69",
        		"advertisement": "Video Link"
    		}
		{
                "name": "DRAGON BALL: Sparkling! ZERO",
        		"developer": “Spike Chunsoft",
       		    "category": "3D Fighter, Multiplayer",
		        “released: “11 October, 2024”
        		"price": "₱2799.00",
        		"advertisement": "Video Link"
    		},
		        "name": "Tekken 8",
        		"developer": “Bandai Namco",
       		    "category": "Martial Arts, Multiplayer",
		        “released: “26 Jan, 2024”
        		"price": "₱2799.95",
        		"advertisement": "Video Link"
    		},
		]


		        “Multiplayer” {
			    “games”: {
				“Minecraft”,
				“DRAGON BALL: Sparkling! ZERO”,
				“Tekken 8”
            }
        }
