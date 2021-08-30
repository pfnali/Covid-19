# Empirical trends of Covid-19 outbreak in Italy: a standard spreadsheet analysis.
Our approach to analyzing the temporal evolution of the COVID-19 and other epidemic outbreaks is purely empirical. We limit ourselves using some phenomenological models that proved useful in the past to reproduce the patterns observed in time series data. Among them you can choose the best suitable growth model for a given outbreak. The advantage of this approach consists in providing a fairly simple temporal description of epidemic growth trends through macroscopic laws of simple mathematical form, as in [[1]](#1). The word "macroscopic" is intended here in the sense that these growth laws do not rest on a theory grounded on underlying microscopic laws or mechanisms, physical and / or biological, that may be difficult to identify ("theory-less" models), but on a small number of model parameters that can be easily calibrated to obtain a fit to (and possibly a prediction of) the observed data with defined uncertainty, as in [[2]](#2). The models are realized on the Excel spreadsheet with the SOLVER add-in (free of charge) we use for parameter calibration. The worksheets are structured with the aim of rendering the presentation of the results dynamic. Epidemic data sets are imported online from the repository of the italian Protezione Civile https://github.com/pcm-dpc/COVID-19 to data tables in the worksheets. The use of worksheet labels, structured references, and other Excel features in the spreadsheet, facilitate dynamic rendering of model results, as in [[3]](#3) and [[4]](#4). The choice of the Excel spreadsheet to build the models is due, besides simplicity, to its widespread knowledge among physicians and biologists. The data refer to Italy (easily adaptable to other countries), the considered parametric models are three- and four-parameter.

- Three-parameter models:
  - Power Law with exponential cut off (PL-ECO) [[5]](#5), [[6]](#6)
  - Boltzmann ion channel (logistic-like)
  - Gompertz-like
- Four-parameter models:
  - Generalized Gompertz Model (GGoM) [[2]](#2)
  - Lognormal with estimated starting and ending points [[7]](#7)
  - basic SIR for cumulative and new removals with estimated starting point and basic reproductive rate [[8]](#8), [[9]](#9)

Though the detected cases do not certainly represent the totality of cases and the uncertainties on Italy's data are still enormous, we may perhaps reasonably confirm that we left the exponential phase around March the 16th. My analysis is very gross for now (March 2020). Here is a nonlinear regression analysis of Covid-19 confirmed cases in Italy (whole country) from Feb. the 24th to March the 21th: https://github.com/pfnali/Covid-19. The Boltzmann sigmoidal (logistic) function and the gompertzian macroscopic growth law were used to model data. These models are somewhat arbitrary but they have empirically shown to work well enough for Chinese data (see [1]). The iteration procedure uses the SOLVER function of the Excel spreadsheet based on the generalized reduced gradient (GRG) algorithm. The method is depicted in ref. [2]. See also ref. [3] for a similar protocol. 

I have applied a generalized logistic model to my analysis of the outbreak trajectories in Italy. The model is tuned by a scaling parameter p governing different growth rates (0 = exponential growth, 1 = pure logistic, 0 < p <1 intermediate trends). The fits show at glance the different progression of the outbreak in the examined areas. Lombardy is closer to saturation than Italy's average and the rest of Italy regions lag behind. On April the 18th Lombardy reached 90% saturation (= accumulated number of deaths when daily deaths fall to zero), against 84% of the Italy average and 74% of the rest of the country. The corresponding values ​​of the scaling parameter are: p = 0.77 for Lombardy, p = 0.71 for Italy average and p = 0.66 for the rest of the regions, showing that growth is far from exponential trend and in Lombardy it is even more so. All in all, the whole trend is closer to a logistic-like curve. In the plots comparing daily vs. accumulative growth, x-y axes are rescaled to the unit, just as the y axis in the plots of growth over time. The model (not posted on github) does not have an explicit analytical solution and it is approximated by numerically integrated DDEs. 

The lockdown starting date apparently coincides with the stop of the exponential growth of the acceleration of the daily cases (variation rate of the new cases per day). This coincidence was noticed in Olsson & Zhang paper at https://www.preprints.org/manuscript/202003.0077/v4 on Chinese data and confirmed also for Italy. What may be suprising more than the effect in itself is its instantaneousness. Is this something general or a mere coincidence limited to those two countries? (from my check on the Spanish data, the latter seems more likely). As a first check I fitted the Protezione Civile reported cases in Italy with a standard lognormal distribution. The plots have show some results obtained with this model. The acceleration graph (derivative of the new cases per day curve) indeed shows a peak near the lockdown starting date after which the descent begins. This is best seen in a plot where some indicators (doubling and halfing time, growth rate), normalized to their values ​​on the day of the lockdown, are grouped. It shows that acceleration has a maximum exactly at lockdown starting date (assumed March the 11th for Italy). There is a difference between different Italian regions exemplified by a log-linear plot showing the halfing time divaricated for Lombardy that is falling slower than for the rest of the country. This same difference applies to the growth rate. Finally, two log-linear plots that cut the time axis when the number of new cases per day drops below 1, illustrate how a rough estimate on the ending point of the spreading can be made (result: last case around September 4 for Lombardy, August 24 for the rest of the country). For details see at https://github.com/pfnali/Covid-19.

## References
<a id="1">[1]</a> 
P. Castorina, A. Iorio and D. Lanteri, Data analysis on Coronavirus spreading by macroscopic growth laws, arXiv:2003.00507.

<a id="2">[2]</a>  
R. Bürger, G. Chowell and L. Y. Lara-Díaz, Comparative analysis of phenomenological growth models applied to epidemic outbreaks, Mathematical Biosciences and Engineering 16 (2019) 4250-4273, doi: 10.3934/mbe.2019212.

<a id="3">[3]</a> 
A. M. Brown, A step-by-step guide to non-linear regression analysis of experimental data using a Microsoft Excel spreadsheet, Computer Methods and Programs in Biomedicine 65 (2001) 191–200.

<a id="4">[4]</a>
G. Kemmer and S. Keller, Nonlinear least-squares data fitting in Excel spreadsheets, Nature Protocols 5 (2010) 267-281.

<a id="5">[5]</a>
A. L. Ziff and R. M. Ziff, Fractal kinetics of COVID-19 pandemic, medRxiv 2020.02.16.20023820, https://doi.org/10.1101/2020.02.16.20023820.

<a id="6">[6]</a>
A. Vazquez, Polynomial Growth in Branching Processes with Diverging Reproductive Number, Phys. Rev. Lett. 96 (2006) 038702, https://doi.org/10.1103/PhysRevLett.96.038702.

<a id="7">[7]</a>
S. Olsson and J. Zhang, The Ongoing COVID-19 Epidemic Curves Indicate Initial Point Spread in China With Log-Normal Distribution of New Cases per Day With a Predictable Last Date of the Outbreak Version 4: Predictions for Selected European Countries, USA and the World as a Whole and Try to Predict the End of the Outbreak Including a Discussion of a Possible “New Normal”, Preprints 2020, 2020030077, doi: 10.20944/preprints202003.0077.v4. 

<a id="8">[8]</a>
W. O. Kermack and A. G. McKendrick, A Contribution to the Mathematical Theory of Epidemics, Proceedings of the
Royal Society of London A 115 (1927) 700-721, https://www.jstor.org/stable/94815.

<a id="9">[9]</a>
D. Sulsky, Using real data in an SIR model (2015) https://www.math.unm.edu/~sulsky/mathcamp/ApplyData.pdf.
