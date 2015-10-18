#### Barebones API

From: http://www.yoniweisbrod.com/rails-api-mini-guide/


## Endpoints

### Stories
http://liveproxy-rails-example.herokuapp.com/api/v1/stories

#### Create [POST]
```json
{
  story: {
    title: String (Required)
  }
}
```

#### List [GET]
```json
{
  "stories": [
    {
      "id": 1,
      "title": "Hola Mundo",
      "sentences": [
        {
          "id": 1,
          "content": "Once upon a time",
          "position": 1
        }
      ]
    }
  ]
}
```

### Sentences
http://liveproxy-rails-example.herokuapp.com/api/v1/sentences

#### Create [POST]
```json
{
  sentence: {
    content: String (required)
  }
  story_id: Integer (required)
}
```

#### List [GET]
URL Params: story_id (required)
```
{
  "sentences": [
    {
      "id": 1,
      "content": "Once upon a time",
      "position": 1
    }
  ]
}
```
