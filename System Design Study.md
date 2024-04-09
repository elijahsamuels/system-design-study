# System Design Study

## Common System Design Questions

- Design Uber, Ola or Lyft type of systems
- Design a social media app
- Design a global chat service like Whatsapp or a facebook messenger
- Design Facebook’s newsfeed system
- Design a URL shortening service like TinyURL or bit.ly
- Design a forum-like systems like Quora, Reddit or HackerNews
- Design a parking lot system
- Design an e-commerce store
- Design a recommendation system
- Design an API
- Design an API Rate Limiter system for GitHub or Firebase sites
- Design global file storage and file sharing services like Google Drive or Dropbox
- Design a type-ahead search engine service / autocomplete for a search engine
- Design Netflix
- Design a game (Tic-Tac-Toe, Chess, Boggle, Minesweeper, Cards/poker)
- Design a traffic control system
- Design Web Crawler
- Design a web cache
- Design ATM system

## Ask clarifying questions

Is the interviewer looking for a design of the core features, or a high-level overview of the whole service?
What are the constraints of the system?
What are your assumptions? (traffic distribution, number of active users and tweets, read vs write-heavy)

What are the rules of the game?
How many players are there? Are there spectators?
Do we need a timer? Are any other special functions required?

Is this a multiple floor parking garage or a single level parking lot?
How many entry and exit points will be needed, and for what types of vehicles?
Are there monetary goals for this parking lot?

Will users be able to customize the URL?
How long do the URLs last before they expire?
What are the availability and latency requirements for this system?

Consider the functional and non-functional requirements: put (storing objects under a unique key), get (retrieving objects), scalability, availability, performance, etc.
Specify your assumptions: can we assume that put and get are strings?

What are the key features? (fast response time, high relevance, number of results, etc.)
What are the functional and non-functional requirements?

Who/what will be using the API?
What is the purpose of the API?
What kind of information does the API need to pass?

What is the scale and profile of the user base?
What features should be incorporated into the messenger? (e.g. text, video, audio, read receipts, message encryption, etc.)
Should we focus on monetizing the system?

What is the expected user base and usage patterns? (e.g., individual users, businesses, file sizes, frequency of uploads/downloads)
Are there any specific security requirements for file storage and sharing?
Should the service support file versioning, collaboration, and synchronization across devices?

Will the store be available globally or limited to specific regions?
Do we need any specific features or functionalities desired, such as reviews, recommendations, or personalized experiences?

Are we just focusing on Uber's main ride-hailing service?
Are there any specific features or requirements, such as real-time tracking, payment options, or driver-partner management?
Any existing infrastructure or partnerships to leverage?
