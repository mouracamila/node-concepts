<p align="center">
  <img src="https://miro.medium.com/max/1400/1*fzcYZIhdZjuQaT8gTk1YAQ.png" style="width:auto;">
</p>

<p align="center">
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/github/license/rluders/oc-cors-plugin.svg">
  </a>
<p>

# Concepts NodeJS with TypeScript

## Introduction

This is an aplication for storing incoming an outgoing financial transactions, and also, allows the user to record and list these transactions.

### Technologies used

- **NodeJS**
- **TypeScript**
- **UUID**
- **JSON**
- **EXPRESS**

Did apply models concepts, repositories and services.

## Installation

1.  Clone this repository:

    `git@github.com:mouracamila/node-concepts.git`

2.  Installing dependencies:

    `$ yarn`

3.  Running project:

    `$ yarn dev:server`

##### Obs: **Yarn** should be run where **packege.json** is in your project

#### After running the project, in your terminal, this message shold be displayed:

```
 🚀 Server started on port 3333!
```

## Create project

`POST /transactions`

#### Parameters

| Name  | Type              | Required | Description       |
| ----- | ----------------- | -------- | ----------------- |
| title | string            | No       | Name transaction  |
| value | number            | Yes      | Value transaction |
| type  | income or outcome | Yes      | Income or Outcome |

#### Responses

SUCCESS
`Code: 200`

```
{
  "id": <UUID>,
  "title": <string>,
  "value": <number>
  "type": <income | outcome>
}
```

ERROR

`Code: 400`

```
{
  "error": "Transaction type is invalid"
}
```

```
{
  "error": "Value is invalid"
}
```

### List project

`GET /transactions`

#### Responses

SUCCESS

`Code: 200`

```
{
  "id": <UUID>,
  "title": <string>,
  "value": <number>
  "type": <income | outcome>
}

{
  "balance": {
    "income": <number>,
    "outcome": <number>,
    "total": <number>
}
```

#### The basis of this application can be found at this URL: [ Template](https://github.com/Rocketseat/gostack-template-fundamentos-node)
