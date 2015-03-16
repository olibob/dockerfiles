# Sickbeard

A dockerfile for sickbeard based on their git repository.

## Ports

`8081`

## Volumes

`/media` and `/config`

## Usage

```
docker run -d --name sic -p 8081:8081 -v /your_config:/config -c /your_media:/media olibob/sickbeard
```
