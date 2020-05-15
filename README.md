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
