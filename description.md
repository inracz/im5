## API endpoints

| Method | URI                                      | Description
| ------ | -----------------------------------------| -----------
| GET    | /questions                               | Get all questions
| GET    | /questions/{question}                    | Get one question
| GET    | /questions/{question}/comments           | Get comments on a question
| GET    | /users/{user}                            | Get a user
| POST   | /questions                               | Create a new question
| POST   | /questions/{question}/comments           | Create a new comment 
| POST   | /users                                   | Create a new user
| PUT    | /users/{user}                            | Edit a user
| PUT    | /questions/{question}                    | Edit a question
| DELETE | /users/{user}                            | Delete a user
| DELETE | /questions/{question}                    | Delete a question
| DELETE | /questions/{question}/comments/{comment} | Delete a comment


## Database

| questions |      |
| --------- | ---
| id        | int
| title     | string
| body      | text

| tags      |      |
| --------- | ---
| id        | int
| title     | string

| questions_tags |      |
| -------------- | ---
| id             | int
| question_id    | int
| tag_id         | int

| comments       |      |
| -------------- | ---
| id             | int
| question_id    | int
| user_id        | int
| body           | text

| question_ratings |      |
| ---------------- | ---
| id               | int
| question_id      | int
| user_id          | int
| rating           | boolean

| comment_ratings  |      |
| ---------------- | ---
| id               | int
| comment_id       | int
| user_id          | int
| rating           | boolean