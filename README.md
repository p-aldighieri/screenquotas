# Screen Quotas: Evidence from the exhibition market in Brazil

Screen quotas in Brazil have been in effect, in their present form, since 2001. Legislation requires movie theaters to screen Brazilian movies for a minimum of days on a yearly basis. Even though two decades have passed since its inception, quantitative analyses of the policy’s eﬀects have been scarce. Furthermore, the policy is set to expire by the end of 2020 and renewal will demand legislative approval.  To investigate policy effects, we run a set of reduced-form regressions, using exogenous variation in the movie theater quotas per viewing room

The details surrounding the policy have changed throughout the years, but a basic feature has remained that quotas set a minimum amount of days of Brazilian feature ﬁlms a movie theater has to screen each year. Interestingly for our purposes, the number of days a multiplex has to fulﬁll is a non-linear function of the number of its viewing rooms, meaning screen quotas per viewing room vary with the size of the movie theater.

## Data

The analysis uses administrative micro-level data from the Brazilian national regulator ([Ancine](https://www.gov.br/ancine/pt-br)). The main sources of data used are:  <b>(a)</b> ticket-sales session-level data from exhibitors, from 2017 to 2019; and <b>(b)</b> inspection reports regarding screen quotas, [publicly](https://antigo.ancine.gov.br/pt-br/fiscalizacao/cinema-fiscalizacao) available. Ticket-sales data was obtained through a [Brazilian Freedom of Information Act](http://www.planalto.gov.br/ccivil_03/_ato2011-2014/2011/lei/l12527.htm) request to Ancine. Movie-theater and chain information was de-identified to preserve protected revenue information.

The whole dataset consists of 12,820,617 individual sessions, spanning 2,178 unique titles (823 of which are Brazilian), 70 movie theater chains, with 928 movie theaters and 3,797 screens.

To run reduced-form regressions, I build a panel grouping data by movie-theater chain/year level, combining information regarding screen quota obligations and fulﬁllment from inspection data. As an auxiliary source of data, we also use Brazilian oﬃcial inﬂation statistics data to correct all prices for inflation using the IPCA price index.

## File description

Cota_fiscalizacao_2017_2019.csv -- Inspection data organized at movie theater-level  (see INSPECTION DATA notebook)

Cota_grupo_fiscalizacao_2017_2019.csv -- Inspection data organized at movie theater-chain level (see INSPECTION DATA notebook)

INSPECTION DATA - Cleaning and organizing.ipynb -- Treating inspection data, outputs Cota_fiscalizacao files

REDUCED-FORM Regressions.ipynb -- Notebook containing all specs, regressions and results

Relat_rio_de_Aferi__o_Cota_de_Tela_-\_2017.xlsx -- Inspection data from Ancine, used as input for INSPECTION DATA notebook

Relat_rio_de_Aferi__o_Cota_de_Tela_-\_2018.xlsx -- Inspection data from Ancine, used as input for INSPECTION DATA notebook

SAD-SCB - cleaning and organizing.csv -- Session-data preparation, exports base files for regressions (SCB_Complexo x Ano and SCB_Grupo x Ano)

SCB_Complexo x Ano - 2017 a 2019 - mesclado fiscalização.csv -- Movie theater yearly revenue and moviegoers, merged with inspection data, ready for regressions

SCB_Complexo x Ano (receita brasileiros) - 2017 a 2019 - mesclado fiscalização.csv -- Movie theater yearly revenue and moviegoers (only for foreign movies), merged with inspection data, ready for regressions

SCB_Complexo x Ano (receita estrangeiros) - 2017 a 2019 - mesclado fiscalização.csv -- Movie theater yearly revenue and moviegoers (only for Brazilian movies), merged with inspection data, ready for regressions

SCB_Grupo x Ano - 2017 a 2019 - mesclado fiscalização.csv -- Movie theater chain yearly revenue and moviegoers, merged with inspection data, ready for regressions

SCB_Grupo x Ano (receita brasileiros) - 2017 a 2019 - mesclado fiscalização.csv -- Movie theater chain yearly revenue and moviegoers (only for foreign movies), merged with inspection data, ready for regressions

SCB_Grupo x Ano (receita estrangeiros) - 2017 a 2019 - mesclado fiscalização.csv -- Movie theater chain yearly revenue and moviegoers (only for Brazilian movies), merged with inspection data, ready for regressions
