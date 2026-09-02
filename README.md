# تحليل البيانات باستخدام آر

مواد تدريبية بالعربية لتحليل البيانات باستخدام R و tidyverse.

| الملف | الوصف |
|:------|:------|
| `index.Rmd` | الدورة الأساسية (3 أيام): أساسيات R، استكشاف البيانات، ggplot2، dplyr، tidyr، الربط، القيم المفقودة |
| `tidyverse_one_day.Rmd` | **دورة يوم واحد (8 ساعات) للمستوى المتوسط في tidyverse** |
| `exercises/tidyverse_one_day_exercises.Rmd` | دفتر تمارين المتدرب لدورة اليوم الواحد |
| `exercises/tidyverse_one_day_solutions.Rmd` | حلول التمارين والمشروع الختامي |
| `data/` | البيانات المستخدمة: `flights.csv`, `airlines.csv`, `gapminder.csv`, `riskfactors.csv`, `diamonds.csv` |

## One-day tidyverse training (intermediate)

An 8-hour, hands-on course built on the same xaringan + flipbookr style as the
3-day course. It assumes participants already know basic R and the core dplyr
verbs, and pushes into the tidyverse features an intermediate analyst uses daily.

### Schedule

| Time | Block | Topic | Exercise |
|:-----|:------|:------|:---------|
| 09:00 – 09:30 | Opening | Why tidyverse, the pipe (`%>%` / `\|>`), tibbles, workflow | |
| 09:30 – 10:30 | Module 1 | `readr` column types, core dplyr verbs review, `count`/`distinct`/`slice_*`, `case_when` | 15 min |
| 10:30 – 10:45 | Break | | |
| 10:45 – 12:00 | Module 2 | `across()`, tidy-select helpers, `.by`, grouped `mutate`, window functions, `rowwise`, `pick`, `reframe` | 20 min |
| 12:00 – 13:00 | Lunch | | |
| 13:00 – 14:00 | Module 3 | Tidy data, `pivot_longer` with `.value`, `pivot_wider`, `separate_wider_*`, `complete`, `fill`, `nest` | 15 min |
| 14:00 – 14:45 | Module 4 | Joins with `join_by`, key checks, `relationship`/`unmatched`, inequality and rolling joins, filtering joins | 10 min |
| 14:45 – 15:00 | Break | | |
| 15:00 – 15:45 | Module 5 | `stringr` + regex, `forcats`, `lubridate` | 15 min |
| 15:45 – 16:30 | Module 6 | `purrr` map family, `nest` + `map` models, `walk2`, writing functions with `{{ }}` and `:=` | 15 min |
| 16:30 – 17:00 | Closing | Capstone: which airline is most on time?, recap, references | 30 min |

### Requirements

- R >= 4.1 and RStudio
- `tidyverse` >= 2.0 (dplyr >= 1.1, tidyr >= 1.3, purrr >= 1.0)
- To render the slides: `xaringan`, `xaringanthemer`, `xaringanExtra`, `flipbookr`

```r
install.packages(c("tidyverse", "xaringan", "xaringanthemer", "rmarkdown"))
remotes::install_github(c("gadenbuie/xaringanExtra", "EvaMaeRey/flipbookr"))
```

### Render

Run from the project root (the `.Rproj` directory):

```r
rmarkdown::render("tidyverse_one_day.Rmd")                      # slides
rmarkdown::render("exercises/tidyverse_one_day_exercises.Rmd")  # participant workbook
rmarkdown::render("exercises/tidyverse_one_day_solutions.Rmd")  # solutions (runs all code)
```

All slide code and every solution were executed against the files in `data/`
with R 4.3 and tidyverse 2.0 (dplyr 1.1.4, tidyr 1.3.1, purrr 1.0.2).
