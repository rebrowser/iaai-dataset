# IAAI Insurance Auto Auction Dataset

![Updated](https://img.shields.io/badge/updated-2026--03--16-brightgreen?style=flat-square)&nbsp;![Records](https://img.shields.io/badge/records-455k-blue?style=flat-square)&nbsp;[![Rebrowser](https://img.shields.io/badge/full%20dataset-rebrowser.net-orange?style=flat-square)](https://rebrowser.net/products/datasets/iaai)

Daily sample of IAAI insurance auto auction lots with damage assessments, title status, bidding data, and branch locations across North America.


This repository contains a preview sample of the [IAAI dataset](https://rebrowser.net/products/datasets/iaai) published by Rebrowser. If you're doing academic research, you may be eligible for free access to a much larger slice — see [Free Datasets for Research](https://rebrowser.net/free-datasets-for-research).


This dataset contains **1** entity, each in its own folder: Auction Listings (`auction-listings`). See below for a full field breakdown, sample counts, and data distributions for each.

*Found this useful? ⭐ Star this repo to help us keep publishing fresh data. Found an error? [Let us know](https://rebrowser.net/contact-us).*


---

### Auction Listings
IAAI insurance auto auction lots with vehicle specs, damage classifications, loss types, title status, mileage, drivetrain, branch locations, and auction scheduling.




> **454,606** total records from 2025-11-16 to 2026-03-15, **up to 30,000** rows in this sample (6.6% of full dataset).
> Exported as one file per day, up to 1,000 rows each, last 30 days retained.

![Data Growth](auction-listings/chart-growth.svg)

| Field | Type | Fill Rate | Description |
| --- | --- | --- | --- |
| `_primaryKey` | `string` | 100% | Unique identifier for this record |
| `_firstSeenAt` | `datetime` | 100% | First time this record was seen |
| `_lastSeenAt` | `datetime` | 100% | Last time this record was updated |
| `stockNumber` | `string` | 100% | Unique IAA stock number (auction identifier) |
| `itemId` | `string` | 100% | IAA item ID for the auction listing |
| `salvageId` | `string` | 100% | IAA salvage ID (used in image URLs) |
| `auctionId` | `string` | 100% | IAA auction ID |
| `vin` 🔒 | `string` | 100% | Vehicle Identification Number |
| `vinStatus` | `string` | 100% | VIN validation status (OK, Missing, Damaged, Retagged, Altered) - fraud indicator |
| `year` | `float` | 100% | Vehicle model year |
| `make` | `string` | 100% | Vehicle manufacturer (e.g., CHEVROLET, TOYOTA) |
| `model` | `string` | 100% | Vehicle model name (e.g., SILVERADO 1500, CAMRY) |
| `series` | `string` | 90% | Vehicle series/trim (e.g., LTZ, SE, LS) |
| `bodyStyle` | `string` | 100% | Body style (SEDAN, EXTENDED CAB, SUV, COUPE, etc.) |
| `exteriorColor` | `string` | 100% | Exterior color (WHITE, BLACK, GRAY, etc.) |
| `vehicleType` | `string` | 100% | Inventory type (AUTOMOBILE, MOTORCYCLE, etc.) |
| `vehicleCategory` | `string` | 100% | Inventory category (VEHICLE, EQUIPMENT, etc.) |
| `vehicleClass` | `string` | 100% | Vehicle class (Sedan, Truck, SUV, Coupe, etc.) |
| `inventoryStatus` | `string` | 100% | Inventory status code (RS = Ready for Sale) |
| `interiorColor` | `string` | 22% | Interior color |
| `engine` | `string` | 100% | Engine description (e.g., "5.3L V-8 285HP") |
| `cylinders` | `float` | 98% | Number of engine cylinders |
| `transmission` | `string` | 100% | Transmission type (Automatic, Manual, Unknown) |
| `drivetrain` | `string` | 100% | Drivetrain type (FWD, RWD, 4x4, AWD) |
| `fuelType` | `string` | 100% | Fuel type (Gasoline, Diesel, Electric, Hybrid, FlexibleFuel) |
| `hybridIndicator` | `bool` | 100% | Whether vehicle is a hybrid |
| `primaryDamage` | `string` | 100% | Primary damage (FRONT END, REAR, LEFT SIDE, etc.) |
| `primaryDamageCode` | `string` | 100% | Primary damage code (F, R, LF, RF, etc.) |
| `secondaryDamage` | `string` | 49% | Secondary damage description |
| `secondaryDamageCode` | `string` | 49% | Secondary damage code |
| `lossType` | `string` | 100% | Loss type (Collision, Theft, Fire, Water, Other) |
| `lossTypeCode` | `string` | 100% | Loss type code (0=Collision, 1=Fire, 2=Other, 3=Theft, 4=Water) |
| `titleType` | `string` | 100% | Title document type (BillOfSale, Certificate, etc.) |
| `titleCode` | `string` | 100% | Title code (SAL=Salvage, CLR=Clear, ORG=Original, BOS=Bill of Sale, NRP=Non-Repairable, JNK=Junk) |
| `titleBrand` | `string` | 10% | Title brand (REBUILT, REPAIRABLE, REPOSSESSED, etc.) |
| `titleState` | `string` | 100% | State where title is held (e.g., TX, CA, FL) |
| `titleNotes` | `string` | 10% | Additional title notes/conditions |
| `tboIndicator` | `bool` | 100% | Title Buyer Only - requires special buyer license |
| `hasKeys` | `bool` | 100% | Whether keys are present |
| `runAndDrive` | `bool` | 100% | Whether vehicle runs and drives - critical for buyers |
| `startsDesc` | `string` | 100% | Start condition (Starts, Stationary) |
| `mileage` | `float` | 93% | Odometer reading in miles |
| `odometerBrand` | `string` | 100% | Odometer status (ACTUAL, NOT ACTUAL, NOT REQUIRED/EXEMPT, EXCEEDS MECHANICAL LIMITS, MISSING) |
| `odometerUnit` | `string` | 100% | Odometer unit of measure (mi, km) |
| `airbagState` | `string` | 100% | Airbag condition (Intact, Deployed, Missing, None) |
| `vehicleGrade` | `float` | 91% | Vehicle condition grade (0-100 scale) |
| `vehicleCondition` | `string` | 21% | Overall condition (Complete, Partially Dismantled, Body Only, Frame Only) |
| `catalyticConverter` | `string` | 100% | Catalytic converter status (Present, Missing) - theft indicator |
| `battery` | `string` | 21% | Battery status (Present, Missing, etc.) |
| `radiator` | `string` | 21% | Radiator status (Present, Missing, Damaged) |
| `crExists` | `bool` | 100% | Whether condition report exists |
| `buyNowPrice` 🔒 | `float` | 100% | Buy Now price in USD |
| `minimumBidAmount` 🔒 | `float` | 100% | Minimum bid amount in USD |
| `estimatedRepairCost` 🔒 | `float` | 100% | Estimated repair cost in USD |
| `auctionDateTime` | `datetime` | 100% | Scheduled auction date and time |
| `timedAuctionIndicator` | `bool` | 100% | Whether this is a timed/online auction |
| `buyNowIndicator` | `bool` | 100% | Whether Buy Now is available |
| `currencyCode` | `string` | 100% | Currency code for prices (USD, CAD, etc.) |
| `branchNumber` | `string` | 100% | IAA branch/facility number |
| `branchName` | `string` | 100% | IAA branch/facility name (e.g., "Salt Lake City (UT)") |
| `branchState` | `string` | 100% | Branch state code |
| `branchLink` | `string` | 100% | Branch link identifier (e.g., "342~US") |
| `locationName` | `string` | 100% | Storage location name |
| `locationAddress` | `string` | 100% | Storage location street address |
| `locationCity` | `string` | 100% | Storage location city |
| `locationState` | `string` | 100% | Storage location state |
| `locationZip` | `string` | 100% | Storage location ZIP code |
| `locationPhone` | `string` | 100% | Storage location phone number |
| `locationLatitude` | `float` | 100% | Storage location latitude (for shipping cost calculations) |
| `locationLongitude` | `float` | 100% | Storage location longitude (for shipping cost calculations) |
| `isOffsite` | `bool` | 100% | Whether vehicle is stored offsite |
| `aisle` | `string` | 93% | Storage aisle location |
| `stall` | `string` | 93% | Storage stall number |
| `sellerName` 🔒 | `string` | 84% | Seller/provider name |
| `providerType` | `string` | 100% | Provider type (INS=Insurance, RCC=Remarketing, DLR=Dealer, COR=Corporate, SDS=Specialty, SAL=Salvage, ADJ=Adjuster, GOV=Government, FIN=Finance) |
| `origin` | `string` | 100% | Vehicle origin (Insurance, Repossession, Remarketing Vehicles, Donation, IAA Purchase, Lease/Rental) |
| `countryOfOrigin` | `string` | 100% | Country where vehicle was manufactured |
| `whoCanBuy` | `string` | 66% | Buyer type codes (DEA=Dealer, DIS=Dismantler, EXP=Exporter, REB=Rebuilder, PUB=Public, etc.) |
| `catIndicator` | `bool` | 100% | Catastrophe/flood vehicle indicator - important disclosure |
| `imageUrl` 🔒 | `string` | 92% | Main image URL |
| `image360Url` 🔒 | `string` | 68% | 360-degree view URL |
| `updatedAt` | `datetime` | 100% | Timestamp when IAA last updated the listing |
| `listingUrl` 🔒 | `string` | 100% | Full URL to the IAA vehicle listing page |



> 🔒 **Premium fields** are included in the data files but their values are replaced with `[PREMIUM]`. To access real values, [use our website](https://rebrowser.net/products/datasets/iaai).



#### Field Distributions


<details>
<summary><strong>Loss Type Distribution</strong> (<code>lossType</code>)</summary>


| Value | Count | Share |
| --- | --- | --- |
| Collision | 317,861 | `██████████████░░░░░░` 69.9% |
| Other | 123,350 | `█████░░░░░░░░░░░░░░░` 27.1% |
| Theft | 7,525 | `░░░░░░░░░░░░░░░░░░░░` 1.7% |
| Fire | 3,652 | `░░░░░░░░░░░░░░░░░░░░` 0.8% |
| Water | 2,218 | `░░░░░░░░░░░░░░░░░░░░` 0.5% |

</details>


<details>
<summary><strong>Primary Damage Location</strong> (<code>primaryDamage</code>)</summary>


| Value | Count | Share |
| --- | --- | --- |
| FRONT END | 160,283 | `████████░░░░░░░░░░░░` 40.5% |
| REAR | 39,926 | `██░░░░░░░░░░░░░░░░░░` 10.1% |
| LEFT SIDE | 32,066 | `██░░░░░░░░░░░░░░░░░░` 8.1% |
| RIGHT SIDE | 30,146 | `██░░░░░░░░░░░░░░░░░░` 7.6% |
| NORMAL WEAR & TEAR | 26,983 | `█░░░░░░░░░░░░░░░░░░░` 6.8% |
| LEFT FRONT | 26,445 | `█░░░░░░░░░░░░░░░░░░░` 6.7% |
| RIGHT FRONT | 26,309 | `█░░░░░░░░░░░░░░░░░░░` 6.6% |
| FRONT & REAR | 23,064 | `█░░░░░░░░░░░░░░░░░░░` 5.8% |
| UNKNOWN | 18,733 | `█░░░░░░░░░░░░░░░░░░░` 4.7% |
| LEFT REAR | 12,136 | `█░░░░░░░░░░░░░░░░░░░` 3.1% |

</details>


<details>
<summary><strong>Vehicle Class Distribution</strong> (<code>vehicleClass</code>)</summary>


| Value | Count | Share |
| --- | --- | --- |
| Sedan | 285,561 | `█████████████░░░░░░░` 63.7% |
| Truck | 83,401 | `████░░░░░░░░░░░░░░░░` 18.6% |
| Hatchback | 31,163 | `█░░░░░░░░░░░░░░░░░░░` 7.0% |
| Coupe | 20,927 | `█░░░░░░░░░░░░░░░░░░░` 4.7% |
| Sedan/Hatchback | 9,544 | `░░░░░░░░░░░░░░░░░░░░` 2.1% |
| Convertible | 6,250 | `░░░░░░░░░░░░░░░░░░░░` 1.4% |
| Hatchback/Crossover | 5,534 | `░░░░░░░░░░░░░░░░░░░░` 1.2% |
| Wagon | 3,309 | `░░░░░░░░░░░░░░░░░░░░` 0.7% |
| Wagon/Hatchback | 1,416 | `░░░░░░░░░░░░░░░░░░░░` 0.3% |
| Wagon/Crossover | 1,186 | `░░░░░░░░░░░░░░░░░░░░` 0.3% |

</details>


<details>
<summary><strong>Title Code Distribution</strong> (<code>titleCode</code>)</summary>


| Value | Count | Share |
| --- | --- | --- |
| OTH | 202,271 | `█████████░░░░░░░░░░░` 44.5% |
| SAL | 153,669 | `███████░░░░░░░░░░░░░` 33.8% |
| CLR | 64,115 | `███░░░░░░░░░░░░░░░░░` 14.1% |
| ORG | 23,639 | `█░░░░░░░░░░░░░░░░░░░` 5.2% |
| BOS | 8,578 | `░░░░░░░░░░░░░░░░░░░░` 1.9% |
| NRP | 1,666 | `░░░░░░░░░░░░░░░░░░░░` 0.4% |
| JNK | 668 | `░░░░░░░░░░░░░░░░░░░░` 0.1% |

</details>


<details>
<summary><strong>Vehicle Origin</strong> (<code>origin</code>)</summary>


| Value | Count | Share |
| --- | --- | --- |
| Insurance | 348,437 | `███████████████░░░░░` 76.6% |
| Remarketing Vehicles | 64,125 | `███░░░░░░░░░░░░░░░░░` 14.1% |
| Repossession | 23,487 | `█░░░░░░░░░░░░░░░░░░░` 5.2% |
| Donation | 9,068 | `░░░░░░░░░░░░░░░░░░░░` 2.0% |
| IAA Purchase | 4,924 | `░░░░░░░░░░░░░░░░░░░░` 1.1% |
| Lease/Rental | 4,494 | `░░░░░░░░░░░░░░░░░░░░` 1.0% |
|   | 71 | `░░░░░░░░░░░░░░░░░░░░` 0.0% |

</details>


<details>
<summary><strong>Listings by Branch State</strong> (<code>branchState</code>)</summary>


| Value | Count | Share |
| --- | --- | --- |
| CA | 57,799 | `████░░░░░░░░░░░░░░░░` 21.1% |
| TX | 56,877 | `████░░░░░░░░░░░░░░░░` 20.8% |
| GA | 25,975 | `██░░░░░░░░░░░░░░░░░░` 9.5% |
| FL | 23,454 | `██░░░░░░░░░░░░░░░░░░` 8.6% |
| NC | 23,301 | `██░░░░░░░░░░░░░░░░░░` 8.5% |
| NY | 20,782 | `██░░░░░░░░░░░░░░░░░░` 7.6% |
| OH | 20,039 | `█░░░░░░░░░░░░░░░░░░░` 7.3% |
| IL | 16,442 | `█░░░░░░░░░░░░░░░░░░░` 6.0% |
| VA | 15,217 | `█░░░░░░░░░░░░░░░░░░░` 5.6% |
| PA | 14,093 | `█░░░░░░░░░░░░░░░░░░░` 5.1% |

</details>






---

## Pre-built Views on Rebrowser

Rebrowser web viewer lets you filter, sort, and export any slice of this dataset interactively. These pre-built views are ready to open:


### Auction Listings


[Listings with Buy Now Price](https://rebrowser.net/products/datasets/iaai/auction-listings/views/listings-with-buy-now) — 89,259 records

↳ `[{"field":"buyNowIndicator","op":"isTrue","value":true},{"sort":"buyNowPrice ASC"}]`

[Run and Drive Vehicles](https://rebrowser.net/products/datasets/iaai/auction-listings/views/run-and-drive-vehicles) — 269,113 records

↳ `[{"field":"runAndDrive","op":"isTrue","value":true},{"sort":"_lastSeenAt DESC"}]`

[Collision Total Loss Vehicles](https://rebrowser.net/products/datasets/iaai/auction-listings/views/collision-total-loss) — 289,423 records

↳ `[{"field":"lossType","op":"is","value":"Collision"},{"sort":"_lastSeenAt DESC"}]`

[Theft Recovery Vehicles](https://rebrowser.net/products/datasets/iaai/auction-listings/views/theft-recovery-vehicles) — 6,813 records

↳ `[{"field":"lossType","op":"is","value":"Theft"},{"sort":"_lastSeenAt DESC"}]`

[Insurance Company Listings](https://rebrowser.net/products/datasets/iaai/auction-listings/views/insurance-seller-listings) — 317,624 records

↳ `[{"field":"origin","op":"is","value":"Insurance"},{"sort":"_lastSeenAt DESC"}]`


*[See all 40 views →](https://rebrowser.net/products/datasets/iaai/auction-listings)*




---

## Code Examples

```python
import pandas as pd
from pathlib import Path

# ── Auction Listings ─────────────────────────────────────────────────────────
files = sorted(Path('rebrowser/iaai-dataset/auction-listings/data').glob('*.parquet'))[-7:]
df = pd.concat([pd.read_parquet(f) for f in files])

# Top 10 makes by listing volume
print(df['make'].value_counts().head(10).to_string())

# Average mileage by vehicle class for collision total losses
collision = df[df['lossType'] == 'Collision']
print(collision.groupby('vehicleClass')['mileage'].mean().sort_values().round(0).to_string())

# Loss type distribution across all listings
print(df['lossType'].value_counts().to_string())

# Run-and-drive listings by branch state (top 10 states)
drivable = df[df['runAndDrive'] == True]
print(drivable['branchState'].value_counts().head(10).to_string())

# Title code breakdown for theft recovery vehicles
theft = df[df['lossType'] == 'Theft']
print(theft['titleCode'].value_counts().to_string())
```

---

## Use Cases


### Salvage Valuation Modeling

Build pricing models using loss type, damage location, mileage, title status, and vehicle specs. Compare across branches and states to identify regional price variations.


### Theft Recovery Analysis

Filter by loss type to study theft recovery patterns by make, model, and state. Identify which vehicles are most frequently recovered and their typical condition at auction.


### Inventory Sourcing

Monitor auction listings by vehicle class, drivetrain, and branch location to find inventory matching rebuild or parts sourcing criteria. Track run-and-drive status and key availability.


### Market Trend Research

Track shifts in loss type distribution, vehicle class mix, and geographic auction volume over time. Analyze how catastrophe events and seasonal patterns affect regional supply.



---

## Full Dataset on Rebrowser


This repo is a 1,000-row preview sample. The full dataset is at [rebrowser.net/products/datasets/iaai](https://rebrowser.net/products/datasets/iaai)

Doing academic research? You may qualify for free access to a larger slice. See [Free Datasets for Research](https://rebrowser.net/free-datasets-for-research).

On Rebrowser you can:
- **Filter before you buy** — use the web UI to apply filters on any field and sort by any column. Preview results before purchasing. You only pay for records that match your criteria.
- **Export in your format** — CSV, JSON, JSONL, or Parquet depending on your plan.
- **Access via API** — integrate dataset queries into your pipelines and workflows.
- **Choose your freshness** — plans range from a 14-day lag to real-time data with no delay.
- **Select only the fields you need** — keep exports lean. Premium fields with richer data are available on higher plans.

[Pricing](https://rebrowser.net/pricing) starts at **$2 per 1,000 rows** with volume discounts.

---

## License & Terms

**Free for research and non-commercial use** with attribution. See [license terms](https://rebrowser.net/free-datasets-for-research#license) and [how to cite](https://rebrowser.net/free-datasets-for-research#citation).

```bibtex
@misc{rebrowser_iaai,
  author       = {Rebrowser},
  title        = {IAAI Insurance Auto Auction Dataset},
  year         = {2026},
  howpublished = {\url{https://rebrowser.net/products/datasets/iaai}},
  note         = {Accessed: YYYY-MM-DD}
}
```

Commercial use requires a paid license — see [pricing](https://rebrowser.net/pricing). Use of this data is governed by the [Rebrowser Terms of Use](https://rebrowser.net/terms-of-use), which may be updated at any time independently of this repository.

---

## Disclaimer

Rebrowser is an independent data provider and is not affiliated with, endorsed by, or sponsored by IAAI. Any trademarks are the property of their respective owners. This dataset is compiled from publicly available information; we do not request or collect IAAI user credentials. By using this dataset, you agree to comply with IAAI's Terms of Service and all applicable laws and regulations. Images, logos, descriptions, and other materials included in this dataset remain the intellectual property of their respective owners and are provided solely for informational purposes. Rebrowser makes no warranties regarding the accuracy, completeness, or legality of the data and assumes no liability for how the data is used. You are solely responsible for ensuring that your use of this dataset does not infringe on the rights of any third party.


You can also find this data on [Kaggle](https://www.kaggle.com/datasets/rebrowser/iaai-dataset), [HuggingFace](https://huggingface.co/datasets/rebrowser/iaai-dataset), [Zenodo](https://doi.org/10.5281/zenodo.18854631).


