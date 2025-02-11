---
id: es-index-tags
title: tags
---


## _id

The `_id` field of this index is represented by the tag name in a base64 encoding.

## Fields

| Field | Description                                                         |
|-------|---------------------------------------------------------------------|
| count | The count field represents the number of NFTs with the current tag. |
| tag   | This field represents the tag in an alphanumeric format.            |

## Query examples

### Fetch NFTs count with a given tag

```
curl --request GET \
  --url ${ES_URL}/tags/_search \
  --header 'Content-Type: application/json' \
  --data '{
	"query": {
		"match": {
			"tag":"sport"
		}
	}
}'
```
