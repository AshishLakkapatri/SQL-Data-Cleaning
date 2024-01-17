## Overview
This project focuses on data cleaning and transformation for the `NashvilleHousing` dataset within the `PortfolioProject` database. The script performs various tasks to standardize date formats, populate missing property addresses, break down addresses into individual columns, handle owner address components, change 'Y' and 'N' values to 'Yes' and 'No,' remove duplicates, and delete unused columns.

## Standardize Date Format
The initial section standardizes the `SaleDate` format by converting it to the `Date` data type. In case of issues, a new column `SaleDateConverted` is added, and the conversion is attempted again.


## Populate Property Address Data
This section populates missing property addresses by matching records with the same `ParcelID` and different `UniqueID`. The script updates records with null property addresses based on available data from matching records.



## Break Out Addresses into Individual Columns
This section separates the `PropertyAddress` column into `Address` and `City` columns. New columns `PropertySplitAddress` and `PropertySplitCity` are added to store the separated data.

## Handle Owner Address Components
Similar to the `PropertyAddress`, this section separates the `OwnerAddress` into `Address`, `City`, and `State`. New columns `OwnerSplitAddress`, `OwnerSplitCity`, and `OwnerSplitState` are added for the respective components.



## Change 'Y' and 'N' to 'Yes' and 'No' in "Sold as Vacant" Field
The script converts 'Y' and 'N' values in the `SoldAsVacant` field to 'Yes' and 'No,' respectively.



## Remove Duplicates
This section identifies and retains only unique records based on a combination of `ParcelID`, `PropertyAddress`, `SalePrice`, `SaleDate`, and `LegalReference`.


## Delete Unused Columns
Unused columns such as `OwnerAddress`, `TaxDistrict`, `PropertyAddress`, `SaleDate` are removed from the dataset.

