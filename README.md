# Todoist Tasks plugin for TRMNL

![Screenshot](https://github.com/shagn/trmnl-todoist/blob/master/screenshot.png?raw=True)

## Description
A TRMNL plugin to show your tasks from Todoist (developed for [BYOS Laravel](https://github.com/usetrmnl/byos_laravel)). 

## Development

Use [trmnlp](https://github.com/usetrmnl/trmnlp/) to run the plugin locally. 

```bash
docker run \
    --publish 4567:4567 \
    --volume ".:/plugin" \
    trmnl/trmnlp serve
```

## Todoist API

The plugin uses the 'Get Tasks' endpoint: https://developer.todoist.com/api/v1/#tag/Tasks/operation/get_tasks_api_v1_tasks_get

```bash
# get all tasks
curl https://api.todoist.com/api/v1/tasks -H "Authorization: Bearer <API_KEY>"

# get all tasks with project_id query parameter
curl https://api.todoist.com/api/v1/tasks?project_id= -H "Authorization: Bearer <API_KEY>"
```


curl https://api.todoist.com/api/v1/tasks?project_id=6fhHx97v9XMxFQjr -H "Authorization: Bearer 4f70075ea642a159462ba2fe6f5b153a4af1361a"