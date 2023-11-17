
```plantuml

hide circle
skinparam linetype ortho

entity game {
	id : serial <<primary key, not nullable>>
	--
	first_player_id : integer <<foreign key, not nullable>>
	second_player_id : integer <<foreign key, not nullable>>
}

entity player {
	id : serial <<primary key, not nullable>>
	--
	name : varchar <<not nullable>>
}

player ||--|{ game: game.first_player_id -> player.id\ngame.second_player_id -> player.id

```
