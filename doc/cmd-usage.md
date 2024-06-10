← [Back to menu](./toc.md)

# Installation

## Requirements
- [nodejs](https://nodejs.org/en)

## Download
From Github ...

# Command line

```sh
node invert.js —help
```

This will display
```sh
Usage: stress-cmd [options]

Tecto-Stress is a web application that enables tectonic stress inversion
by utilizing various types of data such as fault striae, fracture orientation...,
and combining them to better constrain the inversion.

Options:
  -v, --vers             output the current version
  -h, --help             display help for command
  jsonFile               the model configuration file
```

To run an inversion using data and options
```sh
node invert.js model.json
```
## JSON format of the model
For a given dataset, the `file` can be any known format (`json`, `csv`...).
```json
{
    "dataset": [
        {
            "file": "stylos/stylolites-1.json",
            "weight": 0.83, // optional, default 1
            "active": true // optional, default true
        },
        ...
    ],
    "options": {
        "searchMethod": {
            "name": "Monte Carlo",
            "nbIter": 50000
        },
        "stressRatio": {
            "min": 0.7,
            "max": 0.9
        }
    }
}
```

## JSON format of the data
A json dataset is simply an Array of data. Each data has the following structure:
```ts
{
    "id": number,
    "type": string,
    "strike": number,
    "dip": number,
    "dipDirection": string,
    "normal": [number, number, number],
    ...
    "weight": 1,
    "active": true
}
```

### Examples
```json
[
    {
        "id": 1,
        "type": "extension fracture",
        "strike": 45,
        "dip": 90,
        "dipDirection": "SE",
        "normal": [-0.707, 0.707, 0]
    },
    {
        "id": 8,
        "type": "Striated Plane",
        "strike": 315,
        "dip": 30,
        "dipDirection": "W",
        "rake": 90,
        "strikeDirection": "N",
        "typeOfMovement": "N",
        "normal": [-0.353, -0.353, 0.866]
    }
]
```

## JSON format for the options

### Example
```json
{
    "searchMethod": {
        "name": "Monte Carlo",
        "nbIter": 50000
    }
}
```
