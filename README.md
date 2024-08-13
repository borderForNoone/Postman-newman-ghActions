# Postman + newman + github actions (Simple store template)

<a href="https://drive.google.com/file/d/1LQ1uG7Tt70Jubuk5loS4dMSk-1AJ5jzz/view?usp=sharing" /> Intro </a>

# Preconditions

1. Install Node.js;
2. Clone the repository where the project is stored:
    - `git clone https://github.com/borderForNoone/cypress-cucumber.git`
    - `cd cypress-cucumber`
3. Install Dependencies;
    - `npm install`
  
# Steps to run

1. Run `npm run tern-on-api`(to run testing server locally);
2. Open a new powershell and do not close the one on which the server is running;
3. Run `newman run store.postman_collection.json`.

### Overview of local server testing
Routes `/products`, `/orders` and `/users`. Below is a table of supported operations with `products` as example resource. The same operations are also supports for `orders/` and `users/`.

| VERB     |Route          | Input      | Output             |
|----------|---------------|------------|--------------------|
| GET      | /products     | *None*     | **Array**          |
| GET      | /products/:id |  **e.g 3** | **Object**         |
| POST     | /products     | **object** | **Created object** |
| PUT      | /products     | **object** | **Updated object** |
| DELETE   | /products/:id | **e.g 3**  | **Deleted object** |

# Report

The report is generated on the gitHub page: https://borderfornoone.github.io/Postman-newman-ghActions/report.html

# CI

Testing runs in GitHub actions and deploys a report on the gitHub page: https://borderfornoone.github.io/Postman-newman-ghActions/report.html
