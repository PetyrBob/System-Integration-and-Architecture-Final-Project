# System Integration Api Documentation Endpoints
## Finals Exam

Peter Bob R. Domogma

John Rymell P. Pabellosa

# **J & B GameHub**

## End Point 1: Get all available games
**Request:**
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
		“game_id”: 001,
                	"game_name": "Valorant",
        		"developer": “Riot Games",
       		"category": "First-Person Shooting Games",
		“released_date: “2 June, 2020”
        		"price": "Free",
        		"advertisement_video": "Video Link"
    		},
    		{
        		“game_id”: 002,
        		"game_name": "League of Legends",
        		"developer": "Riot Games",
        		"category": “Multiplayer Online Battle Arena(MOBA)",
		“released_date: “27 October, 2007”
        		"price": "Free",
        		"advertisement_video": "Video Link"
    		},
    		{
		“game_id”: 003,
                	"game_name": "Minecraft",
        		"developer": “Mojang Studios",
       		"category": "Survival, Multiplayer",
		“released_date: “18 November, 2011”
        		"price": "₱69",
        		"advertisement_video": "Video Link"
    		}
	]
    		
Response(XML):

    <body>
    	<game>
        	<game_id>001</game_id>
        	<game_name>Valorant</game_name>
        	<developer>Riot Games</developer>
        	<category>First-Person Shooting Games</category>
		    <released_date>2 June, 2020</released_date>
        	<price>zFree</price>
        	<advertisement_video>Video Link</advertisement_video>
	    </game>
	    <game>
        	<game_id>002</game_id>
        	<game_name>League of Legends</game_name>
        	<developer>RiotGames</developer>
        	<category>Multiplayer Online Battle Arena(MOBA)</category>
		    <released_date>27 October, 2007</released_date>
        	<price>Free</price>
        	<advertisement_video>Video Link</advertisement_video>
	    </game>
	    <game>
        	<game_id>003</game_id>
        	<game_name>Minecraft</game_name>
        	<developer>Mojang Studios</developer>
        	<category>Survival, Multiplayer</category>
		    <released_date>18 November, 2011</released_date>
        	<price>₱69</price>
        	<advertisement_video>In Stock</advertisement_video>
	    </game>
    <body>




## End Point 2: Filter a games by name
**Request:**
    `GET /api/games/{game_name}`

**Description:**
    Filter a game by name

**Headers:**
    
    Accept: application/json
    Accept: application/xml
**Request(JSON):**
Status code: `200 OK`

	body:
		{
            "game_name": "Tekken 8",
        	"developer": “Bandai Namco",
       		"category": "Martial Arts, Multiplayer",
		    “released_date: “26 Jan, 2024”
        	"price": "₱2799.95",
        	"advertisement_video": "Video Link"
    	},

Response(XML):

	<body>
    	<game>
            <game_name>Tekken 8</game_name>
        	<developer>Bandai Namco Studios</developer>
        	<category>Martial Arts, Multiplayer</category>
		    <released_date>26 Jan, 2024</released_date>
        	<price>₱2799.95</price>
        	<advertisement_video>Video Link</advertisement_video>
	    </game>
	</body>





## End Point 3: Create a game 
**Request:**
    `POST  /api/games`

**Description:**
    Add a new game

**Headers:**
    
    Accept: application/json
    Accept: application/xml
**Request Body(JSON):** Status code: `200 OK`

    body:
		{
            "game_name": "DRAGON BALL: Sparkling! ZERO",
        	"developer": “Spike Chunsoft",
       		"category": "3D Fighter, Multiplayer",
		    “released_date: “11 October, 2024”
        	"price": "₱2799.00",
        	"advertisement_video": "Video Link"
    	},

**Request Body(XML):**

	<body>
    	<game>
        	<game_name>DRAGON BALL: Sparkling! ZERO</game_name>
        	<developer>Bandai Namco Studios</developer>
        	<category>3D Fighter, Multiplayer</category>
		    <released_date>26 Jan, 2024</released_date>
        	<price>₱2799.95</price>
        	<advertisement_video>Video Link</advertisement_video>
	    </game>
	</body>

**Response(JSON):**

    body:
		{
		    “game_id”: 004,
            "game_name": "DRAGON BALL: Sparkling! ZERO",
        	"developer": "Spike Chunsoft",
       		"category": "3D Fighter, Multiplayer",
		    "released_date": “11 October, 2024”
        	"price": "₱2799.00",
        "advertisement_video": "Video Link"
    	},

**Response(XML):**

	<body>
    	<game>
        	<game_id>004</game_id>
        	<game_name>DRAGON BALL: Sparkling! ZERO</game_name>
        	<developer>Bandai Namco Studios</developer>
        	<category>3D Fighter, Multiplayer</category>
	        <released_date>26 Jan, 2024</released_date>
        	<price>₱2799.95</price>
        	<advertisement_video>Video Link</advertisement_video>
	    </game>
	</body>


## End point 4: Update game by ID
**Request:**
   `PUT /api/games/{game_id}`

**Description:**
   Update a game by ID

**Headers:**
    
    Accept: application/json
    Accept: application/xml

**Request Body(JSON):** Status code: `200 OK`

    body:
		{
            "game_name": "Assasin’s Creed Origins",
        	"developer": “Ubisoft Montreal",
       		"category": "Action Role-Playing",
		    “released_date: “27 October, 2017”
        	"price": "₱2200.00",
        	"advertisement_video": "Video Link"
    	},

**Request Body(XML):**

	<body>
    	<game>
            <game_name>Assasin’s Creed Origins</game_name>
            <developer>Ubisoft Montreal</developer>
            <category>Action Role-Playing</category>
		    <released_date>27 October, 2017</released_date>
            <price>₱2200.00</price>
        	<advertisement_video>Video Link</advertisement_video>
	    </game>
	</body>

**Response(JSON):**

    body:
		{
		“game_id”: 006,
                	"game_name": "Assasin’s Creed Origins",
        		"developer": “Ubisoft Montreal",
       		"category": "Action Role-Playing",
		“released_date: “27 October, 2017”
        		"price": "₱2200.00",
        		"advertisement_video": "Video Link"
    	},

**Response(XML):**

	<body>
    	<game>
		<game_id>006</game_id>
        <game_name>Assasin’s Creed Origins</game_name>
        <developer>Ubisoft Montreal</developer>
        <category>Action Role-Playing</category>
		<released_date>27 October, 2017</released_date>
        <price>₱2200.00</price>
        <advertisement_video>Video Link</advertisement_video>
	</game>
	</body>


## End point 5: Add a game to WishList Collection
**Request:**
   `POST /api/games/game_name/game_list`

**Description:**
   
**Headers:**
    
    Accept: application/json
    Accept: application/xml

**Request Body(JSON):** Status code: `200 OK`

	body:
		{
            "game_name": "Red Dead Redemption 2",
        },

Request Body(XML):

	<body>
    	<game>
        <game_name>Red Dead Redemption 2</game_name>
        </game>
	</body>

Response(JSON):

	body:
		{
            "game_name": "Red Dead Redemption 2",
		    "game_name": "Minecraft",
		    "game_name": "Valorant",
        },

Response(XML):
	<body>
    	<game>
            <game_name>Red Dead Redemption 2</game_name>
		    <game_name>Minecraft</game_name>
		    <game_name>Valorant</game_name>
        </game>
	</body>

## End point 6: Get game by ID
**Request:**
   `GET /api/games/{game_id}`

**Description:**
    Retrieve a game by ID

**Headers:**

    Accept: application/json
    Accept: application/xml

**Request Body(JSON):** Status code: `200 OK`

	body:
		{
		    “game_id”: 006,
            "game_name": "Call of Duty: Black Ops 6",
        	"developer": “Treyarch, Raven Software",
       		"category": "FPS",
		    “released_date: “25 October, 2024”
        	"price": "₱3699.00",
        	"advertisement_video": "Video Link"
    	},


**Response(XML):**

	<body>
    	<game>
			<game_id>006</game_id>
        	<game_name>Call of Duty: Black Ops 6</game_name>
        	<developer>Treyarch, Raven Software</developer>
        	<category>FPS</category>
		    <released_date>25 October, 2024</released_date>
        	<price>₱3699.00</price>
        	<advertisement_video>Video Link</advertisement_video>
	</game>
	</body>


## End point 7: Retrieve all games in a collection 
**Request:**
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
        		<game_name>Red Dead Redemption 2</game_name>
		<game_name>Minecraft</game_name>
		<game_name>Valorant</game_name>
        	</games>
	</wishlist>

## End point 8: Delete game by ID
**Request:**
  `DELETE /api/games/{game_id}`

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
**Request:**
  `GET /api/games/{developer}`

**Description:**
   Get games from the developers

Headers:

    Accept: application/json
    Accept: application/xml
**Request Body(JSON):** Status code: `200 OK`

	Body:
    	{
            “game_name”: “Valorant”,
            “game_name”: “League of Legends”,
            “game_name”: “Teamfight Tactics(TFT)”,
    	}


	
## End point 10: Retrieve games by their category
Request:
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
		        "game_name": "Minecraft",
        		"developer": “Mojang Studios",
       		    "category": "Survival, Multiplayer",
		        “released_date: “18 November, 2011”
        		"price": "₱69",
        		"advertisement_video": "Video Link"
    		}
		{
                "game_name": "DRAGON BALL: Sparkling! ZERO",
        		"developer": “Spike Chunsoft",
       		    "category": "3D Fighter, Multiplayer",
		        “released_date: “11 October, 2024”
        		"price": "₱2799.00",
        		"advertisement_video": "Video Link"
    		},
		        "game_name": "Tekken 8",
        		"developer": “Bandai Namco",
       		    "category": "Martial Arts, Multiplayer",
		        “released_date: “26 Jan, 2024”
        		"price": "₱2799.95",
        		"advertisement_video": "Video Link"
    		},
		]


		        “Multiplayer” {
			    “games”: {
				“Minecraft”,
				“DRAGON BALL: Sparkling! ZERO”,
				“Tekken 8”
            }
        }
