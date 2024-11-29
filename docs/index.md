

# Type of competition
Only onsite competitions are accepted into the Open Functional Fitness Data repository.


# Data

## Folder structure
the `data` folder is structured as follows
- first level: abbreviation of the competition organizer, federation or association
- second level: folder for each competition & division `YY%3d` (year and 3-digit number) 
- third level: files
    - `table.csv` - the result table with ranks and scores (e.g. times, reps, points, cap, etc.)
    - `comp.json` - meta information about the competition, e.g. date, venue/location, name, organizer, etc.
    - `tests.txt` - information about the tests/workouts
    - `analytics-zscores.csv` - normalized data for sport analytics purposes
    - `original.*` raw data file (e.g. CC JSON export, leaderboard.com CSV file)


# Name Matching

## Ambiguous Names
Name disambiguation will not work for larger populations. 
The file `athletes/ambiguous.csv` contains names 
that we have identified as belonging to several different individuals.
These names are excluded from name based data matching. 


## Athlete ID
We recommend that competition organizers offer a custom registration field `openff_athlete_id` (for UUID4).
And athlete should add their the `id` used in the file `athletes/athletes.json`

## Claiming competition results
Athletes can claim competition results by opening an issue 
at https://github.com/openfunctionalfitness/openff-data/issues

and providing the following information

* the athlete URL (what contains their `openff_athlete_id`), and
* the competition results that is not linked to their name.



# Name Redaction

## Redacting for Privacy
OpenFunctionalFitness collects public data from sport competitions.

The GDPR operates on the basis of user consent withdrawal,
what does not apply here, because:

- OpenFunctionalFitness does not have users.
- The public record of sport has no consent requirement.

Although not required by law, we can redact athletes' names
while preserving the accuracy of the historical record.

## How to redact
Make a pull-request on the file `athletes/redaction-requests.csv`

