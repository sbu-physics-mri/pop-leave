# Leave Populator

Asks the minimum amount of questions to populate a leave request form.

## Installation

### Recommended

```sh
pip install popleave
```

### Local installation

1. Install [poetry](https://python-poetry.org/docs/#installation) following the official guidelines for your system.

2. Clone the repository.

3. Install the dependencies.

```sh
poetry install
```

## Usage

### First run

Run the program with

```sh
popleave
```

On the first run, you will be asked for your name:

```
Enter name (press Enter to use Samwise Gamgee): 
```

and your department:

```
Enter department (press Enter to use The Shire):
```

and the current amount of days holiday you have remaining:

```
Enter remaing_days_leave (press Enter to use 26):
```

If you ever need to change or correct these details, pass the `--init` flag when running the script:

```sh
popleave --init
```
and you will be able to update the values accordinly.

### Populating a form

When run you will then be prompted for:

- The start date of your leave.
- The duration of your leave.
- The reason for your leave.

If you'd rather, you can use commandline arguments.
A full list of commandline arguments can be found by using the `--help` flag.

```sh
usage: popleave    [-h] [-i] [-s START_DATE] [-e END_DATE] [-d DURATION]
                   [-r REASON] [-t]

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
  -t, --toil            Fills out Time Off In Leu instead of annual leave.
```

All resulting forms will be stored in the current directory in the format `INITIALS_ANNUAL_STARTDATE.docx`.
Thus Samwise Gamgee requesting some leave starting on 1969-12-31 will result in:
```
SG_ANNUAL_31121969.docx
```

## License

This project is licensed under the [GPLv3 license](LICENSE).

## Contributing

All contributions welcome. Submit a pull a request or create an issue to start the ball rolling.
