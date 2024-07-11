# Leave Populator

Asks the minimum amount of questions to populate a leave request form.

## Installation

1. Install [poetry](https://python-poetry.org/docs/#installation) following the official guidelines for your system.

2. Install the dependencies.

```sh
poetry install
```

## Usage

Run the program with

```sh
poetry run python src/populate.py
```

On the first run, you will be asked for your name:

```
Enter name (press Enter to use Samwise Gamgee): 
```

and the current amount of days holiday you have remaining:

```
Enter remaing_days_leave (press Enter to use 26):
```

If you ever need to change or correct these details, pass the `--init` flag when running the script:

```sh
poetry run python src/populate.py --init
```
and you will be able to update the values accordinly.

You will then be prompted for:

- The start date of your leave.
- The duration of your leave.
- The reason for your leave.

If you'd rather, you can use commandline arguments.
A full list of commandline arguments can be found by using the `--help` flag.

```sh
usage: populate.py [-h] [-i] [-s START_DATE] [-e END_DATE] [-d DURATION]
                   [-r REASON]

Populates the leave of absence form with a CLI

options:
  -h, --help            show this help message and exit
  -i, --init            Forces reinitialisation of config file.
  -s START_DATE, --start_date START_DATE
                        Start date in YYYY-MM-DD format.
  -e END_DATE, --end_date END_DATE
                        End date in YYYY-MM-DD format.
  -d DURATION, --duration DURATION
                        Duration in days.
  -r REASON, --reason REASON
                        Reason for leave.
```    