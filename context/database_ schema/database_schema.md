

### The database will have following tables
- User
- Expense

### User Schema
User(
    id int auto_increment Primary Key,
    name varchar,
    email varchar unique,
    created_at DateTime Default=Now()
)auto_increment=1001

### Expense Schema
Expense(
    id integer auto_increment Primary Key,
    user_id integer,
    amount double,
    category varchar,
    description varchar,
    date Date,
    created_at DateTime default=Now()
    Foriegn Key(user_id) Refrences User(id)
)auto_increment =101
