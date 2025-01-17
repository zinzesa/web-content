# Get Started

Milvus offers RESTful API for you to manipulate your collections and data stored in them. Before you dive in, there are several things that are worth noting:

## Understanding the API endpoints

These API endpoints involve manipulating collections in a specified cluster as well as the data in a specific collection.

The prefix of an API endpoint should always be the URI of your Milvus instance, such as `localhost:19530`.

The following is the API endpoint used to list collections in a Milvus cluster.

```shell
curl --request GET \
    --url "${MILVUS_HOST}:${MILVUS_PORT}/v1/vector/collections" \
    --header "Authorization: Bearer ${TOKEN}" \
    --header "accept: application/json" \
    --header "content-type: application/json"
```

## Authentication credentials

You can use a token as the authentication method when you access the API endpoints. To obtain a token, you should use a colon (:) to concatenate the username and password that you use to access your Milvus instance. For example, `root:Milvus`.
