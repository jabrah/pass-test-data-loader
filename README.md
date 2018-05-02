
Outline:

First data pass
1. Read in JSON data into PASS objects
  * Ignore extra JSON properties
2. Map object fake ID -> PASS entity
3. Remove fake IDs in all PASS entities, as Fedora will auto-assign appropriate IDs
4. Save all objects in Fedora
  * Keep a map of fake ID -> URI (Will this be in the first map?)

Second data pass
1. Read in JSON data as bare JSONObject, looking for appropriate relationship tags
2. For each JSONObject relationship:
    a. Get source entity
    b. Get target URI
    c. Add target URI to appropriate place on entity
    d. Save source entity to Fedora

