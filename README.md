# MovieLens 1M — Rating Patterns

**Explore movie-rating distributions, group means, and disagreement using relational joins in pandas.**

An educational analysis of the MovieLens 1M dataset. The notebook joins users, ratings, and movie metadata, filters sparse titles, and compares rating patterns. It is not a recommendation engine or evidence of a commercial engagement.

## Dataset and reproduced results

| Measure | Value |
| --- | --- |
| Ratings | 1,000,209 |
| Users | 6,040 |
| Movie metadata records | 3,883 |
| Titles with at least 250 ratings | 1,216 |

These counts were recomputed during review. The 250-rating threshold applies to total ratings per title, not to each demographic subgroup.

## Run locally

```bash
git clone https://github.com/joaovitormessias/conjunto-de-dados-movielens-1M.git
cd conjunto-de-dados-movielens-1M
python -m venv .venv
source .venv/bin/activate
pip install pandas jupyter
jupyter notebook ConjuntoMovieLens1M.ipynb
```

Run all cells from the repository directory. Data files are included. The loaders use relative paths, the `::` separator, and Latin-1 encoding. The rating time field is named `timestamp`; it is not a movie duration.

## Technical walkthrough

- [Notebook](ConjuntoMovieLens1M.ipynb): loading, joins, pivot tables, minimum-count filtering, and rating dispersion.
- [users.dat](users.dat): historical user attributes.
- [ratings.dat](ratings.dat): user/movie ratings with timestamps.
- [movies.dat](movies.dat): title and genre metadata.

Comparing averages without checking sample size can overstate a group's preference. Treat the notebook's group labels as the dataset's historical categories, not comprehensive descriptions of identity or evidence of causation.

## Verification and limits

All 24 nonempty code cells executed in order during review. There is no predictive evaluation, fairness audit, or causal experiment. Dependencies are not locked. The dataset is historical and self-selected; findings do not generalize automatically to today's audience.

Code is distributed under the repository's [MIT license](LICENSE). Dataset terms and attribution are separate: consult [GroupLens MovieLens](https://grouplens.org/datasets/movielens/1m/).

[Maintainer](https://github.com/joaovitormessias)
