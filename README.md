# Chat App

## Authors

-   Barte Sadlej (github: barteksad)

## Description

Chat app written in Rust with Postgress db. Allows users to create new accounts and channels and communicate within channel. All unseed messages from last login are delivered once logged in again.

By default server stats with one user named ADMIN with password ADMIN

### Usage

#### Server:

To run specify DB_URL to postgress database in chat-app/src/config

```
pub const DB_URL: &str = "postgresql://bs429589:iks@localhost:11212/bd";
```

and then run

```
cd chat-app/ && cargo run --bin server
```

#### Client:

run

```
cd chat-app/ && cargo run --bin client [name] [password]
```

press Ctrl+C to exit channel

### How it looks like

![alt text](readme_images/main_menu.png) ![alt text](readme_images/chatt_room.png)

## Functionality

1.

-   [x] Server creates channels provided as input arguments
-   [x] Users provide nick-names and password while joining and can choose channels
-   [x] Messages are visible across channel
-   [x] One can either send a message or change the channel

2.

-   [x] Added logging and creating users
-   [x] Loading and saving channels and users from database
-   [x] Creating new channels and saving messages
-   [x] Added meassages history and sending messages unseen from last user logging

-   everything from terminal

## A proposal for division into parts

In first pars first four points,

In secound part, secound four points,

## Libraries

-   Tokio : threads for each connection and TCP stream
-   Serde : for messages serialization
-   and lots of smaller ones
