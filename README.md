![Imgur](https://i.imgur.com/FwNH7tU.jpg)

# GeoFirestore — Realtime location queries with Firestore

GeoFirestore is set of open-source libraries for iOS and Android applications which allow you
to store and query a set of documents based on their geographic location. At its heart, GeoFirestore
simply stores locations with string keys. Its main benefit, however, is the possibility of
querying documents within a given geographic area - all in realtime.

GeoFirestore uses the Firestore database for data storage, allowing query results to be updated in realtime as they change. GeoFirestore *selectively loads only the data near certain locations, keeping your applications light and responsive*, even with extremely large datasets.

## GeoFirestore Clients

The GeoFirestore library is available in two different languages:

* [GeoFirestore for iOS](https://github.com/imperiumlabs/GeoFirestore-iOS)
* [GeoFirestore for Android](https://github.com/imperiumlabs/GeoFirestore-Android)

All of the clients work on the same underlying data structure and have similar APIs, making
it easy to create a cross-platform app on top of GeoFirestore.

### Integrating GeoFirestore with your data

GeoFirestore is designed as a lightweight add-on to Firestore. However, to keep things simple, GeoFirestore stores data in its own format and its own location within your Firestore database. This allows your existing data format and security rules to remain unchanged and for you to add GeoFirestore as an easy solution for geo queries without modifying your existing data.

### Example usage

Assume you are building an app to rate bars, and you store all information for a bar (e.g. name, business hours and price range) at `collection(bars).document(bar-id)`. Later, you want to add the possibility for users to search for bars in their vicinity. This is where GeoFirestore comes in. You can store the location for each bar document using GeoFirestore. GeoFirestore then allows you to easily query which bar are nearby.

## Getting Started with Firestore

GeoFirestore requires the Firestore database in order to store location data. You can [learn more about Firestore here](https://firebase.google.com/docs/firestore/).
