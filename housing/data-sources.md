# Housing: Data Sources & Methodology

## Primary Data Sources

### Hong Kong Government
- **Rating and Valuation Department (R&VD)**: Monthly Price Indices, Rental Indices, Vacancy Rates, Stock Returns
  - URL: https://www.rvd.gov.hk/en/publications/index.html
  - Key Reports: Hong Kong Property Review (annual), Monthly Digest (monthly)
- **Hong Kong Housing Authority (HA)**: PRH stock, wait times, HOS supply, income limits
  - URL: https://www.housingauthority.gov.hk/en/index.html
- **Land Registry**: Transaction data, consideration, instrument types
  - URL: https://www.landreg.gov.hk/en/
- **Census and Statistics Department (CenStatD)**: Household income, dwelling characteristics
  - URL: https://www.censtatd.gov.hk/en/
- **Buildings Department**: Building age, occupation permits, slope registers
- **Urban Renewal Authority (URA)**: Redevelopment projects, acquisition data

### Singapore Government
- **HDB (Housing & Development Board)**: BTO launches, resale prices, grants, eligibility, ethnic quotas
  - URL: https://www.hdb.gov.sg/
  - Key Data: Resale Price Index (quarterly), BTO Application Rates, Sample Prices
- **URA (Urban Redevelopment Authority)**: Private Price Index, Rental Index, Vacancy, Pipeline Supply, GLS Sites
  - URL: https://www.ura.gov.sg/
  - Key Reports: Release of Flash Estimate (quarterly), Property Market Report (quarterly), GLS Programme
- **SLA (Singapore Land Authority)**: Land sales, state land, leasehold info, GCB areas
  - URL: https://www.sla.gov.sg/
- **SingStat (Department of Statistics)**: Household income, dwelling type, ownership rates
  - URL: https://www.singstat.gov.sg/
- **CPF Board**: CPF usage for housing, OA balances, withdrawal rules
  - URL: https://www.cpf.gov.sg/

### Market Data Providers
| Provider | Hong Kong | Singapore | Frequency | Access |
|----------|-----------|-----------|-----------|--------|
| **Centaline / Midland / Centadata** | Transaction prices, rental, indices | — | Daily/Weekly | Paid/Partial free |
| **SRX / PropertyGuru / 99.co** | — | Transaction prices, rental, indices | Daily | Free/Paid |
| **JLL / CBRE / Cushman / Savills / Knight Frank** | Market reports, capital values, yields | Market reports, capital values, yields | Quarterly | Free registration |
| **REITAS / iFAST** | REIT data, yields, NAV | REIT data, yields, NAV | Daily | Free/Paid |
| **Bloomberg / Refinitiv** | Listed developer stocks, REITs, bonds | Listed developer stocks, REITs, bonds | Real-time | Terminal |

### Academic & Think Tanks
- **Hong Kong Institute of Surveyors (HKIS)**: Professional standards, valuation guidelines
- **Singapore Institute of Surveyors and Valuers (SISV)**: Professional standards
- **CUHK / HKU / NUS / SMU** Real Estate Research Centres: Working papers, price models
- **Demographia**: International Housing Affordability Survey (annual)
- **IMF / BIS / OECD**: Housing price databases, policy analysis

## Methodology Notes

### Price Index Construction
- **HK R&VD**: Laspeyres-type chain index, quality-adjusted via hedonic regression, base 1999=100
- **URA Private Price Index**: Stratified median approach, 5 regions, 3 completion periods, base 2009=100
- **HDB Resale Price Index**: Hedonic regression controlling for floor, location, lease, model, base 2009=100

### Affordability Metrics
- **Price-to-Income Ratio**: Median private residential price / median annual household income
  - HK: R&VD median price / CenStatD median household income (monthly × 12)
  - SG: URA median private price / SingStat median household income
  - HDB: HDB median resale / SingStat median household income (citizen households)
- **Median Multiple (Demographia)**: Median house price / median household income
  - Uses metropolitan definitions, internationally comparable

### Rental Yield Calculation
- **Gross Yield**: Annual median rent / median capital value (per psf or per unit)
- **Net Yield**: (Annual rent - management fee - property tax - insurance - vacancy) / capital value
- **HK Management Fee**: ~HK$3-8 psf/mo (luxury higher)
- **SG MCST Fee**: ~S$0.30-0.60 psf/mo + sinking fund

### Leasehold Valuation
- **Bala Curve (SLA)**: Statutory lease extension premium formula (Singapore)
- **HK Lease Extension**: Non-statutory, case-by-case, premium negotiated with Lands Department
- **Empirical Decay**: Regression of transacted price vs. lease remaining (controlling for location, age, size)

### Foreign Buyer Cost Calculation
- **HK**: BSD (1.5-4.25%) + BSD2 (15% non-PR) + SSD (if flip <36m) + Agent (1%) + Legal (0.1-0.2%)
- **SG**: BSD (1-6%) + ABSD (5-65%) + SSD (if flip <3yr) + Agent (1%) + Legal (0.1-0.2%)

## Key Reports (2023-2024)

### Hong Kong
- **Hong Kong Property Review 2024** (R&VD, April 2024)
- **Policy Address 2023/2024** (Housing chapter: 301k target, Northern Metropolis, Lantau Tomorrow)
- **Budget 2024/25** (Stamp duty adjustments, LTV, Special 100% loan guarantee)
- **HKMA Half-Yearly Monetary & Financial Stability Report** (Mortgage survey, DSR, delinquency)
- **Centaline/Centadata Monthly Reports** (Leading indicators, transaction volume)
- **JLL/CBRE Hong Kong Market Updates** (Quarterly, investment focus)

### Singapore
- **URA Property Market Report Q1-Q4 2024** (Flash estimates + full reports)
- **HDB Annual Report 2023/24** (BTO supply, resale stats, grant take-up, waiting times)
- **Budget 2024** (ABSD Apr 2024, property tax progression, carbon tax impact)
- **MAS Financial Stability Review** (Household balance sheet, mortgage stress test)
- **SLA State Land Sales Programme** (GLS confirmed + reserve list)
- **OrangeTee / ERA / PropNex Market Pulse** (Monthly agent-ground reports)

### Comparative
- **Demographia International Housing Affordability 2024** (HK #1, SG not ranked separately)
- **UBS Global Real Estate Bubble Index 2023** (HK: bubble risk, SG: fair valued)
- **Knight Frank Global Cities Index / Prime Global Cities Index** (Quarterly)
- **Savills World Cities Prime Residential Index** (Annual)
- **IMF Housing Watch / BIS Property Price Database** (Cross-country comparable)

## Data Gaps & Limitations

### Hong Kong
1. **Subdivided Units**: Official count ~110k, NGO estimates 200k+ — no transaction data
2. **Offshore Ownership**: Corporate structures, nominees — beneficial ownership opaque
3. **Vacant Units**: R&VD vacancy rate (3-4%) excludes "investment vacant" (held empty)
4. **Pre-1997 Lease Data**: No centralized database of lease terms, renewal premiums
5. **Cross-Border Mortgages**: Mainland income recognition — limited data on default rates

### Singapore
1. **HDB Lease Decay Pricing**: Limited transactions <60yr lease — model-dependent
2. **VERS/SELECTERS Valuation**: No market transactions — compensation formula unknown
3. **PR Buyer Data**: HDB resale by buyer citizenship — aggregated, not granular
4. **En-bloc Pipeline**: Failed attempts not public — only successful ones
5. **Sentosa Cove Foreign Transactions**: Not in URA private index — separate registry

### Both
1. **Shadow Inventory**: Developer-held completed unsold, not in official vacancy
2. **Rental Market**: Private rental transactions not registered (only stamp duty) — sample bias
3. **Renovation/Quality Adjustment**: Indices struggle with quality improvement over time
4. **Household Balance Sheet**: Leveraged vs unlevered returns — microdata restricted

## Citation Format for This Repo
```
[Source] Metric — Value (Period) — [URL/Report Title]
Examples:
[R&VD] Private Domestic Price Index — 310 (Aug 2024, 1999=100) — Hong Kong Property Review 2024
[URA] Private Residential Price Index — 232 (Q2 2024, 2009=100) — URA Flash Estimate Q2 2024
[HDB] 5-Room Resale Median (Woodlands) — S$620,000 (Q2 2024) — HDB Resale Statistics
[CenStatD] Median Monthly Household Income — HK$30,000 (Q2 2024) — Quarterly Report on General Household Survey
[SingStat] Median Monthly Household Income (Citizen) — S$10,869 (2023) — Key Household Income Trends 2023
```

## Update Cadence
| Data Type | Frequency | Primary Source | Repo Update |
|-----------|-----------|----------------|-------------|
| Price Indices | Monthly (HK), Quarterly (SG) | R&VD, URA | Quarterly |
| Transaction Volume | Monthly | Land Registry, URA/Stamp Duty | Monthly |
| Rental Indices | Monthly (HK), Quarterly (SG) | R&VD, URA | Quarterly |
| BTO Launches/Results | Monthly/Quarterly | HDB | Per launch |
| GLS Results | Per tender | URA/SLA | Per result |
| Policy Changes | Ad-hoc | Govt Gazettes, Budget | Immediate |
| REIT Results | Quarterly | SGX, HKEX | Quarterly |
| Demographia Affordability | Annual | Demographia | Annual (Mar) |

## Modeling Assumptions (For Comparison Tables)

### Mortgage Modeling
- **HK**: 30-year amortization, HIBOR+1.5% (floating) or 3.0% fixed 2yr, stress +2%
- **SG**: 25-30 year amortization, 3.0-3.5% (bank) / 2.6% (HDB concessionary), TDSR 55%

### CPF/MPF Modeling
- **HK MPF**: 5% employer + 5% employee, capped HK$18k/yr, no housing withdrawal (except pre-2000)
- **SG CPF**: 20% employee + 17% employer (age <55), OA for housing, BRS/SA protection at 55

### Tax Modeling
- **HK**: Salaries tax 15% standard rate, property tax 15% on net AV, no CGT, no GST
- **SG**: Progressive income tax (max 22-24%), property tax progressive on AV, 9% GST, no CGT

### Inflation/Real Returns
- **Nominal → Real**: HK CPI (2-3%), SG CPI (2-3%) — similar long-run
- **Currency**: HKD/USD pegged (7.75-7.85), SGD managed float (1.30-1.40) — USD basis for comparison