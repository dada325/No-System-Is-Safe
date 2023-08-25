# alpha_course


## Vision:
This is something I always want to do, and it is something i always hope i have the ability to do. 
To democratize financial education, bridging the knowledge gap between industry leaders and everyday individuals, and empower everyone to navigate the financial markets with confidence.


## **Mission**:

1. **Education for All**: To provide top-tier, comprehensive financial education that caters to both seasoned hedge fund professionals and individuals new to the financial world.
2. **Empowerment**: To equip users with the tools, knowledge, and insights they need to make informed financial decisions.
3. **Collaboration**: To foster a community where experts and novices can collaborate, share insights, and learn from one another.
4. **Innovation**: To continuously evolve, leveraging the latest technology and pedagogical methods to deliver the best educational experience.


## **High level basic design 
![mermaid-diagram-2023-08-25-150524](https://github.com/dada325/alpha_course/assets/7775973/4aa540c7-f608-4b09-92d2-be97d1e30409)





## Database design 

## Frontend backend design

<img width="601" alt="Screenshot 2023-08-25 at 18 53 38" src="https://github.com/dada325/alpha_course/assets/7775973/69fba9ad-13ce-484a-97b9-fd1b19d70619">

### Backend on GCP

1. **Google App Engine**: Deploy our backend Flask application on Google App Engine. It will scale automatically and provide we with a URL endpoint that we can use to interact with the frontend.

2. **Cloud Functions**: If our backend is made up of stateless, independent functions, we might prefer to use Google Cloud Functions. Each function would become its own endpoint.

3. **Google Kubernetes Engine (GKE)**: If we need more control over our environment, we can containerize our backend application using Docker and deploy it on GKE.

### Frontend on GCP

1. **Google Cloud Storage**: For a static site like wourer frontend, Google Cloud Storage is a cost-effective and simple hosting solution. we can configure a bucket to act like a static website.

2. **Firebase Hosting**: This is another option for hosting static sites that offers benefits like easy SSL setup, CDN distribution, and more. Firebase is also a Google Cloud product, so it integrates well with other GCP services.

3. **App Engine**: we can also host static sites on App Engine, although it's generally more suited for dynamic applications.

### Connecting Frontend and Backend

- Once both are deployed, we will have URLs for both the frontend and backend. 
- The frontend will make API calls to the backend URL to fetch or send data.
- Make sure to update frontend code to use the production backend URL once deployed. Similarly, update our backend to expect requests from the production frontend URL, and configure CORS accordingly.

So, yes, both the frontend and backend can be hosted on GCP but in different services optimized for their specific needs.
