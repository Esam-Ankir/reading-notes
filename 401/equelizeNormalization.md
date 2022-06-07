# Read: Class 04 sequelize-normalization

* Sequelize supports the standard associations: One-To-One, One-To-Many and Many-To-Many.

* To do this, Sequelize provides four types of associations that should be combined to create them:

- The A.hasOne(B) association means that a One-To-One relationship exists between A and B, with the foreign key being defined in the target model (B).

- The A.belongsTo(B) association means that a One-To-One relationship exists between A and B, with the foreign key being defined in the source model (A).

- The A.hasMany(B) association means that a One-To-Many relationship exists between A and B, with the foreign key being defined in the target model (B).

- The A.belongsToMany(B, { through: 'C' }) association means that a Many-To-Many relationship exists between A and B, using table C as junction table, which will have the foreign keys (aId and bId, for example). Sequelize will automatically create this model C (unless it already exists) and define the appropriate foreign keys on it.

***To create a One-To-One relationship, the hasOne and belongsTo associations are used together;***

***To create a One-To-Many relationship, the hasMany and belongsTo associations are used together;***

***To create a Many-To-Many relationship, two belongsToMany calls are used together***

## One-To-One relationships

Foo.hasOne(Bar);

Bar.belongsTo(Foo);


ON DELETE and ON UPDATE

RESTRICT, CASCADE, NO ACTION, SET DEFAULT and SET NULL

SET NULL for ON DELETE and CASCADE for ON UPDATE

foreignKey 

type, allowNull, defaultValue

allowNull: false

- to use UUID as the foreign key data type instead of the default (INTEGER

## One-To-Many relationships

Team.hasMany(Player);

Player.belongsTo(Team);


foreignKey

- ON DELETE defaults to SET NULL and ON UPDATE defaults to CASCADE.


## Many-To-Many relationships

const Movie = sequelize.define('Movie', { name: DataTypes.STRING });

const Actor = sequelize.define('Actor', { name: DataTypes.STRING });

Movie.belongsToMany(Actor, { through: 'ActorMovies' });

Actor.belongsToMany(Movie, { through: 'ActorMovies' });


_ Unlike One-To-One and One-To-Many relationships, the defaults for both ON UPDATE and ON DELETE are CASCADE for Many-To-Many relationships.


## Special methods/mixins added to instances

_ When an association is defined between two models, the instances of those models gain special methods to interact with their associated counterparts.

_ For example, if we have two models, Foo and Bar, and they are associated, their instances will have the following methods/mixins available, depending on the association type:

### Foo.hasOne(Bar)

•	fooInstance.getBar()

•	fooInstance.setBar()

•	fooInstance.createBar()

### Foo.hasMany(Bar)

•	fooInstance.getBars()

•	fooInstance.countBars()

•	fooInstance.hasBar()

•	fooInstance.hasBars()

•	fooInstance.setBars()

•	fooInstance.addBar()

•	fooInstance.addBars()

•	fooInstance.removeBar()

•	fooInstance.removeBars()

•	fooInstance.createBar()






