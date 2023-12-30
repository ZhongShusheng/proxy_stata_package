
# ReadMe File for proxy Stata Pacakge
The Stata **proxy** command implements the proxy method used in [Bell (2022)](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4173522) and [Bell, Calder-Wang, and Zhong (2023)](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4565093).

## Installation
- Download **proxy.ado** and **proxy.sthlp** from this repository
- In Stata, type in _sysdir_, find the directory listed as _PERSONAL_
- Put **proxy.ado** and **proxy.sthlp** in the _PERSONAL_ directory

## Syntax
 **proxy** depvar varlist [if] [in], h(varlist) [control(string)] [weight(string)]

## Input List
 - **depvar** the outcome variable 
 - **varlist** the list of amenities 
 - **h** a list of proxy variables (!currently PROXY only supports one proxy variable) 
 - **control** specify the list of control variables; can be fixed effects
 - **weight** specifies weighting options

## Return List
 - **Partial F** Partial F-Stat 
 - **beta"var"** Coefficient for the amenity "var" 
 - **lb_AR"var"** Anderson-Rubin Confidence Interval (Lower Bound) for the amenity "var" 
 - **ub_AR"var"** Anderson-Rubin Confidence Interval (Upper Bound) for the amenity "var" 
 - ereturn stores all the post-estimation results from the baseline regression: reg h varlist depvar

## Examples
### Example 1: Job Safety
- Exercepted from [Bell (2022)](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4173522)
- Import accompanying labor market data. Wage is the outcome variable, safety is the amenity to be priced, and AFQT score is the proxy variable of choice.
  .use safety_proxy_example, clear
- 


