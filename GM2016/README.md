# GM2016, JFE
Paper: Gormley, Todd A., and David A. Matsa. "Playing it safe? Managerial preferences, risk, and agency conflicts." Journal of Financial Economics 122.3 (2016): 431-455.

Contributor: Dian Jiao 

Email: dj2526@columbia.edu

## Introduction
I replicated Table 1, Table 2, and Table A.3 in the paper. 

## Data Description
I use the following data sources:

- CRSP/Compustat Merged - Fundamentals Annual (https://wrds-www.wharton.upenn.edu/pages/get-data/center-research-security-prices-crsp/annual-update/crspcompustat-merged/fundamentals-annual/?saved_query=2861041)
- CRSP/Compustat Merged - Fundamentals Quarterly (https://wrds-www.wharton.upenn.edu/pages/get-data/center-research-security-prices-crsp/quarterly-update/crspcompustat-merged/fundamentals-quarterly/?saved_query=2862850)
- CRSP - Daily Stock File (https://wrds-www.wharton.upenn.edu/pages/get-data/center-research-security-prices-crsp/annual-update/stock-version-2/daily-stock-file/?saved_query=2861103)

I use GVKEY to merge Fundamentals Annual with Fundamentals Quarterly. GVKEY is the primary identifier of Compustat, and using it can guarantee the best matching. To merge the fundamental data with CRSP, I use LPERMNO, and the merged dataset provided by WRDS facilitates the merge. To ensure that unexpected data needs to be entertained, I download the data from 1970 to 2009 and keep the sample from 1976 to 2006 after all the data processing clears. 

## Technical Specification
Coding Language: Python, Stata
Software: jupyter notebook, Stata SE

## Comments
There might be several reasons why the replication results are slightly different from those in the paper, including but not limited to
- The authors used data on historical states of location and incorporation from Cohen (2012). This replication uses “STATE” and “INCORP” from Compustat.
- The CRSP and Compustat datasets are constantly updating the data and the matching between the datasets to retrospectively correct possible errors.
- The programming software and the version of the software might cause differences. 
- There might be nuanced differences in data collection and processing. 
