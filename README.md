# Github repositories' key metrics

Get your github account's repositories' key data and traffic metrics.

* title
* slug
* description
* url
* link
* type
* views number
* clones number
* unique views number
* stars number
* watchers number
* open issues number

## Preparation

In the "script" directory, there is a file called `process.py` which will generate a csv file, containing all items listed above.

## Instructions:

1. Download "requirements.txt" and "process.py" from the `script` directory
2. Go to your terminal, navigate to the folder where you saved the files and use the following command to run the dependencies 

`pip install -r requirements.txt`

! If you receive an error, check the Troubleshooting section below.

3. Run `cp .env.example .env` and fill out the options for: 

`ORGANIZATION`: here goes the name of the user or the organization whose repositories you want to scrape

`GITHUB_TOKEN`: here goes your personal private token. You can get yours from the [Github settings](https://github.com/settings/tokens).

4. Run the process.py script by using the following command

`python process.py`

5. Voilà! You will find a CSV file called `repos-metrics.csv` in a new directory called `data`.

## Troubleshooting requirements install

The packages PyGithub and PyGithub3 can trigger a conflict during the installation. 

If you receive the error message `from github import Github ModuleNotFoundError: No module named 'github'` during the `pip install -r requirements.txt` phase, please run: 

`$ pip install PyGithub` and then again:

`$ pip install -r requirements.txt`

## License

This Data Package is made available under the Public Domain Dedication and License v1.0


