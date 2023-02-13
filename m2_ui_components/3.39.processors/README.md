Write a code to use a `http processor` to get the list of pokemons via API.

`Endpoint: https://pokeapi.co/api/v2/pokemon`

Follow below steps to use a `http processor`

1. Create a FTD file with name as `processor.ftd`

2. First of all, import the `processors` in your FTD file

It should be like this:

```
-- import: fastn/processors
```

3. The pokemon API returns a `JSON response` which we can be handled by creating a record.

Consider the following JSON response sample:

```
// https://pokeapi.co/api/v2/pokemon?limit=5&offset=10
{
  "count": 1279,
  "next": "https://pokeapi.co/api/v2/pokemon?offset=15&limit=5",
  "previous": "https://pokeapi.co/api/v2/pokemon?offset=5&limit=5",
  "results": [
    {
      "name": "metapod",
      "url": "https://pokeapi.co/api/v2/pokemon/11/"
    },
    {
      "name": "butterfree",
      "url": "https://pokeapi.co/api/v2/pokemon/12/"
    },
    {
      "name": "weedle",
      "url": "https://pokeapi.co/api/v2/pokemon/13/"
    },
    {
      "name": "kakuna",
      "url": "https://pokeapi.co/api/v2/pokemon/14/"
    },
    {
      "name": "beedrill",
      "url": "https://pokeapi.co/api/v2/pokemon/15/"
    }
  ]
}
```

4. From the JSON response, map the required fields to use/display and create a record with name as `response-record` having fields

   a. `integer` with name as `count`

   b. `results-record` with list type and name as `results` which is present as array in response

   c. `result-record` is a record nested in `response-record` having fields in `result-record` as `string` datatype with field name as `name`

Follow below code:

```
-- record response-record:
integer count:
results-record list results:

-- record results-record:
string name:

```

5. Create a instance of `response-record` as `response` along with `processor`. You can pass the query params as field names to a HTTP processor

Follow below code:

```
-- response-record response:
$processor$: processors.http
url: https://pokeapi.co/api/v2/pokemon
limit: 10
offset: 10
```

6. Create a component with name as `pokemon` having `caption` field with name as `name` to display the value of `name` field using `ftd.text` component

Follow below code to create the pokemon component:

```
-- component pokemon:
caption name:

-- ftd.text: $pokemon.name

-- end: pokemon

```

6. Final step is to use the component now and map with the `response` and loop the data over the `response.results`

Follow below to display the list of pokemons

```
-- pokemon: $poke.name
$loop$: $response.results as $poke

```

Run your code in the browser, by the file name as processor
