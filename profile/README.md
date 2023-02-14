<div align="center"> 

![Asset 4](https://user-images.githubusercontent.com/105073232/217386688-758d8d96-71ec-46cf-84ea-9de425b0dff0.png)  
</div>
A user can search for a city and get a big picture 'snapshot' of the notable things in that city - list of the museums, top restaurants, etc based off of criteria they define. 
<br>
<br>


:earth_americas: [Learning Goals](#learning-goals)
<br>
:earth_americas: [Project Overview](#project-overview)
<br>
:earth_americas: [Planning](#planning)
<br>
:earth_americas: [Endpoints](#endpoints)
<br>
:earth_americas: [Tech Stack](#tech-stack)
<br>
:earth_americas: [Deployment](#deployment)
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


### Project Overview

[Backend Repository](https://github.com/DiscoverIt-2208/DiscoverIt-2208-BE)
<br>
[Frontend Repository](https://github.com/DiscoverIt-2208/DiscoverIt-2208-FE)

### Planning
Database Design 
![image](https://user-images.githubusercontent.com/105073232/217670746-aa1f1e46-625a-480d-a246-a539dbb20624.png)
<br> 

### Endpoints
`https://discover-it.herokuapp.com/graphql'
#### Queries
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
  * Favorite 
      ```
      favorite (id:) {
    }
      ```
  * Fetch Places 
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

### Tech Stack
![rubyonrails](https://img.shields.io/badge/Ruby-100000?style=for-the-badge&logo=rubyonrails&logoColor=cc0000&labelColor=000000&color=000000)
<br>
![ruby](https://img.shields.io/badge/Ruby-100000?style=for-the-badge&logo=Ruby&logoColor=cc0000&labelColor=000000&color=000000)
<br>
![json](https://img.shields.io/badge/json-000000?style=for-the-badge&logo=json&logoColor=white)
<br>
![CSS3](https://img.shields.io/badge/CSS3-100000?style=for-the-badge&logo=Css3&logoColor=FFFFFF&labelColor=1388BA&color=1388BA)
<br>
![postgresql](https://img.shields.io/badge/postgresql-000000?style=for-the-badge&logo=postgresql&logoColor=light-blue)
<br> 
![ReactRouter](https://img.shields.io/badge/React_Router-100000?style=for-the-badge&logo=ReactRouter&logoColor=FFFFFF&labelColor=D31313&color=D31313)
<br> 
![Heroku](https://img.shields.io/badge/heroku-000000.svg?style=for-the-badge&logo=heroku&logoColor=%23430098)
<br>
![React](https://img.shields.io/badge/React-100000?style=for-the-badge&logo=React&logoColor=46CCEE&labelColor=black&color=black)
<br>
![Markdown](https://img.shields.io/badge/markdown-000000.svg?style=for-the-badge&logo=markdown&logoColor=white)
<br>
![Webpack](https://img.shields.io/badge/Webpack-100000?style=for-the-badge&logo=webpack&logoColor=000000&labelColor=8ED5FA&color=8ED5FA)
<br>
![Miro](https://img.shields.io/badge/Miro-000000?style=for-the-badge&logo=Miro&logoColor=yellow)
<br>
![GraphQL](https://img.shields.io/badge/GraphQL-000000?style=for-the-badge&logo=GraphQL&logoColor=pink)
<br>
![Cypress](https://img.shields.io/badge/Cypress-100000?style=for-the-badge&logo=Cypress&logoColor=62E4B4&labelColor=000000&color=black)
<br>
![NodeJS](https://img.shields.io/badge/node.js-100000?style=for-the-badge&logo=NODE.JS&logoColor=FFFFFF&labelColor=6CC24A&color=6CC24A)
<br>
![HTML](https://img.shields.io/badge/HTML-100000?style=for-the-badge&logo=HTML5&logoColor=FF5733&labelColor=black&color=black)



### Deployment
[Check out our live app here!](https://discover-it.herokuapp.com/graphql)


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
