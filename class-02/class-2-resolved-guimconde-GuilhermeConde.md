# MongoDB - Aula 02 - Exercício
autor: Guilherme Machado Conde


guilherme-virtual-machine(mongod-2.4.9) be-mean-instagram> use be-mean-pokemons
switched to db be-mean-pokemons
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> show collections
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> db.expokemons.insert({name:'Charizard', description:'Dragao de fogo', type:'Fogo', atack:150, height:10, defense:55})
Inserted 1 record(s) in 155ms
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> db.expokemons.insert({name:'Alakazan', description:'Doido de natureza', type:'Psiquico', atack:120, height:4, defense:40})
Inserted 1 record(s) in 1ms
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> db.expokemons.insert({name:'Butterfly', description:'Borboletinha xD', type:'Inseto', atack:70, height:3, defense:20})
Inserted 1 record(s) in 0ms
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> db.expokemons.insert({name:'Raichu', description:'Outro rato eletrico ', type:'Eletrico', atack:90, height:6, defense:45})
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> db.expokemons.insert({name:'Onix', description:'Minhoca gigante de pedra', type:'Pedra', atack:78, height:12, defense:65})
Inserted 1 record(s) in 0ms
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> db.expokemons.find()
{
  "_id": ObjectId("565de4737e6c18992f1c0970"),
  "name": "Charizard",
  "description": "Dragao de fogo",
  "type": "Fogo",
  "atack": 150,
  "height": 10,
  "defense": 55
}
{
  "_id": ObjectId("565de4c37e6c18992f1c0971"),
  "name": "Alakazan",
  "description": "Doido de natureza",
  "type": "Psiquico",
  "atack": 120,
  "height": 4,
  "defense": 40
}
{
  "_id": ObjectId("565de4f87e6c18992f1c0972"),
  "name": "Butterfly",
  "description": "Borboletinha xD",
  "type": "Inseto",
  "atack": 70,
  "height": 3,
  "defense": 20
}
{
  "_id": ObjectId("565de5367e6c18992f1c0973"),
  "name": "Raichu",
  "description": "Outro rato eletrico ",
  "type": "Eletrico",
  "atack": 90,
  "height": 6,
  "defense": 45
}
{
  "_id": ObjectId("565de5727e6c18992f1c0974"),
  "name": "Onix",
  "description": "Minhoca gigante de pedra",
  "type": "Pedra",
  "atack": 78,
  "height": 12,
  "defense": 65
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> var p = {name: 'Charizard'}
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> var poke = db.expokemons.findOne(p)
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> poke
{
  "_id": ObjectId("565de4737e6c18992f1c0970"),
  "name": "Charizard",
  "description": "Dragao de fogo",
  "type": "Fogo",
  "atack": 150,
  "height": 10,
  "defense": 55
}
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> poke.description = 'Dragao mal humorado de fogo'
Dragao mal humorado de fogo
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> db.expokemons.save(poke)
Updated 1 existing record(s) in 80ms
guilherme-virtual-machine(mongod-2.4.9) be-mean-pokemons> db.expokemons.find()
{
  "_id": ObjectId("565de4c37e6c18992f1c0971"),
  "name": "Alakazan",
  "description": "Doido de natureza",
  "type": "Psiquico",
  "atack": 120,
  "height": 4,
  "defense": 40
}
{
  "_id": ObjectId("565de4f87e6c18992f1c0972"),
  "name": "Butterfly",
  "description": "Borboletinha xD",
  "type": "Inseto",
  "atack": 70,
  "height": 3,
  "defense": 20
}
{
  "_id": ObjectId("565de5367e6c18992f1c0973"),
  "name": "Raichu",
  "description": "Outro rato eletrico ",
  "type": "Eletrico",
  "atack": 90,
  "height": 6,
  "defense": 45
}
{
  "_id": ObjectId("565de5727e6c18992f1c0974"),
  "name": "Onix",
  "description": "Minhoca gigante de pedra",
  "type": "Pedra",
  "atack": 78,
  "height": 12,
  "defense": 65
}
{
  "_id": ObjectId("565de4737e6c18992f1c0970"),
  "name": "Charizard",
  "description": "Dragao mal humorado de fogo",
  "type": "Fogo",
  "atack": 150,
  "height": 10,
  "defense": 55
}
Fetched 5 record(s) in 113ms

