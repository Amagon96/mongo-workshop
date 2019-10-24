# Training data set

Data set taken from [here](https://docs.atlas.mongodb.com/sample-data/sample-training/`).

## sample_training.companies
This collection contains information on companies listed on Crunchbase. It has a variety of information such as the company website and/or blog websites about the company, funding rounds, and known individuals associated with the company.


## sample_training.grades
This collection has randomly generated student grades. Each document contains a class_id that identifies the class and a student_id that identifies the student. All student class exam scores are stored in the scores array, which contains subdocuments with two fields representing the type of assessment and the student score for that assessment.

## sample_training.inspections
The inspections collection was taken from the NYC OpenData dataset. Each inspections document contains information about:

The inspected business name, sector and address,
Inspection id, result, date and certificate number.

## sample_training.posts
The posts collection is a set of randomly generated blog posts created using US Senate speeches as the seed for the document body field. On each document you will find:

Information on the blog posts like body text, author, permalink, date and title,
Randomly generated list of tags,
Randomly generated list of comment subdocuments.

## sample_training.routes
The routes collection data was sourced from the Open Flights data. The documents of this collection have information on airline routes between airports.

Each document contains information about:

Airline data in subdocument containing the name, alias, unique identifier and the IATA airline code,
The source and destination airports, identified their IATA airport code,
Route codeshare and the number of stops.

## sample_training.stories
The stories collection data is sourced from Digg, a web post and story sharing service. Each story document contains contains information about the posting such as:

Hyperlink of the story post, number of comments,
User that posted the story,
Number of diggs (likes) in the story.
The documents in this collection showcase different sets of rich subdocuments. These are useful to teach how to represent multi-dimensional data and dot notation queries.

## sample_training.trips
The trips collection contains bike trips data from the New York City Citibike service. The documents are composed of:

Bicycle unique identifier,
Trip start and stop time and date,
Trip start and end stations names and geospatial location,
User information such as gender, year of birth and service type (Customer or Subscriber).

## sample_training.tweets
The tweets collection is composed of real tweets posted on Twitter. This collection documents exemplify a set of very rich document structures such as subdocuments, embedded subdocument arrays and arrays of subdocuments. These documents provide a variety of different data types on different document fields.

For information on querying embedded documents, see Query on Embedded/Nested Documents in the MongoDB manual.

## sample_training.zips
The zips collection contains information of US cities and their area postal/zip code. Documents contain information on the city name, area zip code, city center geo coordinates (latitude and longitude), state and population.

This dataset is used to explore 2d Index creation and queries.

# Setup
You can add the custom tap in a MacOS terminal session using:

```
$ brew tap mongodb/brew
```
# Installing Formulae
Once the tap has been added locally, you can install individual software packages with:
```
$ brew install mongodb-community
```
# Starting the mongodb-community Server
Run mongod as a service
```
$ brew services start mongodb-community
```

# Imports

```
mongoimport --db training --collection companies --file companies.json
```

```
mongoimport --db training --collection grades --file grades.json
```

```
mongoimport --db training --collection inspections --file inspections.json
```

```
mongoimport --db training --collection posts --file posts.json
```

```
mongoimport --db training --collection routes --file routes.json
```

```
mongoimport --db training --collection stories --file stories.json
```

```
mongoimport --db training --collection trips --file trips.json
```

```
mongoimport --db training --collection tweets --file tweets.json
```

```
mongoimport --db training --collection zips --file zips.json
```