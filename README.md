<div align="center">

<img src="assets/BuberBreakfastUiUx.png" alt="drawing" width="1000"/>

 [![GitHub Stars](https://img.shields.io/github/stars/amantinband/buber-breakfast.svg)](https://github.com/amantinband/buber-breakfast/stargazers) [![GitHub license](https://img.shields.io/github/license/amantinband/buber-breakfast)](https://github.com/amantinband/buber-breakfast/blob/main/LICENSE)

---

### This is the source code of the [CRUD REST API from scratch using .NET 6 tutorial](https://youtu.be/PmDJIooZjBE)

</div>

- [Give it a star ⭐!](#give-it-a-star-)
- [Overview](#overview)
- [Service Architecture](#service-architecture)
- [Technologies](#technologies)
- [Architecture](#architecture)
- [Usage](#usage)
- [API Definition](#api-definition)
  - [Create Breakfast](#create-breakfast)
    - [Create Breakfast Request](#create-breakfast-request)
    - [Create Breakfast Response](#create-breakfast-response)
  - [Get Breakfast](#get-breakfast)
    - [Get Breakfast Request](#get-breakfast-request)
    - [Get Breakfast Response](#get-breakfast-response)
  - [Update Breakfast](#update-breakfast)
    - [Update Breakfast Request](#update-breakfast-request)
    - [Update Breakfast Response](#update-breakfast-response)
  - [Delete Breakfast](#delete-breakfast)
    - [Delete Breakfast Request](#delete-breakfast-request)
    - [Delete Breakfast Response](#delete-breakfast-response)
- [Credits](#credits)
- [VSCode Extensions](#vscode-extensions)
- [Disclaimer](#disclaimer)
- [License](#license)

---

# Give it a star ⭐!

Loving it? Show your support by giving this project a star!

# Overview

In the tutorial, we build a CRUD REST API from scratch using .NET 6.
As you would expect, the backend system supports Creating, Reading, Updating and Deleting breakfasts.

# Service Architecture

<div align="center">

<img src="assets/BackendServiceArchitecture.png" alt="drawing" width="700px"/>

</div>

# Technologies

<div align="center">

<img src="assets/Technologies.png" alt="drawing" width="700px"/>

</div>

# Architecture

<div align="center">

<img src="assets/Architecture.png" alt="drawing" width="700px"/>

</div>

# Usage

Simply `git clone https://github.com/amantinband/buber-breakfast` and `dotnet run --project BuberBreakfast`.

# API Definition


## Create Breakfast

### Create Breakfast Request

```js
POST /breakfasts
```

```json
{
    "name": "Vegan Sunshine",
    "description": "Vegan everything! Join us for a healthy breakfast..",
    "startDateTime": "2022-04-08T08:00:00",
    "endDateTime": "2022-04-08T11:00:00",
    "savory": [
        "Oatmeal",
        "Avocado Toast",
        "Omelette",
        "Salad"
    ],
    "Sweet": [
        "Cookie"
    ]
}
```

### Create Breakfast Response

```js
201 Created
```

```yml
Location: {{host}}/Breakfasts/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Vegan Sunshine",
    "description": "Vegan everything! Join us for a healthy breakfast..",
    "startDateTime": "2022-04-08T08:00:00",
    "endDateTime": "2022-04-08T11:00:00",
    "lastModifiedDateTime": "2022-04-06T12:00:00",
    "savory": [
        "Oatmeal",
        "Avocado Toast",
        "Omelette",
        "Salad"
    ],
    "Sweet": [
        "Cookie"
    ]
}
```

## Get Breakfast

### Get Breakfast Request

```js
GET /breakfasts/{{id}}
```

### Get Breakfast Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Vegan Sunshine",
    "description": "Vegan everything! Join us for a healthy breakfast..",
    "startDateTime": "2022-04-08T08:00:00",
    "endDateTime": "2022-04-08T11:00:00",
    "lastModifiedDateTime": "2022-04-06T12:00:00",
    "savory": [
        "Oatmeal",
        "Avocado Toast",
        "Omelette",
        "Salad"
    ],
    "Sweet": [
        "Cookie"
    ]
}
```

## Update Breakfast

### Update Breakfast Request

```js
PUT /breakfasts/{{id}}
```

```json
{
    "name": "Vegan Sunshine",
    "description": "Vegan everything! Join us for a healthy breakfast..",
    "startDateTime": "2022-04-08T08:00:00",
    "endDateTime": "2022-04-08T11:00:00",
    "savory": [
        "Oatmeal",
        "Avocado Toast",
        "Omelette",
        "Salad"
    ],
    "Sweet": [
        "Cookie"
    ]
}
```

### Update Breakfast Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Breakfasts/{{id}}
```

## Delete Breakfast

### Delete Breakfast Request

```js
DELETE /breakfasts/{{id}}
```

### Delete Breakfast Response

```js
204 No Content
```

# Credits

- [ErrorOr](https://github.com/amantinband/error-or) - A simple, fluent discriminated union of an error or a result.

# VSCode Extensions

- [VSCode Rest Client](https://github.com/Huachao/vscode-restclient) - REST Client allows you to send HTTP request and view the response in Visual Studio Code directly.

- [VSCode Markdown Preview Enhanced](https://github.com/shd101wyy/vscode-markdown-preview-enhanced) - Markdown Preview Enhanced is an extension that provides you with many useful functionalities for previewing markdown files.

# Disclaimer

This is an educational project. The source code is licensed under the MIT license.

# License

This project is licensed under the terms of the [MIT](https://github.com/amantinband/buber-breakfast/blob/main/LICENSE) license.
