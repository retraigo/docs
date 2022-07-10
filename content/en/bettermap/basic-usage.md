---
title: Basic Usage
description: "Basic usage of BetterMap."
position: 15
category: BetterMap
---

## Use Case
BetterMap is just an extension of the built-in Map class from JavaScript.

## Example with sorting
```ts
import Pokemon from "https://deno.land/x/fortuna@v1.1.2/testdata/pokemon.json" assert {
  type: "json",
};
import { BetterMap } from "https://deno.land/x/bettermap/mod.ts";

interface PokemonData {
  name: string;
  id: number;
  tier: string;
}


const b = new BetterMap<string, PokemonData>("Pokemon");
for (const pokemon of Pokemon) {
  b.set(`${pokemon.name}`, pokemon);
}

// The sort() method allows sorting a map. 
// It returns the Map instance to allow chaining methods.

console.log(
  b.sort((a, b) => a.name.toLowerCase().localeCompare(b.name.toLowerCase())),
);
```