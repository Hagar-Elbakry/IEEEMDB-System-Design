# Recommendation

- this is the part where the user get recommendation based on his preferences or viewing history

## Inputs
- User Id
- User History
## Outputs
- List of recommended movies the user might like

## Flow
- User send request to browse recommended movies
- The request is served with recommend service that dealing with user's viewing history
- The recommended movie's data is fetched from database and implement some algorithem to measure the accuracy of matching user preferences and generate list of recommended movies
- maybe cached result if user makes many request to this endpoint

## Storage 
- User History in NoSQL database because it gets large with time
- Movie's data in SQL database for quick fetching

## Trade-offs
- if i depened on cache the response will be fast but maybe the recommendation be out of date
- if the recommendation service goes down maybe as a temporary solution we can dispaly the most popular movies or the movies with the highest ratings
