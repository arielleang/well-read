# Delete a book by ID

Deletes the [book](book.md) object specified by the `id` parameter, if it exists.

## Method

`DELETE`

## URL

```shell

{base_url}/books/{id}
```

## Parameters

| Parameter name | Type   | Description | Required? |
| ------------- | ------ | ----------- | --------- |
| `id` | number | The book's unique record ID | Yes |

## Request headers

None

## Request body

None

## Return body

Returns an empty object.

```js
{}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
