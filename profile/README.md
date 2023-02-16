<div align="center"> 
   <a href="https://discoverit2208.vercel.app/">
<img src="https://user-images.githubusercontent.com/108088961/219437996-b2e9a496-bbf6-40e3-bd24-935c9df9e6d6.png" width="60%" height="60%"></a>
</div>

---
### Project Description
   A user can search for a city and get a big picture 'snapshot' of the notable things in that city - list of the museums, top restaurants, etc based off of criteria they define. 
<br>

:earth_americas: [Learning Goals](#learning-goals)
<br>
:earth_americas: [Deployment](#deployment)
<br>
:earth_americas: [Repositories](#repositories)
<br>
:earth_americas: [Planning](#planning)
<br>
:earth_americas: [Endpoints](#endpoints)
<br>
:earth_americas: [Tech Stack](#tech-stack)
<br>
:earth_americas: [Contributors](#contributors)
<br>

### Learning Goals
- Use an agile process to turn well defined requirements into deployed and production ready software
- Gain experience dividing applications into components and domains of responsibilities to facilitate multi-developer teams. Service oriented     architecture concepts and patterns are highly encouraged.
- Explore and implement new concepts, patterns, or libraries that have not been explicitly taught while at Turing
- Practice an advanced, professional git workflow including a Pull Request Review
- Gain experience using continuous integration tools to build and automate the deployment of features
- Build applications that execute in development, test, CI, and production environments
- Focus on communication between front-end and back-end teams in order to complete and deploy features that have been outlined by the project spec


### Deployment
   * [Check out our live app here!](https://discoverit2208.vercel.app/)


### Repositories
   * [Backend Repository](https://github.com/DiscoverIt-2208/DiscoverIt-2208-BE)
   * [Frontend Repository](https://github.com/DiscoverIt-2208/DiscoverIt-2208-FE)


### Planning
   * [Our planning miro board](https://miro.com/app/board/uXjVPsXFTmY=/)
   * [Daily standup form](https://forms.gle/o8uT9dCMNmHPEj1n7)
   * [MVP Proposal](https://docs.google.com/document/d/1zh159QSWUgpQ51-qvm1RADbU4RuLf_LI1CyZz_HZR9k/edit)


### Endpoints
All requests use GraphQL queries and mutations at the following URL:

    https://discover-it.herokuapp.com/

#### GraphQL Queries
  * User:
    ```
    user(id:) {
      id: Integer
      name: String
      email: String
      password: String
      favorites: [
        FavoriteType
      ]
      created_at
      updated_at
    }
    ```
  * User example query to get list of favorites belonging to user with id 1 and the desired fields for the favorite type:
    ```
    { 
      user(id: 1) {
        favorites{
         placeId 
         placeName 
         city}
       }
     }
    ```
  * Favorite type fields (note: favorite itself cannot be directly queried, the entire list of favorites for a specific user has to be queried through said user as shown above):
      ```
      favorite {
      id: Integer
      user: Usertype
      placeID: String
      thumnbailUrl: String
      city: String
      country: String
      state: String
      address: String
      createdAt: DateTime
      updatedAt: DateTime
    }
      ```
  * Fetch Places - key value pairs between the parenthesis are arguments (returns a list of places (each being a PlaceType with the fields show below in the curly brackets): 
      ```
      places (city: String, country: String, categories: [String], page: Integer, radius: Integer) {
        name: String
        address: String
        place_id: String
        categories: [
          String
        ]
        city: String
        country: String
        lat: Float
        lon: Float
      }
      ```
      * Example query to get places in Denver with a category of tourism:
      ```
      {places(
                city: "Denver"
                country: "United States"
                categories: ["tourism"]
                page: 0
              ) {
                  name
                  address
                  placeId
                  categories
                  lat
                  lon
                }
      }
      ```
#### GraphQL Mutations
   * Create User Favorite example query (input field is supplied with an input hash) that gives back a success or error message based on whether the place has been added successfully or if the favorite already exists):
      ```
      mutation CREATE_USER_FAVORITE {
        createUserFavorite(input: {userId: 1, 
                                  placeId: "513340fdc206bc5ec059039010feea844740f00103f9012a0f3f090200000092030e506c616e6574204669746e657373", 
                                  placeName: "Planet Fitness", 
                                  thumbnailUrl: "", 
                                  city: "Olympia", 
                                  state: "Washington",
                                  country: "United States",
                                  address: "Planet Fitness, 1000 Cooper Point Road Southwest, Olympia, WA 98502, United States of America"}) {success error}
                                  }
      ```
      * Delete User Favorite example query (input field is supplied with an input hash) that removes a favorite):
      ```
      mutation DELETE_USER_FAVORITE {
        deleteUserFavorite(input: {userId: 1, placeId: "513340fdc206bc5ec059039010feea844740f00103f9012a0f3f090200000092030e506c616e6574204669746e657373"}) 
                                      {success}
                                     }

      ```


### Tech Stack
![rubyonrails](https://img.shields.io/badge/Ruby-100000?style=for-the-badge&logo=rubyonrails&logoColor=cc0000&labelColor=000000&color=000000)
![ruby](https://img.shields.io/badge/Ruby-100000?style=for-the-badge&logo=Ruby&logoColor=cc0000&labelColor=000000&color=000000)
![json](https://img.shields.io/badge/json-000000?style=for-the-badge&logo=json&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-100000?style=for-the-badge&logo=Css3&logoColor=FFFFFF&labelColor=1388BA&color=1388BA)
![postgresql](https://img.shields.io/badge/postgresql-000000?style=for-the-badge&logo=postgresql&logoColor=light-blue)
<br>
![ReactRouter](https://img.shields.io/badge/React_Router-100000?style=for-the-badge&logo=ReactRouter&logoColor=FFFFFF&labelColor=D31313&color=D31313)
![Heroku](https://img.shields.io/badge/heroku-000000.svg?style=for-the-badge&logo=heroku&logoColor=%23430098)
![React](https://img.shields.io/badge/React-100000?style=for-the-badge&logo=React&logoColor=46CCEE&labelColor=black&color=black)
![Markdown](https://img.shields.io/badge/markdown-000000.svg?style=for-the-badge&logo=markdown&logoColor=white)
![Webpack](https://img.shields.io/badge/Webpack-100000?style=for-the-badge&logo=webpack&logoColor=000000&labelColor=8ED5FA&color=8ED5FA)
<br>
![Miro](https://img.shields.io/badge/Miro-000000?style=for-the-badge&logo=Miro&logoColor=yellow)
![GraphQL](https://img.shields.io/badge/GraphQL-000000?style=for-the-badge&logo=GraphQL&logoColor=pink)
![Cypress](https://img.shields.io/badge/Cypress-100000?style=for-the-badge&logo=Cypress&logoColor=62E4B4&labelColor=000000&color=black)
![NodeJS](https://img.shields.io/badge/node.js-100000?style=for-the-badge&logo=NODE.JS&logoColor=FFFFFF&labelColor=6CC24A&color=6CC24A)
![HTML](https://img.shields.io/badge/HTML-100000?style=for-the-badge&logo=HTML5&logoColor=FF5733&labelColor=black&color=black)


### Contributors
<table>
  <tr>
    <th>Jennifer Yacoubian</th>
    <th>Astrid Hecht</th>
    <th>Dani Bagley</th>
    <th>Ian McIntosh</th>
    <th>Lucas Colwell</th>
    <th>Mostafa Sakr</th>
    <th>Ashley Turner</th>
    <th>Ty Keating<br>(Project Mentor)</th>
    <th>Leta<br>(Project Manager)</th>
  </tr>
  <tr>
    <td><img src="https://avatars.githubusercontent.com/u/106957849?v=4"></td>
    <td><img src="https://avatars.githubusercontent.com/u/106942456?v=4"></td>
    <td><img src="https://avatars.githubusercontent.com/u/108088961?v=4"></td>
    <td><img src="https://avatars.githubusercontent.com/u/106535343?v=4"></td>
    <td><img src="https://avatars.githubusercontent.com/u/98673086?v=4"></td>
    <td><img src="https://avatars.githubusercontent.com/u/110377741?v=4"></td>
    <td><img src="https://avatars.githubusercontent.com/u/105073232?v=4"></td>
    <td><img src="https://avatars.githubusercontent.com/u/5234142?v=4"></td>
    <td><img src="https://avatars.githubusercontent.com/u/22563791?v=4"></td>
    
  </tr>
 
  <tr>
    <td>
       <a href="https://github.com/jmyacobn" rel="nofollow noreferrer">
           Github
      </a><br>
        <a href="https://www.linkedin.com/in/jennifer-yacoubian/" rel="nofollow noreferrer">
    LinkedIn
      </a>
    </td>
    <td>
       <a href="https://github.com/Astrid-Hecht" rel="nofollow noreferrer">
           Github
      </a><br>
        <a href="https://www.linkedin.com/in/astrid-hecht/" rel="nofollow noreferrer">
     LinkedIn
      </a>
    </td>
    <td>
      <a href="https://github.com/daniabee"  rel="nofollow noreferrer">
           Github
        </a><br>
      <a href="https://www.linkedin.com/in/dani-bagley-798463116/" rel="nofollow noreferrer">
     LinkedIn
        </a>
    </td>
    <td>
      <a href="https://github.com/grainymac" rel="nofollow noreferrer">
           Github
        </a><br>
      <a href="https://www.linkedin.com/in/ianmac87/" rel="nofollow noreferrer">
     LinkedIn
        </a>
    </td>
    <td>
      <a href="https://github.com/lcole37"  rel="nofollow noreferrer">
          Github
        </a><br>
      <a href="https://www.linkedin.com/in/lucas-colwell-b3a753179/" rel="nofollow noreferrer">
     LinkedIn
        </a>
    </td>
    <td>
      <a href="https://github.com/msakr21" rel="nofollow noreferrer">
           Github
        </a><br>
      <a href="https://www.linkedin.com/in/mostafa-sakr-4bb722250/" rel="nofollow noreferrer">
     LinkedIn
        </a>
    </td>
    <td>
      <a href="https://github.com/ashuhleyt" rel="nofollow noreferrer">
           Github
            </a><br>
            <a href="https://www.linkedin.com/in/ashuhleyt/" rel="nofollow noreferrer">
     LinkedIn                                                         
        </a><br>
        </td>
    <td>
       <a href="https://github.com/bontgoy" rel="nofollow noreferrer">
           Github
      </a><br>
        <a href="https://www.linkedin.com/in/tyler-keating" rel="nofollow noreferrer">
           LinkedIn
      </a>
    </td>
    <td>
       <a href="https://github.com/letakeane" rel="nofollow noreferrer">
           Github
      </a><br>
        <a href="https://www.linkedin.com/in/letakeane" rel="nofollow noreferrer">
           LinkedIn
      </a>
    </td>
  </tr>
</table>
