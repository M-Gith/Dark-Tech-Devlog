# A Mirror, Firebase and an Exhibition Floor

Soon we will have to step onto the exhibition floor and present our provocative mirror to the exhibition crowd. Before we do this, however, we wanted to sharpen our priorities as a team regarding the project and what needs to be done at the moment, so we know what to focus on in the next sprint.

It basically came down to the following:

## Current Sprint

1. **Get as much of the provocative experience done as possible.** This way, we don't have to focus on this aspect in the final stretch (which includes a Christmas holiday!).

## Next and Final Sprint

2. **Shift focus to the functionality of the mirror.** We want to make sure the mirror works on its own. For this, we will look into connecting the mirror to a Raspberry Pi.

For the current sprint, my teammate Donny and I had the responsibility of getting the backend connected to a database, so we can store information and send it to and retrieve it from the frontend of the mirror.

---

# Firebase: For a Quick Proof of Concept

![Physical prototype](assets/images/article%203/firebase-intro.png)

You may have heard of Firebase before. In case you haven't, it's a Google product that allows for quick application setup due to the extensive backend functionality it already provides.

Basically, since a lot of functionality is already provided, it gives us the ability to quickly set up a product/PoC (which it's also often used for) before delving too deeply into the nitty-gritty of real-time relational databases and server hosting.

## Firestore: A NoSQL Database

Firebase has some limitations, though. It's a NoSQL database, which, in a positive sense, means that there's a less complex way of working since it uses a document-based structure instead of everything being organised in relational tables.

However, it also means that the complexity of a project can only reach a certain depth before constraints are encountered. But regarding the scope of our project, I don't think it's something we should worry about.

## Building Quickly

I think it's good to consider what we really need in a project. When taking into account the fact that we want to create a whole and complete experience, and that the final product will function as a prototype/provocatype, it's worth considering quick-to-build solutions.

They allow us to quickly see what's possible and what isn't. On top of that, they can help us become inspired by our own product and develop an even greater desire to succeed.

## What We Need from Firebase

Firebase has a bunch of different functionalities, but currently, we don't need that many of them. We need the following two things:

1. **Firestore** – The NoSQL database.
2. **Storage** – For storing media files.

Firestore is needed to store our data objects.

For us, these will be the clothing items that are recommended to people. To recommend these clothing items, we store a bit of data with each item to determine what may be recommended. To keep things simple, we have, for now, just looked at the colour of the clothing someone is wearing and recommend items of the opposite colour.

![Physical prototype](assets/images/article%203/firestore.png)

But it's not like we can just store a whole image for each item in Firestore. It doesn't allow for this. That's why we need something else: Storage.

Storage is basically where our media files are stored. These can then be retrieved using the storage path that we link to each item in Firestore.

It does mean that when wanting to retrieve a specific image, we first need to retrieve the document in which the storage path resides, but so far, this hasn't made things more difficult for us.

![Physical prototype](assets/images/article%203/storage.png)
---

# Scoping the Event Location

We are starting to get closer and closer to our exhibition date, which is on the **4th of January inside HvA's FLOOR!**

But we still need to know a bunch of things about the event location. Especially since we have a smart mirror, we want to make sure people get the whole experience of it.

To achieve this, we wanted to make sure we had a spot by the wall where we could hang our mirror and give visitors a full "mirror" experience. However, we learned that some things would have to go differently...

## Getting Event Location Details

About two weeks ago, all of the project groups were invited to receive information about the exhibition location and ask questions and make requests, so everyone could already start planning what they would need at the location.

![Physical prototype](assets/images/article%203/event-location-overview.jpg)

I took the initiative to visit the location so that I could communicate our team's needs and ask questions regarding the display of our smart mirror.

We aren't very demanding, so we didn't actually have that many wishes. However, we did have one important request: **a place on the wall to hang up our mirror.**

During the orientation, the most relevant points came up, which already answered most of our questions:

- We may use things that are already available at the exhibition location as decoration (plants and such).
- There is a mannequin in the storage room that we can use.
- Someone has a severe nut allergy, so absolutely **NO bringing of nuts!**
- Nothing may be hammered or stuck to the wall.

Of all these points, the last two seem to hold the most significance.

For one, we don't want anyone to have a severe allergic reaction at the event location, so it will be for the best that we hold off on the nuts. This is naturally met with severe disappointment by members of our team.

But more importantly, it was stated that we couldn't place anything on the wall. This raised some concerns, but after taking some time with the person responsible for coordinating the exhibition, we were able to explore a few solutions.

## Exploring Solutions

### 1. Using a Painting Stand

The first solution was to put the mirror on a painting stand. However, this wouldn't have been possible since the painting stand wasn't able to support the thickness of our mirror.

### 2. Placing the Mirror on the Bar

![Physical prototype](assets/images/article%203/floor-bar.jpg)

The second solution we explored was elevating the mirror and placing it against a wall of the bar.

This would have been a good solution since the bar could allow us to simulate a real-life environment. For example, we could bring household products and place them on the bar in front of the mirror to make it look like a bathroom or something along those lines.

The problem we ran into, however, was that the bar was right in front of the entrance, as seen in the picture on the right.

This would mean that the flow of people entering and leaving could interfere with the display of our mirror.

### 3. Using the Cabinets

![Physical prototype](assets/images/article%203/floor-cabinets.jpg)

The third, and likely final, solution came when we saw some open cabinets that were fairly high and could be used to place the mirror on.

What's actually nice about this solution is that the cabinets allow us to simulate an environment in which the mirror would likely reside.

The person from FLOOR mentioned that having notable decorations makes something a lot more memorable and engaging.
![Physical prototype](assets/images/article%203/random-cabinet.jpg)

With these cabinets, we can bring some decorations and make it seem like an actual part of the house!

Not only that, but with the plants we can use, we can really put people in the right frame of mind for using and understanding our smart mirror by bringing them into an everyday context.

## The Mannequin

I had also made sure to reserve the mannequin that FLOOR had available.

I figured we could dress it up to immediately draw people into our space and help them understand the context of the mirror!

---

# Finishing Off...

Things are going as expected so far.

At the start of the final sprint, we will have to get together as a team to design a solution that elevates and holds up the mirror, since we won't be able to lean it against a wall.

Data is being pulled from our Firebase and is being used to make clothing recommendations. We can perhaps work on this further in the last sprint to make the smart mirror seem even more sophisticated and "dark".