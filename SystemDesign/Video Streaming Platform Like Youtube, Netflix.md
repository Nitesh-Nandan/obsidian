
## Functional Requirements
👉 Publishing House Can Upload Videos.
👉 User's HomePage + Search
👉 Play Videos
👉 Support All devices

## Non-Functional Requirements
👉 Low latency and High Availablity
👉 Good Recomendation System
👉 Adaptive BitRate Streaming


## HLD![[Video Streaming Platform.png]]

## **Highlights**

**Services:**
- **Asset Onboarding Service**: Uploads the file to S3 and publish an event.
- **Asset Service:**  Monitor the progress and notify the production house.
- **Content Processor** - Chunker, Content Filter, Classifier, Transcoders, Upload all videos to S3 & CDN.
- **Home Page Service:**  - Recommendation System, Based on past views, age and locality
- **CDN Writer:**  Distributing the file and caching. Peer to peer network like torents.
- **Search Service**: Does the intent and fuzzy search.
- **Search Kafka Consumer**:  Used for indexing.
- **User Service:** Used for authentication and session cache and also supports Home Page  service.
- 


## Keep in Minds
👉 Thumbnail mapping
👉 Why Cassandra
👉 Recomendation Engine -> feedback loop on views, percentage completed
👉 CDN Serving